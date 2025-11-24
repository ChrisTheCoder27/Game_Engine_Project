# Game Project Description
This scenario has the player exploring a forest where they're collecting resources to bring back to their cabin to protect themselves against monsters when night falls. The player can walk, sprint, jump, crouch, pick up items, and interact with certain objects. They also have a flashlight that they can toggle on and off. They can pick up resources like firewood, planks, and food to use in their cabin. There is no combat, so the player has to either run or hide from the monsters. The player has to go through a single day and survive until morning without getting caught by the monsters. The game can be quit at any time by pressing the escape key.

# Improvements on Previous Deliverables
The first improvement made was to the singleton design pattern and the player's UI. The player's health (HP) and stamina (SP) is now displayed using bars instead of just text. HP uses both text and a bar because the player needs to know precisely how much HP they have at any given time to make proper decisions. SP is just a bar because it gives the player a better look at how much stamina they have left compared to looking at a number rapidly going up or down.<br>
<img width="362" height="131" alt="image" src="https://github.com/user-attachments/assets/1fb50df1-8cdb-46ec-bd7e-394d5cf40d43" />
<br> Another improvement made was to the factory design pattern, where the player can use the "fruit" item. If the player has a fruit in their inventory, and they press the use button, then they will eat the fruit (which removes it from their inventory) and regain some of their health. If there is no fruit in the player's inventory, then nothing will happen.
<img width="1304" height="291" alt="image" src="https://github.com/user-attachments/assets/f2ddb4ab-b03f-4d17-bc5f-3e4d89859359" />
<br> Another improvement made was to the enemy, which can now move around, either patrolling between a set of waypoints or chasing the player. Using a navigation mesh, the enemy uses "AI MoveTo" to move between different waypoints placed in the level, and if the enemy sees the player, it will start chasing them.
<img width="1743" height="752" alt="image" src="https://github.com/user-attachments/assets/e8829b9f-9848-4e8a-ae02-69d3708f2c41" />

# Optimization


# Observer
I implemented an observer pattern by having the subject, UIGameInstance, send a notification to all observers when the player runs out of stamina. This is done by getting all actors with the interface BPI_Observer and performing a for loop to call the notify function for each observer. The observer interface, BPI_Observer, creates a notify function that is overwritten for each observer to perform the specific action that it needs to take when something has changed, which is the player's stamina reaching 0. The first observer is the player, which sets the "IsSprinting" bool variable to false and the "IsTired" bool variable to true, forcing the player to stop sprinting and prevents them from sprinting for a few seconds. The other observer is BP_AudioObserver, which simply plays a creepy breathing sound when notified. These observers add to my project since it's a horror game and the player being unable to sprint for a short time after running out of stamina causes them to panic, especially if they're being chased by an enemy. Combining this with the creepy sound effect that is played, it helps add to my project's intended atmosphere by making the player feel uncomfortable and scared.
<img width="737" height="1124" alt="image" src="https://github.com/user-attachments/assets/f6bd8406-ebf4-41ed-bf40-d946454cfcc4" />

# State
