# 🕹️ ARCADE — Puzzle Games

A collection of four classic puzzle games built in a single self-contained HTML file. No frameworks, no dependencies, no server required — just open `index.html` in any browser and play.

**Live demo:** `https://yourusername.github.io/arcade-games`

---

## 🎮 Games

### 🧩 N-Puzzle *(Sliding Tiles)*
The classic 8-puzzle and 15-puzzle. Slide numbered tiles into the correct order.

- **A\* Search engine** computes the optimal solution from any board state
- **Live efficiency coach** — tracks your moves vs. the mathematical optimum after every step
- **Hint system** — highlights the single best tile to move next
- **Auto-Solve** — watches A\* animate the optimal solution step by step
- **Undo / Reset** — step back through your move history
- **Skill issue voice roast** — if you take more than 2× the optimal moves, a deadpan voice lets you know
- **Give-up taunt** — press Auto-Solve mid-game and the coach has something to say
- Board sizes: **3×3** (8-Puzzle) and **4×4** (15-Puzzle)
- Difficulties: Easy, Medium, Hard, Expert

---

### ♛ N-Queens *(Constraint Satisfaction)*
Place N queens on an N×N chessboard so no two queens attack each other — no shared row, column, or diagonal.

- **Real-time conflict detection** — attacking queens turn red instantly
- **Attack line visualisation** — threatened squares are tinted
- **Safe square hint** — highlights a safe cell in the next empty row
- **Backtracking solver** — finds a valid solution instantly using recursive backtracking
- **Live coach** — tracks placed count, conflicts, and gives contextual feedback
- Board sizes: **4×4, 6×6, 8×8, 10×10, 12×12**

---

### 🔢 Sudoku *(Constraint Propagation)*
Fill a 9×9 grid so every row, column, and 3×3 box contains the digits 1–9 exactly once.

- **Procedural puzzle generator** — creates a new unique puzzle every game using backtracking
- **Completion celebrations** — row, column, and 3×3 box completions each trigger a unique flash animation and sound
- **Conflict highlighting** — wrong numbers shown in red
- **Row/col/box highlighting** — click any cell to illuminate its entire group
- **Hint system** — reveals the correct number for any selected cell
- **Backtracking auto-solver** — fills the entire board instantly
- **Keyboard & numpad input** — type 1–9 or use the on-screen pad; arrow keys navigate between cells
- **Undo stack** — step back any number of moves
- Difficulties: Easy (~35 clues), Medium (~28 clues), Hard (~22 clues)

---

### 🌀 Maze Pathfinder *(Graph Search Algorithms)*
Navigate a procedurally generated maze from start to end — or watch three different algorithms solve it and compare their behaviour side by side.

- **Three solvers with animated frontiers:**
  - ⭐ **A\*** — uses Manhattan distance heuristic, explores the fewest cells, always finds the optimal path
  - 🌿 **DFS** (Depth-First Search) — dives deep down one corridor at a time, finds *a* path but rarely the shortest
  - 🌊 **BFS** (Breadth-First Search) — sweeps outward in concentric rings, always finds the shortest path
- **Side-by-side comparison panel** — run all three algorithms and compare path length vs. cells explored
- **Player mode** — navigate with arrow keys or WASD; win screen compares your route to A\* optimal
- **Procedural maze generation** — recursive backtracker DFS creates a perfect maze (every cell reachable, no loops)
- Maze sizes: **11×11** (Small), **21×21** (Medium), **31×31** (Large)

---

## 🧠 Algorithms Used

| Algorithm | Used In | Purpose |
|---|---|---|
| A\* Search | N-Puzzle, Maze | Optimal pathfinding with Manhattan + Linear Conflict heuristic |
| Recursive Backtracking | N-Queens solver, Sudoku generator/solver, Maze generator | Exhaustive search with pruning |
| Min-Heap (Priority Queue) | A\* in N-Puzzle and Maze | Efficient O(log n) node expansion ordering |
| BFS | Maze | Guaranteed shortest path, unweighted graph |
| DFS | Maze, Maze generation | Deep exploration, complete maze carving |
| Constraint Propagation | Sudoku | Conflict detection across rows, columns, boxes |
| Linear Conflict Heuristic | N-Puzzle A\* | Tighter admissible heuristic than Manhattan alone |

---

## ✨ Features

- **Zero dependencies** — pure HTML, CSS, and vanilla JavaScript
- **Single file** — everything is in `index.html`, no build step, no npm
- **Web Audio API sounds** — synthesised click sounds, completion arpeggios, win chimes — no audio files
- **Web Speech API** — voice taunts in N-Puzzle when you play inefficiently
- **Confetti** — canvas-free CSS confetti on every win
- **Responsive** — works on desktop and mobile
- **Dark theme** throughout with a consistent design system

---

## 🚀 Getting Started

### Play locally
```bash
# Clone the repo
git clone https://github.com/yourusername/arcade-games.git

# Open the file — no server needed
open index.html
# or just double-click it in your file explorer
```

### Deploy to GitHub Pages
1. Fork or clone this repo
2. Go to **Settings → Pages**
3. Set source to **Deploy from branch → main → / (root)**
4. Your game will be live at `https://yourusername.github.io/arcade-games`

---

## 📁 Project Structure

```
arcade-games/
├── index.html   ← entire game (HTML + CSS + JS, self-contained)
└── README.md
```

That's it. One file.

---

## 🛠️ How It Was Built

| Layer | Technology |
|---|---|
| Layout | CSS Grid, Flexbox, CSS custom properties |
| Fonts | Google Fonts — Playfair Display, DM Mono, DM Sans |
| Animations | CSS keyframes + Web Animations API |
| Sound | Web Audio API (synthesised, no files) |
| Voice | Web Speech API |
| Canvas | HTML5 Canvas (maze renderer) |
| Logic | Vanilla ES6+ JavaScript |

---

## 📜 License

MIT — do whatever you want with it.
