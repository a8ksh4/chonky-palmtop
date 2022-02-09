# Chonky Palmtop
It struck me to put this together when I saw how close in size the 7" touchscreen, battery cells, and crkbd folded vertically that I had sitting on my desk were.  

The li-on cells aren't the best choice for energy density, but they can fast charge  - limited only by the gauge of the wire I connect tehm with, and if I change them later, therer's room in the battery box for a bunck of 18650 cells instead.

## Status


## Keyboard Pivot Geometry
One corner of each keyboard half moves up the center of the chassis on a straight path.  The other povot point follows some other path to acheive the desired total rotation, and we have some control over how it gets there by curving the path it follows.

We can figure out the starting and ending points of the second pivot by projecting it's location closed and open, and then drawing a path between them.  See the yellow lines in the cad sketch below.  We use a path that first curves down to help us dip the keyboard around the hinges that hold the display.  

<img src="Images/kb-flip-projection.png">

## Power System


## Materials List
* Pi 4 (4gb minimum)
* Ampripper 3k PSU/Charger: https://www.tindie.com/products/kickstart_design/ampripper-3000-5v-3a-lipo-battery-charger/
* Chonker spim08hp cells:https://batteryhookup.com/products/2x-spim08hp-3-7v-8ah-cells-with-threaded-insert
* 7" Touchscreen: https://www.amazon.com/gp/product/B07L6WT77H/
* USB Hub: https://www.amazon.com/gp/product/B00L2442H0/
* Hinges: https://www.amazon.com/gp/product/B07GX8LQCX/
* Bolt and Nut Kit: https://www.amazon.com/gp/product/B093FWLJZC/
* 1/4" Screws: https://www.amazon.com/gp/product/B00GDYNHL6/
* 3/8" Screws: https://www.amazon.com/gp/product/B00GDYNJNM/
* Crkbt Classic PCB: https://www.littlekeyboards.com/collections/corne-pcb-kits/products/crkbd-classic-essentials-kit
* Your choice of choc switches.
* Diodes
* mcu, e.g. pro micro or elite c
* Machine Pin Sockets for mcu: https://www.adafruit.com/product/3647, https://www.adafruit.com/product/3646
* Keycaps: https://www.littlekeyboards.com/collections/keycaps/products/mbk-choc-low-profile-keycaps
* 22 Gauge Silicon Wire: https://www.amazon.com/gp/product/B07T4SYVYG/
* 18 Gauge Silicon Wire: https://www.amazon.com/gp/product/B073RDBW7L/
* In-line Fuses: https://www.amazon.com/gp/product/B07ZTYN9DY/ (higher amperage would be better maybe)
)
* XT60 Connector: https://www.amazon.com/gp/product/B01ETROGP4/
* Voltage Indicator: https://www.amazon.com/gp/product/B00YALUXH0/
* 6mm Tactile Buttons:  https://www.adafruit.com/product/367
* 6mm Clear Top Buttons: https://www.adafruit.com/product/4183
* Switch: https://www.amazon.com/gp/product/B008CZIG3I/

## Keyboard Firmware
Using the Miryoku Firmware found here: https://github.com/manna-harbour/miryoku  
<img src="Images/miryoku-kle-cover.png"/>


## Authors and acknowledgment
Thanks to the Cyberdeck Cafe Discord and the Cyberdeck Reddit for loads of inrpiration and collaboration!

## License
Creative Commons Share Alike

## Project status
If you have run out of energy or time for your project, put a note at the top of the README saying that development has slowed down or stopped completely. Someone may choose to fork your project or volunteer to step in as a maintainer or owner, allowing your project to keep going. You can also make an explicit request for maintainers.
