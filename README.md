# Chonky Palmtop
It struck me to put this together when I saw how close in size the 7" touchscreen, battery cells, and crkbd folded vertically that I had sitting on my desk were.  And I I needed a build that was actually functional for normal computer stuff, so this seemed like a good idea.

It turns out that this is a pretty functional setup.  The 7" display is okay as long as I fullscreen stuff.  Alt+F11 works with a lot of stuff so far.  I've been able to use onshape cad in firefox.  It's a little slow, but works as long as firefox doesn't have issues with gfx acceleration.  Console stuff and web browsing are  great!

<img src="Images/finished01.jpg" width="400" />
<img src="Images/finished02.jpg" width="400" />
<img src="Images/finished03.jpg" width="400" />
<img src="Images/finished04.jpg" width="400" />
<img src="Images/finished05.jpg" width="400" />
<img src="Images/finished06.jpg" width="400" />


## Status
The current to-do list:
* Figure out why gfx acceleration is broken for firefox!
* Look into voltage warning wirining to gpio for the psu... not super useful since I don't have a way to actually switch the psu off.
* Rework the lower left hinge bracket with integrated wire protection to match the lid.
* Integrated pwnagotchi with power controls via gpio.  Sort of a separate project...  

<img src="Images/wiring-20220209.jpg" width="200" />
<img src="Images/first-boot.jpg" width="100" />
<img src="Images/side-closed.jpg" width="100" />

## Keyboard Pivot Geometry
One corner of each keyboard half moves up the center of the chassis on a straight path.  The other povot point follows some other path to acheive the desired total rotation, and we have some control over how it gets there by curving the path it follows.

We can figure out the starting and ending points of the second pivot by projecting it's location in the closed and open positions, and then drawing a path between them.  See the yellow lines in the cad sketch below.  We use a path that first curves down to help us dip the keyboard around the hinges that hold the display.  

<img src="Images/kb-flip-projection.png" width="400" />

First draft of the sliders:  

<img src="Images/keyboard11.jpg" width="100" /><img src="Images/keyboard12.jpg" width="200" />


## Power System
The retro psu seems to work well supplying power, but does not have a working low voltage cutoff, so even though it'll warn you that battery voltage is low, it's still up to you to turn it off and protect the battery.  Probaby some otehr low voltage protection should be used between the psu and battery.

This build has two li-ion pouch cells wired in parallel, each separatly fused for 10a for short curcuit protection.  There's an XT60 connection on the side in case I want to rig up a fast-charge.  The li-on cells used here aren't the best choice for energy density, but they can fast charge  - limited only by the gauge of the wire I connect tehm with, and if I change them later, there's room in the battery box for a bunch of 18650 cells instead.

There is a switch and a voltage button on the right side of the screen to turn it on and check the battery level:  

<img src="Images/disp_buttons02.jpg" width="200" />

## USB Wiring
There is a usb hub inside the lid that'r wired with ground, D+, D-, directly to the usb pins on one of the pi ports.  Posotive power comes directly from the psu.  The ground and data wires are bundled with heat shrink to keep them paralle and close so they have the correct impedance for the usb connection.  I tried with them loose and the connection didn't work.  

<img src="Images/usb01.jpg" width="100" />

Before I added a ground wire and bundled them:  

<img src="Images/usb02.jpg" width="100" />  

And another similar build:  

<img src="Images/usb03.jpg" width="100" />


## Chassis Details
Wiring for the front facing ouchscreen controls:  

<img src="Images/disp_buttons01.jpg" width="200" />

Hinges and stuff:  

<img src="Images/hinge1.jpg" width="100" />
<img src="Images/hinge2.jpg" width="100" />
<img src="Images/hinge3.jpg" width="100" />
<img src="Images/battery-box0.jpg" width="100" />

## Materials List
* Printed parts - See the "Stl Files" derectory.
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
