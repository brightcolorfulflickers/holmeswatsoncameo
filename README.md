# holmeswatsoncameo
An electronic Holmes &lt;3 Watson cameo

![Holmes <3 Watson Necklace](https://github.com/brightcolorfulflickers/holmeswatsoncameo/blob/master/photos/necklace.jpg)

## Overview
I made this steampunky-ish necklace to celebrate my favorite Victorian characters, Holmes and Watson. I totally ship them, as does this necklace. It's inspired by [this Adafruit tutorial](https://learn.adafruit.com/steampunk-cameo-necklace/overview), but I modified it heavily. Full instructions are below.

## Tools Required

I used a soldering iron, sewing machine, heat gun, solder sucker, and needle nose pliers. You may optionally use a laser cutter.

## Parts Used

Electronic parts:
- [Adafruit 5V Pro Trinket](https://www.adafruit.com/product/2000)
- [Pro Trinket LiPoly Backpack](https://www.adafruit.com/products/2124)
- [105 mAh battery](https://www.adafruit.com/product/1570)
- [Slide switch](https://www.adafruit.com/products/805)
- 1.3" OLED display (see below)
- 30 AWG stranded silicone wire
- Heat shrink

Other parts:
- E6000 adhesive
- Metal to glass adhesive
- Hot glue
- [Cameo setting](https://www.etsy.com/listing/123154408/40x30mm-antique-bronze-setting)
- 8 mm bronze jump ring (find at any craft store)
- [Textured ring](https://smile.amazon.com/Cousin-Jewelry-Basics-5-Piece-Textured/dp/B005MAX4L0?ie=UTF8&sa-no-redirect=1) (also found at A.C. Moore)
- 7/8" black grosgrain ribbon
- Adhesive-backed felt
- Black thread

## OLED Display

The OLED display requirements are a bit tricky! There are many 1.3" OLED displays available on Aliexpress and Ebay. The original Adafruit OLED can also be used but it's very expensive and frequently out of stock. Here's how to select an OLED.

Check the dimensions. It must be narrower than your cameo setting. If you use the one I linked above, you must choose an OLED that is no wider than 32 mm.
Example: [32mm wide OLED](http://www.aliexpress.com/item/1-3-Inch-White-I2C-IIC-Serial-128X64-OLED-LCD-LED-Display-Module-for-Arduino-51/32303252088.html).
Incompatible: [33.5mm wide OLED](http://www.aliexpress.com/item/blue-and-white-color-128X64-1-3-inch-OLED-LCD-LED-Display-Module-For-Arduino-1/32276891410.html). Much cheaper, but too wide for the setting I used. May be okay if you use a different setting.

Be sure to check the driver of the OLED display you select and ensure its compatibility with the u8glib library. Both of the ones linked above are compatible. It doesn't really matter if you get one that's SPI or I2C. You will have to figure out which pins to use.

Before you solder anything, test your display. Install the u8glib library. Test your display with an Arduino Uno (or clone etc). The u8glib library has examples you can upload, and you'll need to uncomment the correct initialization line for your display. These displays use either the SSD1306 or SH1106 chip. Find one of those lines with 128x64, select one for SPI or I2C as appropriate, uncomment, and upload. Once you've found the correct one, make a note of it. Make a note of the pins as well and update the define statements.

## Instructions

The Adafruit tutorial linked above gives a good overview, but there are some deviations to make. Read that through without doing anything yet. Also read the [LiPo backpack tutorial](https://learn.adafruit.com/adafruit-pro-trinket-lipoly-slash-liion-backpack).

Follow the LiPo backpack tutorial, with some minor change. You will need to also solder the ground wire for the display to the ground pin where the pins are, which is tricky. Also add heat shrink to the slide switch pins. You will not be soldering the battery wires directly to the board as they do in the original Adafruit cameo tutorial. Just plug in the battery with a JST extension cord.

Desolder the header pins from the OLED display. I have found the easiest way to do this is to place the board in a vice, flow the solder, and pull the pin out with pliers from the other side. Once you remove all the pins, clean up the solder with a solder sucker/solder wick. I like to flow the solder with the iron from one side of the board and vacuum it up from the other.

Largely follow the original cameo tutorial through the soldering section, but be sure to use the appropriate pins as found during the OLED test. Stop before gluing anything!

I recommend uploading the code from my repository before gluing anything. This will allow you to properly place the display. Update my code using the initialization settings you found above.

Apply hot glue as needed to wires for strain relief. You can hot glue the back of the OLED board to the back of the Pro Trinket, but I've found this comes undone over time. E6000 will be permanent, so maybe hold off on that until you're totally ready.

Print out the felt pattern.svg on paper and cut it out. Place in the setting. Make sure it works well or adjust as needed. Once you're satisfied, laser cut the felt using the svg provided. Alternately, print it out, trace it on the backing, and cut by hand.

Place the felt in the setting but don't remove the backing yet. Place the OLED so that you get an idea of how to center the screen, then remove. Now remove the backing and stick the felt to the setting. Once again, see how to place the display. Then add metal-glass glue to the corners of the OLED screen and place it. Hold it firmly for a minute until it sets.

Attach the jump ring to the setting and the large, textured ring.

Okay, now make the ribbon! I feel like the Adafruit tutorial doesn't explain this very well so I'll explain what I did. Measure the ribbon so that it's the desired length and add some slack for tying it behind your neck. Hem the ends of the ribbon; this stuff frays easily. Now tie it around the textured ring. You will want to cut pieces to make a second layer, as explained in the tutorial, to make a channel for the battery. Do that, and be sure to hem the edges before sewing it to the main ribbon. I cut down the JST extension cord, re-soldered, and heat-shrunk. I also made a fake "channel" for the other side to balance it.

You'll then want a little piece of black ribbon to tie around the textured ring to obscure the wire. Measure that, cut it, hem the ends, and tie.

You're finished!