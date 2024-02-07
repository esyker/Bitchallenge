# Bitchallenge

This work was produced as part of a challenge held in University of Lisbon in 2017 for the students of Electrical and Computer Engineering. 
This work achieved the 1st place in the aforementioned challenge.
`Arduino.io` contains the source code for the Arduino gaming console, where it is possible to play four different classical games:
* Snake
* Space Invaders
* Tetris
* Breakout

Our project consists of a portable console, composed of an LCD
monochrome, four buttons, and an Arduino, on which it is possible to play various games
classics: Snake, Tetris, Breakout and Space Invaders. The console obtains power through
a USB cable (connected to a Power Bank for example).

Frontal view of the console:

![image](https://github.com/esyker/Bitchallenge/assets/50277636/dfdfd759-0a44-4018-9dfb-d69b6bab1caa)

Lateral view of the console:

![image](https://github.com/esyker/Bitchallenge/assets/50277636/53721b37-b326-4696-8248-8d391eee0c41)

Frontal view of the console, connected to a Power Bank:

![image](https://github.com/esyker/Bitchallenge/assets/50277636/7c3f715c-a0ac-484b-81df-db6ce6cdd5c7)

### Connections Schema

The diagram in the following figure shows all the connections of our project
(resistances are 10kΩ).

![image](https://github.com/esyker/Bitchallenge/assets/50277636/d65ca021-c892-4a1d-a0a1-d0f5cde77d42)

### Extra Functionalities

##### EEPROM

The EEPROM library allows you to store variables in the Arduino's persistent memory. This way, even when the console is disconnected from the power supply, the variables stored will remain intact. In our project, we used this functionality to save setting values ​​(difficulty and backlight) as well as maximum scores of all games, which are shown when the player finishes (loses or wins) a game, as follows:

![image](https://github.com/esyker/Bitchallenge/assets/50277636/fb53b9d3-ce87-4739-901b-aeb30afd2711)

#### Low Power

The LowPower library contains the powerdown(…) function that allows you to power the Arduino
in standby state until an interruption is detected. In our project, Arduino comes in
in this state when the user is in the main menu and clicks the red key and returns
to the normal state when the user clicks the green key. This way, when you are not
being used, the console remains in standby state and saves energy.

#### Cost of Materials

However, not all purchased materials were used (e.g.
we only used one of the 10 prototyping boards), so:
Actual cost of the prototype (estimate): €23.69.

* Arduinto €20.
  
* Display Nokia 5110
![image](https://github.com/esyker/Bitchallenge/assets/50277636/ecd71e51-a081-4b4a-8171-44e76d5800a2)

* Wires
  ![image](https://github.com/esyker/Bitchallenge/assets/50277636/75747e3b-ca17-4759-9a81-83d990eaac9c)

* Prototyping boards 
![image](https://github.com/esyker/Bitchallenge/assets/50277636/60f3c33b-2406-4b64-b68d-62f30ad82cb1)

* Buttons and Resistances
![image](https://github.com/esyker/Bitchallenge/assets/50277636/1d6c27e4-8c1c-49c9-9c4c-61830f956e3d)





### Menus

When we turn on the console, the first screen that appears is the main menu, where
we can choose two options: Games or Settings. In the Games submenu we can
choose one of the games available on the console and in the Settings submenu we can change
console settings, namely turning the LCD backlight on/off and changing
the difficulty of the games. To navigate through the menus, use the left and right keys.
right to change the selected menu, a green key to go to the selected menu
and a red key to return to the previous menu.
Below are illustrative images of the menus:

![image](https://github.com/esyker/Bitchallenge/assets/50277636/3b8f49c5-d8ab-41a2-a1fe-27f99701359a)

### Snake

The player controls a snake that moves around the screen, picking up apples and not
could collide with your own body. Every time the snake eats an apple, its
body grows and the score increases. The player controls the direction of the snake's head
(up, down, left and right) and your body follows. The greater the
difficulty, the faster the snake moves

Controls:
• Left Key: changes the direction of the snake 90º counterclockwise;
• Right Key: changes the direction of the snake 90º clockwise;
• Red Key: returns to the games menu

![image](https://github.com/esyker/Bitchallenge/assets/50277636/1cb6e584-edad-4571-b76c-99ebec6ef522)

### Tetris

The game consists of stacking pieces of different shapes that go down the screen.
to complete horizontal lines. When a complete line is formed, it
disappears, the upper layers descend, and the score increases. When the stack of
pieces reaches the top of the screen, the game is over. The greater the difficulty, the greater the
falling speed of the pieces.
Controls:
• Left Key: moves the current piece one unit to the left (or more
if the key is pressed for a few moments);
• Right Key: moves the current piece one unit to the right (or more if the
key is pressed for a few moments);
• Green Key (when clicked): rotates the current piece 90º clockwise;
• Green Key (when pressed): causes the piece to fall further
quickly;
• Red Key: returns to the games menu

![image](https://github.com/esyker/Bitchallenge/assets/50277636/352e190b-d545-49aa-bd78-99a804f55cb0)

### Breakout

The player controls a platform that moves horizontally at the bottom
of the screen. At the beginning of the game, there is a layer of blocks at the top of the screen that
player has to destroy using a ball. When a block is hit by the ball,
This bounces, the block is destroyed and the score increases. The block layer will
growing as the player destroys it. The player loses if he lets the ball fall
at the bottom of the screen or if you let the block layer reach that same part
of the screen. By increasing the difficulty, the speed of the ball increases.
Controls:
• Left Key: moves the platform to the left;
• Right Key: moves the platform to the right;
• Red Key: returns to the games menu

![image](https://github.com/esyker/Bitchallenge/assets/50277636/54aacf6e-ac3c-4f40-8cad-89345ee3647f)

### Space Invaders

The player controls a spaceship that shoots bullets and moves sideways through the
screen. The objective is to destroy all invading “aliens” that move not only
laterally but also downwards, in the direction of the ship, each time they reach the
screen limits. The player loses if he is hit by a bullet fired by an alien
or if the aliens reach the height of the ship. An increase in difficulty makes
increase the difficulty of the aliens' movement and their shooting speed, as well as
such as the number of bullets fired.
Controls:
• Left Key: moves the platform to the left;
• Right Key: moves the platform to the right;
• Green Key: fires a bullet;
• Red Key: returns to the games menu.

![image](https://github.com/esyker/Bitchallenge/assets/50277636/b112121c-082e-4131-8df8-cb2917b045d1)





