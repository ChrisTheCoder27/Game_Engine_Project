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


# State
