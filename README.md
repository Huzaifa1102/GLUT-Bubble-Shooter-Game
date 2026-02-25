# Word Shooter Game

An engaging, fast-paced C++ arcade game where players shoot colored bubbles containing letters to form words. Built using the **CImg** library, the game challenges players to accurately sequence their shots to match valid dictionary entries before the board fills up.

---

## Features

* **Letter-Bubble Mechanics:** Dynamic spawning of letter-filled bubbles that must be shot in order to form words.
* **Word Validation:** Real-time checking against a 370k-word dictionary (`words_alpha.txt`); when a valid word is formed, the bubbles pop and clear from the board.
* **Dynamic Rendering:** High-performance 2D graphics and fluid animations powered by a custom engine and the **CImg** library.
* **Game Board Logic:** Robust collision detection and "out-of-bounds" logic handled by a dedicated `Board` class.
* **Integrated Audio:** Background music and sound effects (e.g., `spinning-head-271171.mp3`) for an immersive arcade experience.

---

## Technical Architecture

The project follows a modular C++ design to separate core game logic from utility functions and graphical rendering.

### Core Components

| Component | Responsibility |
| --- | --- |
| **`wordshooter.cpp`** | Main entry point, game loop, and bubble-shooting logic. |
| **`Board.cpp / .h`** | Manages the game grid, boundaries, and bubble placement. |
| **`CImg.h`** | Provides the graphical framework for windowing and pixel manipulation. |
| **`util.cpp / .h`** | Contains drawing primitives (circles, text) and color constants. |
| **`words_alpha.txt`** | The external dictionary source used to validate popped word sequences. |

---

## Logic & Algorithms

### 1. Dictionary Parsing

The system loads thousands of words into memory at startup, allowing for $O(1)$ validation of letter sequences when bubbles are hit.

### 2. Collision & Physics

Utilizes the `Board` class to detect when a projectile hits a letter bubble and translates abstract game coordinates into screen pixels.

### 3. Build System

A structured `Makefile` manages the compilation of multiple source files into an optimized binary, handling dependencies like X11 and arithmetic libraries.

---

## Getting Started

### Prerequisites

* A C++ compiler (GCC/G++).
* X11 development libraries (installable via `install-libraries.sh`).

### Installation & Compilation

1. **Setup Environment:**
```bash
chmod +x install-libraries.sh
./install-libraries.sh

```


2. **Build Project:**
```bash
make

```



### Running the Game

```bash
./word-shooter

```

---

## Project Description (350 Characters)

Word Shooter is a C++ arcade game where players shoot letter-filled bubbles to form and pop words. Using the CImg library, it features real-time 2D rendering and word validation against a massive dictionary. The project includes modular board logic for collision detection, custom drawing utilities, and automated scripts for a fast-paced experience.

---

## Contributors

* **Huzaifa Mudassar**
* **i24-0050**
