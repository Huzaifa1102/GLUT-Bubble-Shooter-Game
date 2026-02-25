# Word Shooter Game

An engaging, fast-paced C++ arcade game that combines typing proficiency with classic shooter mechanics. Built using the **CImg** library, the game challenges players to eliminate falling words by typing them accurately before they reach the bottom of the screen.

---

## Features

* **Dynamic Word Generation:** Utilizes a comprehensive dictionary (`words_alpha.txt`) to generate a diverse range of targets.
* **Real-time Rendering:** High-performance 2D graphics and fluid animations powered by a custom engine and the **CImg** library.
* **Interactive Mechanics:** Features smooth keyboard input processing for rapid-fire typing and game state management.
* **Audio Immersion:** Integrated background music and sound effects for an enhanced arcade experience.
* **Game Board Logic:** Robust collision detection and "out-of-bounds" logic handled by a dedicated `Board` class.

---

## Technical Architecture

The project follows a modular C++ design to separate core game logic from utility functions and graphical rendering.

### Core Components

| Component | Responsibility |
| --- | --- |
| **`wordshooter.cpp`** | Main entry point, game loop, and typing logic. |
| **`Board.cpp / .h`** | Manages the game grid, boundaries, and object placement. |
| **`CImg.h`** | Provides the graphical framework for windowing and pixel manipulation. |
| **`util.cpp / .h`** | Contains drawing primitives (rectangles, text) and color constants. |
| **`words_alpha.txt`** | The external dictionary source for game vocabulary. |

---

## Logic & Algorithms

### 1. Dictionary Parsing

The system loads thousands of words into memory at startup, allowing for $O(1)$ random selection of new targets during gameplay.

### 2. Coordinate Mapping

Utilizes the `Board` class to translate abstract game coordinates into screen pixels, ensuring consistent rendering across different display sizes.

### 3. Build System

A structured `Makefile` manages the compilation of multiple source files into an optimized binary, handling dependencies like X11 and arithmetic libraries.

---

## Getting Started

### Prerequisites

* A C++ compiler (GCC/G++).
* X11 development libraries (can be installed via `install-libraries.sh`).

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

Word Shooter is a C++ arcade game that blends typing skills with shooter mechanics. Using the CImg library, it features real-time 2D rendering and dynamic word generation from a 370k-word dictionary. The project includes modular board logic, custom drawing utilities, and automated build scripts for a seamless high-speed gaming experience.

---

## Contributors

* **Huzaifa Mudassar**
* **i24-0050**
