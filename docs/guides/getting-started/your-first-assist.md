# Creating an Assist From Template

### Download & Install
In order to start creating your assist from the template you will need to download it [Here.](https://cdn.mcleodgaming.com/fraytools/downloads/17745ac3/fraymakers-assist-template-0.1.0.zip)

Once downloaded navigate to your **FrayToolsData** folder

 - Windows: C:\Users\\[YourAccountName]
 - Mac OS X: /User/[YourAccountName] (or press Cmd+Shift+H)
 - Linux: /home/[username] (or ~./)

In the **FrayToolsData** folder open or create a folder called **templates** and extract the contents of the .zip into the folder.

### Creating Your Project From Template
Open FrayTools and click on **File** on the top left and select **New Project From Template**, if you have done the previous steps correctly
you should see the assist template you had just installed, select it. This will create a new project using the files of the template.

### Exporting Your Assist
Before you start messing with your assist It's good to familiarize yourself with the exporting process and making sure you can get the assist in game.

Click on **File** on the top left and select **Publish Project** and then **Publish All** this will creata a .fra file in the build folder of your project.
Next on Steam right click on Fraymakers and go to properties, from there click **Browse** this will take you to the Fraymakers install directory, from here
open or create a folder called **custom** this is the folder where you will put your .fra file.

Once you have put your .fra file into the custom folder you can launch Fraymakers and test out the assist and make sure it's working.

### Tweaking Your Assist
Lets start tweaking the assist template, first we will add a new hitbox.

In the library on the left of the window, click on the entities folder and then open up assist.entity, here you will see the timeline editor. On the left side
click on and open the animations tab to see all of the animations, choose the animation you want to add your hitbox too and then in the timeline editor above the
layers click the insert layer button and select **Collision Box** click the layer and open the properties on the right side of the window. Set the collision box type
to **Hit Box**.

You now have added a new hitbox to the assist but it is only active for the first frame and wont do much right now unless you added it to an animation with an existing hitbox, if you did go ahead and change the index in the properties to be one that the current animation doesnt have.\
Now select the keyframe in the timeline and then drag it to where you want the hitbox to be active and then select however many frames after it you want it to be active, right click and insert frame and then you are free to position the hitbox however you like in the stage editor below.

Lastly in order to give function to the hitbox, in the library navigate to scripts>assist and then open up HitboxStats.hx, in this file you can see the hitbox for
each animation and thier index go ahead and type in the curly braces for the animation you are using 

    hitbox0: { damage: 999, angle: 40, baseKnockback: 999, knockbackGrowth: 999, hitstop: 60, limb:AttackLimb.BODY}

Replace the 0 in "hitbox0" with the index you set for your hitbox, this hitbox will instantantly knock the opponent into the blast zone and have 1 second of hitstop.
This kind of hitbox is not ideal but it's just to show you how it's done.

You can now publish and test this in game.

## Creating an Assist From Scratch
- Work in Progress
