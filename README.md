# Interaction Prototypes

User Interaction Prototypes for KV6002 group project

## Asset Re-use

The texture assets ‘Button_Hovered.fw.png’, ‘Button_Normal.fw.png’, ‘Button_Pressed.fw.png’,  ‘Game Over Screen.png’, ‘Main Menu.png’, and ‘Menu Screen Template.png’ were previously submitted by James Masterton for KF5012 – Software Engineering Practice.

## Instructions/Details for in-game objects

* Cubes = Health pickups: Increase health if below max value; Despawn/set to invisible after use after use
* Spheres = Placeholder for enemy model (collision detection based on collision box attached to sphere, so should be easy to integrate with AI-driven enemies when integrating subsystems): Causes player mesh to flicker 4 times; health decreases by 0.25 per flicker; 0.1 in total for a full collision. Delay used between collisions to prevent instant player death
* Cylinders = Collectibles: Set to invisible and increments player’s collectibles variable upon collision. Game times how long it takes for player to find 3 collectibles and stores value in record variable, which is displayed on HUD along with the time for the current set of collectibles.

## Notes

* The maim menu will only appear if the game is started from the ‘Main’ level.
* If you’re testing the timing system, I’d recommend setting the record for the first level with collectibles that are spaced out across the map, otherwise it’ll be hard to beat the time set.
* The operations making the timing and collectible systems work are currently within the FirstPersonCharacter blueprint for ease of access to the relevant variables, but I think I can make them accessible to the rest of the game (by using an EventTick to keep duplicate variables up to date in the level blueprint using a cast to the first person character.)
* Pause menu is opened using Left Shift
