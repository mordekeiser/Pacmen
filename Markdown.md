
# Pacman: A Terminal-Based Pac-Man


**Pacman** is a command-line rendition of the classic Pac-Man game, implemented in C++. It offers a nostalgic gaming experience directly within the terminal, utilizing ASCII characters for rendering and standard input for controls.

---

##  Objective of the Study

- Clone and explore the Terminal-Pacman project.
- Analyze the structure, components, and algorithms used.
- Contribute: raise issues, suggest improvements, or make PRs.

---

## 📂 Repository Structure

```
Pacmen/
├── boulder.cpp       # Implementation of boulder obstacles
├── boulder.h         # Declaration of boulder class
├── constants.h       # Game constants and configurations
├── dot.cpp           # Implementation of collectible dots
├── dot.h             # Declaration of dot class
├── game.cpp          # Core game loop and logic
├── game.h            # Declaration of game class
├── ghost.cpp         # Implementation of ghost enemies
├── ghost.h           # Declaration of ghost class
├── main.cpp          # Entry point of the game
├── pacman.cpp        # Implementation of Pac-Man character
├── pacman.h          # Declaration of Pac-Man class
├── termfuncs.cpp     # Terminal control functions (e.g., cursor movement)
├── termfuncs.h       # Declaration of terminal functions
├── Makefile          # Build instructions
└── README.md         # Project description and setup instructions
```

---

##  Breadth-wise Understanding

###  Game Description

Terminal-Pacman replicates the classic Pac-Man gameplay within a terminal environment. Players navigate Pac-Man through a maze, collecting dots while avoiding ghosts. The game employs ASCII characters for visual representation and standard keyboard inputs for controls.

###  Technologies Used

- **Language:** C++
- **Input Handling:** Standard input (keyboard)
- **Build System:** Makefile

### Project Structure

The project is organized into multiple C++ source and header files, each handling specific aspects of the game:

- **main.cpp**: Entry point of the application; initializes the game and starts the main loop.
- **game.cpp / game.h**: Contains the core game logic, including the game loop, state management, and interactions between entities.
- **pacman.cpp / pacman.h**: Defines the Pac-Man character, including movement logic and state.
- **ghost.cpp / ghost.h**: Implements ghost behaviors and movement patterns.
- **dot.cpp / dot.h**: Manages collectible dots within the game.
- **boulder.cpp / boulder.h**: Introduces obstacles that Pac-Man must navigate around.
- **termfuncs.cpp / termfuncs.h**: Handles terminal-specific functions such as cursor movement and screen clearing.
- **constants.h**: Stores game-wide constants, such as symbols used for rendering and game dimensions.
- **Makefile**: Provides build instructions for compiling the project.
---

##  Depth-wise Analysis

### 1.  Approaches Taken

- **Object-Oriented Design:** Each game entity (Pac-Man, ghosts, dots, boulders) is encapsulated within its own class, promoting modularity and ease of maintenance.
- **Game Loop:** Implements a continuous loop that updates game state, processes user input, and renders the game frame-by-frame.

### 2. 🧱 Data Structures Used

- **Classes:** Define entities like Pac-Man, ghosts, dots, and boulders.
- **Arrays:** Represent the game maze and track positions of entities.
- **Constants:** Stored in `constants.h` to manage game configurations like maze size and symbols.

### 3. Game Mechanics and Logic

#### Movement and Input Handling
- User input is captured to control Pac-Man's movement using standard input methods.
- The game loop processes input, updates entity positions, and renders the game state accordingly.

#### Collision Detection
- The game checks for collisions between Pac-Man and other entities (dots, ghosts, boulders) to determine outcomes such as point collection or game over conditions.

#### Ghost AI Behavior
- Ghosts exhibit basic AI behaviors, potentially including random movement or simple chase algorithms.
- The AI lacks advanced pathfinding techniques, resulting in predictable ghost patterns.

#### Rendering
- The game utilizes ASCII characters to represent the maze, Pac-Man, ghosts, dots, and boulders.
- Terminal control sequences manage cursor positioning and screen updates to create a dynamic gameplay experience.


### 4. Tradeoffs Made

- **Terminal-Based Rendering:** While offering simplicity and nostalgia, it limits graphical capabilities compared to GUI-based implementations.
- **Simplified AI:** Ghost behaviors are likely based on basic algorithms, lacking advanced pathfinding techniques like A*.
- **Platform Dependency:** Terminal control sequences may behave differently across operating systems, potentially affecting portability.

---

## Contribution

- **1. Overlap** Noticed that ghosts sometimes overlap with Pac-Man without triggering a game-over, indicating a potential collision detection bug.
- **Fix:** Suggest enhancing the collision detection logic to accurately register overlaps between Pac-Man and ghosts.
- **2. No UI** There is no user interface made for this project and you have to start by giving command everytime you lose. There is no place to store scores .
---
