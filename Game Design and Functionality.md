

# Game Design and Functionality

The Snake Game is based on a classic single‑player mode in which the player must navigate an endless snake that becomes longer as it consumes objects. The objective of the game is to keep the snake alive for as long as possible without touching the snake's body or the game’s boundaries. Additionally, the game is completely real‑time, and the player must use keyboard commands (WASD or arrow keys, depending on the game) to navigate the snake.

The game operates in only one main mode, which is **Player Mode**, where the player directly operates the snake. This game is based on reflexes. The game loop runs based on timing functions provided by JavaScript, where it constantly updates positions, checks collisions, and draws the game board at fixed intervals.

The grid movement system is the basis for the game's mechanics; the snake moves from one cell to another per second, and food appears at randomly selected empty positions. The head position and the boundaries or body cells within the snake are used to detect collisions. The game's speed is either constant or increases gradually depending on the circumstances. Sound effects are included when food is eaten or when the game ends.



# Technical Architecture

It is developed using HTML, CSS, and JavaScript, and its resource files are arranged into distinct directories for scripts, styles, images, and audio according to the correct directory structure. The game is rendered using DOM manipulation rather than the canvas engine, which allows for user accessibility but is less suited for animations. Global variables are used to control the state of this procedural game.



# A. Strengths

- Simple and intuitive gameplay, so anyone can play.  

- Clean project structure, with assets organized in meaningful folders. 

- Functional collision detection and grid movement.  

- Inclusion of audio assets improves the gaming experience through responsive sounds.



# B. Weakness

## i) Technical Weaknesses

- Overreliance on global variables, making the code less modular and scalable.  

- Limited audio control: no ability to control volume or mute audio.  

- No persistent storage, meaning scores or settings are not saved between sessions.



## ii) User Experience Issues

- No pause feature, meaning the player must play until the end.  

- Minimal customization, such as themes, grid sizes, or snake skins.  

- Lack of visual feedback, such as animations, score pops, or game‑over screens.  

- No adjustable difficulty, so speed and challenge level cannot be changed.



# Areas for Improvement

- Refactor the code into modules such as Snake, Food, and Game classes.  

- Enable pause and resume functionality.  

- Include high scores using `localStorage` so data persists even after closing the game.  

- Enhance graphics and animations to make movement more fluid.  

- Add difficulty modes, such as increasing speed or introducing obstacles.
