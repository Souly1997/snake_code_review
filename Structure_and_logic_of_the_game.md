## Structure and Logic of the Game

**Snake Nervana** is a browser-based implementation of the classic Snake game developed using **HTML, CSS, and JavaScript**. The application follows a clear separation of concerns, where HTML is used to define the structural layout of the game interface, CSS is responsible for visual styling and layout, and JavaScript controls the game logic and behavior.

The HTML file provides containers for the game board, score display, and high score display, serving as the foundation upon which the game operates. The CSS file utilizes a grid-based layout to represent the game board, enabling precise placement of the snake and food elements while maintaining responsiveness across different screen sizes. The JavaScript file acts as the core of the application, managing state, user interaction, and real-time updates.

### Game Loop and Timing
The game logic is driven by a continuous game loop implemented using the `requestAnimationFrame()` method, which synchronizes game updates with the browser’s refresh rate. This approach ensures smooth animation and consistent gameplay regardless of device performance. The speed of the snake is controlled by comparing the elapsed time between frames, allowing movement updates to occur at a defined interval. During each cycle of the game loop, the main game engine function is invoked to update the game state and render the latest changes on the screen.

### Snake Movement and Input Handling
Snake movement is handled by updating the positions of its body segments in reverse order, where each segment takes the position of the one preceding it. The head of the snake is then moved in the direction specified by the user’s keyboard input. This method preserves the snake’s structure while allowing continuous motion across the grid.

User input is captured through keyboard event listeners, which update the current movement direction in real time, enabling responsive control of the snake’s movement.

### Collision Detection
Collision detection plays a crucial role in maintaining the game’s rules. The game checks whether the snake’s head collides with its own body or crosses the boundaries of the game board. When a collision is detected, the game enters a game-over state, triggering a sound effect, resetting the snake’s position, and setting the score back to zero. This logic ensures that the player is penalized for invalid movements and that gameplay restarts in a controlled manner.

### Food Consumption and Growth
Food consumption is implemented by comparing the position of the snake’s head with the position of the food element. When both positions match, the snake grows in length by adding a new segment to its head, and the player’s score is incremented. A new food position is then randomly generated within the boundaries of the grid. This mechanism encourages continuous movement and progression while maintaining unpredictability in gameplay.

### Scoring System
The scoring system tracks both the current score and the highest score achieved by the player. The high score is stored using the browser’s local storage, allowing the value to persist across multiple sessions. Each time the current score exceeds the stored high score, the new value is saved and displayed on the screen. This feature enhances replayability by motivating players to improve their performance.

### Rendering
Rendering is performed during every update cycle by clearing the game board and redrawing all visual elements based on the current game state. Each segment of the snake and the food item is represented as a grid element positioned using CSS grid properties. The snake’s head is visually distinguished from the rest of its body to improve clarity and user experience. This rendering approach ensures that the visual representation remains consistent with the underlying game logic.

### Conclusion
Overall, **Snake Nervana** demonstrates a functional and structured implementation of a classic game using modern web technologies. The project effectively applies fundamental concepts such as real-time game loops, grid-based movement, collision detection, and state management. While the current implementation successfully achieves its core objectives, there are identifiable areas for improvement, including better modularization of logic, refined collision handling, and enhanced input validation. Despite these limitations, the project serves as a solid foundation for further extension and demonstrates a clear understanding of interactive game development principles.
