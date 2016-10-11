## Hello World - Maker Garage Edition

The [Othermill](https://othermachine.co/othermill/features/) is an easy-to-use desktop CNC mill that can fabricate amazing things out a variety of materials, including wood and metal. It’s also great for prototyping PCBs. This is tutorial is based on [Other Machine's Hello World](https://othermachine.co/support/tutorials/hello-world-otherplan-public-beta/) and modified with their permission to make it shorter and use cheaper material!

This tutorial is designed for Othermill and CNC beginners, and we will walk you through all the steps.

You will use Otherplan, the software that drives the CNC mill. It's already installed on PC next to the Othermill in the Garage. 

This tutorial covers:

* Getting familiar with Otherplan 
* Getting familiar with basic operations of the Othermill: loading tools, loading material, running a job
* Using Otherplan with a PCB design (the file is provided in the next step)

You will find the wrenches, end mill and pre-cut pieces of material in the drawer under the Othermill.

### Step 1: Materials, Tools, Files


![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/01-materials.JPG)

Tools
* Computer running Otherplan
* Calipers to measure your board
* 2 wrenches
* end mill (1/32")
* vacuum cleaner to clean-up when you're done


Materials
* Boards (MDF or PCB)
* Double sided tape


Files
* [Hello_World_Mini.brd](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/Hello_World_Mini.brd) - Make sure to save it as a BRD file!


### Step 2: Set Up Otherplan and Your Othermill

* Login to the PC
* Open Otherplan by double-clicking on the icon on the desktop
* Turn on your Othermill using the power switch on the back of the machine.
* Enjoy the mill’s cheerful beeping startup (these beeps sound only when all the windows are in place).
* In Otherplan, a dialogue will pop up asking you to “Start Homing” the machine. Homing tells the machine where it is in space and makes sure the position of the tool in the machine matches the position of the tool in the software. This ensures that all your cuts are exactly where you want them to be.
* Click the Start Homing button.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/01-home.png)

The Othermill will go through its homing procedure, which will take a few seconds. You’re now ready to set up your file!

### Step 3: Set Up Your File in Otherplan
* In Otherplan, click Open Files and select the Hello_World_Mini.brd file that you downloaded.
* You’ll see a rendered version of the file appear on the machining bed in Otherplan, and the file name should appear on the right side of the screen with some options and buttons below. The material dimensions haven’t been set yet, however, so while the file will appear on the top of the material, it will still look strange.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/02-open-file.png)
pb31 
* On the right-hand side of the screen, you’ll see the Configure column, which is made of expandable menus labeled Tool, Material, and Move By, followed by a button labeled Open Files.
* Expand out the "Size" arrow under "Material", and click on the preset dimensions. They should expand out and provide editable fields for you to enter the dimensions of your MDF blank. (Make sure Otherplan is set to view the units you’d like to work with using View > Show Units in Inches/mm.)


![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/03-set-size.png)
pb32 
* Use your calipers to measure the width, length and thickness of your material.

![](https://othermachine.co/assets/pb33.jpg)
pb33 
* Enter the width as the x value, the length as the y value, and the thickness as the z value.
* In the Placement bar directly underneath the z value for the material dimension, enter in .003" (0.076mm) in the z field of the Placement drop-down. This will raise the plan .003" (0.076mm) to make up for the thickness of the tape underneath the board.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/04-set-position.PNG)
pb34 
* Now, in the panel for the plan you opened, select the tool you’re going to use to cut out the circuit board, in this case, is a 1/32" flat end mill, if not already selected.

Your file is ready! Next comes the tool setup.

### Step 4: Set Up Your Tool
* In the upper-right corner of the Otherplan window, click on "Set" (or "Change" if a tool is already selected) to set your tool. This will lower the z-carriage, making it easier to install an endmill, and it will also bring up a dialogue box to walk you through the tool-changing process.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/11-set-tool-b.png)
pb42 

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/12-set-tool-c.png)
pb41 

* In the dialogue box in Otherplan, click Continue and select the tool you want to use. Make sure to choose the 1/32" flat end mill.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/13-set-tool-d.png)
pb43 

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/14-set-tool-e.png)


* The collet is the round device with a hole through it that holds your tool in the machine. It should already be installed on the mill. If you need to put it back, fit the collet, wide end first, into the collet nut, the threaded piece on the end of the spindle where you would expect a tool to go. Then, screw the nut loosely back onto the spindle shaft.

![](https://othermachine.co/assets/Inserting-collet-1.gif)
Inserting-collet-1

* Slide a 1/32" flat endmill into the collet until just a little bit of the wide part of the shaft sticks out. Then use the two wrenches that came with your Othermill to tighten the collet nut onto the spindle. It doesn’t have to be super tight, just snug plus a little bit.

![](https://othermachine.co/assets/Inserting-a-tool.gif)
Inserting a tool

* Click Continue, and the mill will position the tool over the bed. Since we haven’t put the material onto the mill yet, we don’t have to worry about where the tool touches down.


Note: In the future, if you have material loaded before you locate the tool, the machine will go to a spot on the bed it thinks is clear. In that case, make sure the material is truly not in the way, and if it is, double check your material dimensions in Otherplan. Also make sure the tool is not going to sink itself into an alignment bracket hole on the bed. If you are not quite sure where on the bed the tool will touch down, keep your finger on the ESC key and press it if anything looks out of place.
* Click on Locate Tool. The tool will descend to the surface of the machining bed and calculate where the tip of the tool is in space. When the touch-off is complete, the tool will retract but stay in place above the machining bed.

![](https://othermachine.co/assets/pb44.jpg)
pb44 

### Step 5: Put Your Board on the Milling Bed

Now it’s time to position your board in the machine!
* Expand out the Move By arrow underneath the materials settings. Click the Loading button. This will bring the bed of the mill forward.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/otherplan/loading-button.png)
* On the backside of the blank, put an even, non-overlapping layer of double-sided tape across the entire surface.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/02-taping.JPG)
pb51 
* Flip the board tape side down, and stick it to the bed of the mill so that the bottom left corner of the board is flush with the bottom left corner of the aluminum bed.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/03-fixing.JPG)
pb52 


Step 6: Cut Your Board

It’s a good idea to stay close by your mill while it’s cutting. Never leave a working mill unattended.
* Grab whatever you need to get cozy with your Othermill for the next 20 minutes or so.
* Click the "Start Milling" button inside the “Hello_World_Mini.brd” panel. Watch as the mill cuts the traces, holes, and then outline of the file into the board.

![](https://othermachine.co/assets/pb61.jpg)
pb61 

![](https://github.com/brunolewin/othermill/blob/master/helloworld/images/04-milling.JPG)
hw6 carve-1 
* When the mill is finished, vacuum all the chips out and click the Loading button. Grab a putty scraper and gently pry up the board as well as the separated pieces that were cut from it.

![](https://raw.githubusercontent.com/brunolewin/othermill/master/helloworld/images/05-complete.JPG)
hw6 vacuumed-1 

* Clean the edges of your board and use a knife or engraving bit to clear out the holes.

Note: Due to occasional variation in blank thickness, you might notice that when the machine starts cutting, it’s just grazing the surface of the board; this is fine, just let the job complete.

Congratulations, you’ve just made your first project on the Othermill! You can now go explore more on the [Other Machine website](http://othermachine.co).

We hope you make many more, and when you do, share them with us! 

Have questions? Email us at CNCTalk and we’ll be happy to help!
