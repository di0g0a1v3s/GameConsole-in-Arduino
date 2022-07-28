# GameConsole-in-Arduino
 Game Console built with an Arduino, with the games Snake, Tetris, Breakout and Space Invaders
 
 

  ## Exterior Images 
This project consists of a portable console, consisting of a monochrome LCD, four buttons, and an Arduino, on which it is possible to play several classic games: Snake, Tetris, Breakout and Space Invaders. The console obtains power via a USB cable (connected to a Power Bank for example).

 <div>

 <img src="https://user-images.githubusercontent.com/60743836/181638659-56339ba6-5025-4dcd-96c1-ae0b9c716ad5.png" alt="drawing" height="300"/>
 <img src="https://user-images.githubusercontent.com/60743836/181638676-5ddc7173-7631-4084-85ad-077a8d1065e5.png" alt="drawing" height="300"/>
 <img src="https://user-images.githubusercontent.com/60743836/181638692-02c24400-b06e-4914-b0cb-cb163e5ec513.png" alt="drawing" height="300"/>
 
 </div>
 


## Schematic 
The diagram in the following image shows all the connections of this project (the resistors are 10kΩ).
 <div>

 <img src="https://user-images.githubusercontent.com/60743836/181638712-dc96d921-9b61-4034-96d6-e7708b8b35e4.png" alt="drawing" height="600"/>
 
 </div>


## Menus

When we turn on the console, the first screen that appears is the main menu, where we can choose two options: Games or Settings. In the Games submenu we can choose one of the games available on the console and in the Settings submenu we can change the console settings, namely turning on/off the LCD backlight and changing the difficulty of the games. To navigate through the menus, we use the left and right keys to change the selected menu, the green key to go to the selected menu and the red key to go back to the previous menu.
Below are illustrative images of the menus:

 <div>
 <img src="https://user-images.githubusercontent.com/60743836/181638728-ec60b541-1a75-4379-a9c5-0bcfe48e706f.png" alt="drawing" height="200"/>
 <img src="https://user-images.githubusercontent.com/60743836/181638742-b9aa0f0d-0819-4968-9a90-6a504bf819a0.png" alt="drawing" height="200"/>
 <img src="https://user-images.githubusercontent.com/60743836/181638747-0508f40b-6995-402b-b220-3fa18e0719b3.png" alt="drawing" height="200"/>
  </div>
  <div>
 <img src="https://user-images.githubusercontent.com/60743836/181638752-62b050f6-a12e-4f37-b920-0c4696cddca7.png" alt="drawing" height="200"/>
 <img src="https://user-images.githubusercontent.com/60743836/181638755-81803110-be10-4075-aa94-b3c3d3b26e0c.png" alt="drawing" height="200"/>
 <img src="https://user-images.githubusercontent.com/60743836/181638761-5a14c20e-2583-40ac-b3ae-2bd6609aeb85.png" alt="drawing" height="200"/>

 </div>
 
## Snake
The player controls a snake that moves across the screen, picking up apples and not being able to collide with its own body. Each time the snake eats an apple, its body grows and the score increases. The player controls the direction of the snake's head (up, down, left and right) and its body follows. The higher the difficulty, the faster the snake moves.

 Controls:
 * Left Key: changes the snake's direction 90º in an anti-clockwise direction;
 
 * Right Key: changes the snake's direction 90º clockwise; 
 
 * Red Key: Returns to the game menu.
 
 <div>
 <img src="https://user-images.githubusercontent.com/60743836/181638771-25f6bfbe-a3ec-4981-b9d7-d4c36741c0a8.png" alt="drawing" height="200"/>
 </div>
 
 
## Tetris
The game consists on stacking pieces of different shapes that go down the screen in order to complete horizontal lines. When a complete line forms, it disappears, the top layers descend, and the score increases. When the pile of tiles reaches the top of the screen, the game is over. The higher the difficulty, the faster the pieces fall.

Controls: 
* Left Key: moves the current piece one unit to the left (or more if the key is held down for a few moments); 

* Right key: moves the current piece one unit to the right (or more if the key is held down for a few moments); 

* Green key (when clicked): rotates the current part 90º clockwise; 

* Green key (when pressed): makes the piece fall faster; 

* Red Key: Returns to the game menu.


<div>
 <img src="https://user-images.githubusercontent.com/60743836/181648507-16b93204-22d6-44f4-9f37-d17cafce672c.png" alt="drawing" height="200"/>
</div>
 

## Breakout

The player controls a platform that moves horizontally at the bottom of the screen. At the beginning of the game, there is a layer of blocks at the top of the screen that the player has to destroy using a ball. When a block is hit by the ball, it bounces, the block is destroyed and the score increases. The layer of blocks grows as the player destroys it. The player loses if he lets the ball fall to the bottom of the screen or if he lets the layer of blocks hit that same part of the screen. As you increase the difficulty, the speed of the ball increases. 

Controls: 
* Left Key: moves the platform to the left; 

* Right Key: moves the platform to the right; 

* Red Key: Returns to the game menu.

<div>
 <img src="https://user-images.githubusercontent.com/60743836/181638971-33a8d5ea-01c8-40ff-bebf-ab9ef72dbc83.png" alt="drawing" height="200"/>
</div>


## Space Invaders 

The player controls a spaceship that shoots bullets and moves sideways across the screen. The objective is to destroy all the invading “aliens” that move not only sideways but also downwards, towards the ship, each time they reach the edges of the screen. The player loses if he is hit by a bullet fired by an alien or if the aliens reach the height of the ship. A difficulty increase increases the aliens' movement velocity and firing speed, as well as the amount of bullets fired.
Controls: 
* Left Key: moves the platform to the left; 
* Right Key: moves the platform to the right; 
* Green Key: fires a bullet;
* Red Key: Returns to the game menu.

<div>
 <img src="https://user-images.githubusercontent.com/60743836/181638988-f9df8dd8-abf5-411d-9539-731048c0d6ac.png" alt="drawing" height="200"/>
</div>

## EEPROM

The EEPROM library allows you to store variables in the Arduino's persistent memory. This way, even when the console is disconnected from power, the saved variables will remain intact. In this project, we used this feature to save the settings values (difficulty and backlight) and also the high scores of all games, which are shown when the player finishes (loses or wins) a game.

## Low Power

The LowPower library contains the powerdown(…) function that allows you to put the Arduino in standby state until an interruption is detected. In this project, the Arduino enters this state when the user is in the main menu and clicks the red key and returns to the normal state when the user clicks the green key. This way, when not in use, the console is in a standby state and saves energy.

## List of Materials:
* Arduino Uno
* Display Nokia 5110
* Jumper wires
* Green PCB
* Buttons and resistances
