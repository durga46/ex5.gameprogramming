# Ex No :04

# <p align="center">  Making Player to collect the ammo and increase the bullet spawn count. </p>
## AIM:
To create ammo to increase the bullet count and increase the bullet spawn count.

## ALGORITHM:
### For Adding Bullet Count:
#### STEP 1: Create a HUD Blueprint:
In the Content Browser, right-click in the desired folder.
Select Create Basic Asset > Blueprint Class.
In the Class Settings window, search for "HUD" and select it as the parent class. Name the Blueprint (e.g., "GameHUD") and click Create.
### STEP 2: Open the GameHUD Blueprint:
Open the GameHUD Blueprint you just created.
In the Blueprint editor, find the Canvas panel on the left.
Add a Text block widget to the Canvas panel to display the bullet count.
Position the Text block widget on the canvas as desired.
### STEP 3: Create a reference to the player character:
In the GameHUD Blueprint, create a variable of the player character's class to store a reference to it.
To do this, go to the Variables panel and click the "+" button.
Set the variable type to the class of your player character (e.g., ThirdPersonCharacter).
Name the variable (e.g., PlayerCharacter).
### STEP 4: Update the bullet count display:
In the GameHUD Blueprint, locate the Event Tick event.
Drag off the PlayerCharacter variable and search for "Get Bullet Count" (assuming you have a bullet count variable in your player character Blueprint). Connect the output of the Get Bullet Count node to the Text block widget's Text property.
You may need to format the bullet count value as a string before connecting it to the Text property.
### STEP 5: Set the GameHUD as the active HUD:
Open your player character Blueprint.
In the Blueprint editor, locate the Event Begin Play event.
Drag off the execution line and search for "Create Widget".
In the Create Widget node, select the GameHUD Blueprint you created.
Drag off the return value of the Create Widget node and search for "Add To Viewport".
Compile and save the player character Blueprint.
### STEP 6: Test the bullet count display:
Play the game in the editor.
Ensure that the bullet count is displayed on the screen as you interact with the game, such as firing bullets or picking up ammo.
## OUTPUT:
### In Play Mode:
### Before collection:
Screenshot (52)

### After collection:
Screenshot (53)

### Canvas:
image

### Bullet Count Grap:
image

## ALGORITHM:
### For Adding Ammo:
### STEP 1: Create an ammo actor:
In the Content Browser, right-click in the desired folder.
Select Create Basic Asset > Blueprint Class.
In the Class Settings window, search for "Actor" and select it as the parent class. Name the Blueprint (e.g., "AmmoActor") and click Create
### STEP 2: Set up the ammo actor:
Open the player's character Blueprint.
In the Blueprint editor, locate the event that handles the collision or overlaps with the ammo actor.
Add a new custom event node to handle the interaction.
Implement logic to increase the bullet count for the player:
Access the player's character or controller reference.
Increment the bullet count variable or property. Play a sound or visual effect to indicate the pickup.
Destroy the ammo actor after it has been collected.
### STEP 3: Implement the player's interaction with the ammo actor:
In the GameHUD Blueprint, create a variable of the player character's class to store a reference to it.
To do this, go to the Variables panel and click the "+" button.
Set the variable type to the class of your player character (e.g., ThirdPersonCharacter).
Name the variable (e.g., PlayerCharacter).
### STEP 4: Place the ammo actor in the level:
Drag and drop the AmmoActor Blueprint into the level where the player can interact with it.
Adjust its position and orientation as n
### STEP 5: Test the ammo pickup functionality:
Compile and save the AmmoActor Blueprint and the player's character Blueprint. Play the game and navigate the player character to the ammo actor.
Ensure that when the player character overlaps or collides with the ammo actor, the bullet count increases, and the ammo actor disappears
## OUTPUT:
### Event Graph:
image

### Increase Bullet Count in Ammo Actor:
image

## RESULT:
Thus, added ammo to increase the bullet count and displayed it in play-mode
