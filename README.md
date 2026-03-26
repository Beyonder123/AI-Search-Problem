<div align="justify">

# 🚗 Rush Hour Puzzle Solver

An intelligent **Rush Hour** puzzle game implementation featuring AI search algorithms and an intuitive graphical interface built with Pygame. This project demonstrates various artificial intelligence search strategies to solve the classic sliding puzzle game where the goal is to move a red car (marked as 'X') out of a traffic jam.

## 📖 Table of Contents

- [🎯 Overview](#-overview)
- [✨ Features](#-features)
- [🏗️ Project Structure](#️-project-structure)
- [🚀 Usage](#-usage)
- [🧠 Algorithms](#-algorithms)
- [🗺️ Map Format](#️-map-format)
- [⚙️ Configuration](#️-configuration)
- [🎮 Game Controls](#-game-controls)
- [📊 Performance Metrics](#-performance-metrics)

## 🎯 Overview

The **Rush Hour Puzzle Solver** is an educational AI project that implements and compares different search algorithms to solve Rush Hour puzzles. The game features:

- **Interactive GUI**: Built with Pygame for smooth user experience
- **Multiple AI Algorithms**: BFS, DFS, UCS, and A\* search implementations
- **Performance Analysis**: Real-time statistics including execution time, memory usage, and nodes expanded
- **Customizable Maps**: Support for multiple predefined maps and random generation
- **Educational Focus**: Perfect for learning AI search algorithms and their performance characteristics

## ✨ Features

### 🎮 Game Features

- **Intuitive Graphical Interface**: Clean, modern UI built with Pygame
- **Multiple Puzzle Maps**: 10+ predefined maps with varying difficulty levels
- **Random Map Generation**: Procedurally generated puzzles for endless gameplay
- **Interactive Controls**: Mouse and keyboard support for manual play
- **Visual Solution Playback**: Step-by-step animation of AI-generated solutions

### 🧠 AI Features

- **Four Search Algorithms**: BFS, DFS, UCS, and A\* implementations
- **Real-time Performance Metrics**:
  - Execution time measurement
  - Memory usage tracking
  - Number of expanded nodes
  - Solution path length
- **Algorithm Comparison**: Side-by-side performance analysis
- **Optimized Implementations**: Efficient state representation and search strategies

### 🎨 Interface Features

- **Scene Management**: Home screen, game screen, and help screen
- **Dropdown Menus**: Easy algorithm and map selection
- **Statistics Display**: Real-time performance data visualization
- **Responsive Design**: Adapts to different screen sizes
- **Visual Feedback**: Clear indication of moves and solutions

## 🏗️ Project Structure

```
AI-Search-Problem/
├── 📄 README.md              # Project documentation
├── 📄 LICENSE                # MIT License
├── 📄 requirements.txt       # Python dependencies
├── 🗂️ src/                   # Source code directory
│   ├── 📄 main.py            # Main application entry point
│   ├── 🗂️ assets/            # Game assets (images, sounds)
│   │   └── 🖼️ logo.png       # Game logo
│   ├── 🗂️ config/            # Configuration files
│   │   ├── 📄 __init__.py    # Package initialization
│   │   ├── 📄 config.json    # Game configuration settings
│   │   └── 📄 settings.py    # Settings loader
│   ├── 🗂️ core/              # Core game logic
│   │   ├── 📄 __init__.py    # Package initialization
│   │   ├── 📄 board.py       # Game board implementation
│   │   ├── 📄 map_loader.py  # Map loading utilities
│   │   └── 📄 vehicle.py     # Vehicle class definition
│   ├── 🗂️ entities/          # UI entities
│   │   ├── 📄 __init__.py    # Package initialization
│   │   ├── 📄 button.py      # Button UI component
│   │   └── 📄 dropdown.py    # Dropdown UI component
│   ├── 🗂️ maps/              # Puzzle map definitions
│   │   ├── 📄 map1.json      # Beginner level map
│   │   ├── 📄 map2.json      # Easy level map
│   │   ├── 📄 map3.json      # Medium level map
│   │   ├── 📄 map4.json      # Hard level map
│   │   ├── 📄 map5.json      # Expert level map
│   │   └── 📄 ...            # Additional maps (6-10)
│   ├── 🗂️ rushhour/          # Game state management
│   │   └── 📄 state.py       # Game state representation
│   ├── 🗂️ scenes/            # Game scenes
│   │   ├── 📄 __init__.py    # Package initialization
│   │   ├── 📄 home.py        # Main menu screen
│   │   ├── 📄 playing.py     # Game playing screen
│   │   └── 📄 help.py        # Help/instructions screen
│   ├── 🗂️ solvers/           # AI search algorithms
│   │   ├── 📄 __init__.py    # Package initialization
│   │   ├── 📄 base_solver.py # Base solver class
│   │   ├── 📄 bfs_solver.py  # Breadth-First Search
│   │   ├── 📄 dfs_solver.py  # Depth-First Search
│   │   ├── 📄 ucs_solver.py  # Uniform Cost Search
│   │   └── 📄 astar_solver.py# A* Search with heuristics
│   └── 🗂️ utils/             # Utility functions
│       ├── 📄 __init__.py    # Package initialization
│       └── 📄 helper.py      # Helper functions
└── 🗂️ tests/                 # Test files
    └── 📄 test_map.py        # Map loading tests
```

### Core Dependencies

- **pygame (2.5.2)**: Game development framework
- **numpy**: Numerical computations
- **Additional packages**: See `requirements.txt` for complete list

## 🚀 Usage

### Running the Game

1. **Navigate to the project directory**

   ```bash
   cd AI-Search-Problem
   ```

2. **Start the game**

   ```bash
   python src/main.py
   ```

3. **Game Flow**
   - Main menu appears with options to play, view help, or quit
   - Select "Play" to enter the game screen
   - Choose a map from the dropdown menu (1-10 or Random)
   - Select an AI algorithm (BFS, DFS, UCS, or A\*)
   - Click "Solve" to watch the AI solve the puzzle
   - View performance statistics in real-time

### Manual Play Mode

- Click and drag vehicles to move them
- Only valid moves are allowed (no collisions)
- Try to move the red car (X) to the exit on the right side

### AI Solver Mode

- Select your preferred algorithm
- Click "Solve" to start automatic solving
- Watch the solution animation
- Compare algorithm performance metrics

## 🧠 Algorithms

### 1. **Breadth-First Search (BFS)**

- **Strategy**: Explores all nodes at current depth before going deeper
- **Completeness**: Complete (finds solution if one exists)
- **Optimality**: Optimal for unweighted graphs
- **Time Complexity**: O(b^d)
- **Space Complexity**: O(b^d)
- **Best for**: Finding shortest solution path

### 2. **Depth-First Search (DFS)**

- **Strategy**: Explores as far as possible before backtracking
- **Completeness**: Complete in finite spaces
- **Optimality**: Not optimal
- **Time Complexity**: O(b^m)
- **Space Complexity**: O(bm)
- **Best for**: Memory-constrained environments

### 3. **Uniform Cost Search (UCS)**

- **Strategy**: Expands node with lowest path cost first
- **Completeness**: Complete
- **Optimality**: Optimal
- **Time Complexity**: O(b^(C\*/ε))
- **Space Complexity**: O(b^(C\*/ε))
- **Best for**: Weighted graphs with varying costs

### 4. **A\* Search**

- **Strategy**: Uses heuristic function to guide search
- **Completeness**: Complete
- **Optimality**: Optimal with admissible heuristic
- **Time Complexity**: O(b^d)
- **Space Complexity**: O(b^d)
- **Best for**: Optimal solutions with good heuristics
- **Heuristic**: Manhattan distance to goal position

## 🗺️ Map Format

Maps are defined in JSON format with the following structure:

```json
{
  "size": [6, 6], // Board dimensions [rows, cols]
  "vehicles": [
    // Array of vehicles
    {
      "name": "X", // Vehicle identifier (X = main car)
      "row": 2, // Starting row position
      "col": 0, // Starting column position
      "length": 2, // Vehicle length
      "orientation": "H" // H = Horizontal, V = Vertical
    },
    {
      "name": "A", // Other vehicles
      "row": 0,
      "col": 3,
      "length": 2,
      "orientation": "H"
    }
    // ... more vehicles
  ]
}
```

### Creating Custom Maps

1. Follow the JSON structure above
2. Ensure no vehicle overlaps
3. Place the main car (X) that needs to reach the exit
4. Save as `mapN.json` in the `src/maps/` directory

## ⚙️ Configuration

Game settings are stored in `src/config/config.json`:

```json
{
  "TITLE": "Rush Hour Game - Introduction to AI",
  "WINDOW_SIZE": [900, 600],
  "BG_COLOR": [30, 30, 30],
  "SCENES": {
    "MENU": "menu",
    "PLAY": "play",
    "HELP": "help",
    "QUIT": "quit"
  },
  "MAPS": ["1", "2", "3", "4", "5", "Random"],
  "ALGORITHMS": ["BFS", "DFS", "UCS", "A*"],
  "CELL_SIZE": 60,
  "MARGIN": 20,
  "FPS": 60,
  "TIME_LIMIT": 30
}
```

### Customizable Settings

- **Window size**: Adjust game window dimensions
- **Colors**: Modify background and UI colors
- **Cell size**: Change grid cell dimensions
- **FPS**: Set frame rate for smooth animation
- **Time limit**: Set maximum solving time

## 🎮 Game Controls

### Menu Navigation

- **Mouse**: Click buttons and dropdown menus
- **ESC**: Return to main menu or quit

### Game Screen

- **Mouse**:
  - Click and drag vehicles to move
  - Click dropdowns to select maps/algorithms
  - Click "Solve" button to start AI solving
- **Keyboard**:
  - **ESC**: Return to main menu
  - **R**: Reset current puzzle
  - **Space**: Pause/resume solution animation

### Help Screen

- **Mouse**: Click "Back" to return to menu
- **ESC**: Return to main menu

## 📊 Performance Metrics

The game displays real-time performance statistics:

### Timing Metrics

- **Execution Time**: Total time for algorithm to find solution
- **Solution Length**: Number of moves in optimal path
- **Search Efficiency**: Nodes expanded vs. total possible states

### Memory Metrics

- **Memory Usage**: Peak memory consumption during search
- **Nodes Expanded**: Total number of states explored
- **Nodes in Memory**: Maximum nodes stored simultaneously

### Comparison Features

- Side-by-side algorithm comparison
- Historical performance tracking
- Export results to CSV (planned feature)

</div>
