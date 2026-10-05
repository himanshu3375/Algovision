# AlgoVision

A visual learning platform for Algorithms and Data Structures. Built as a single, self-contained HTML file — no build step, no server, no install.

**[Live app](https://claude.ai/artifact/WezqFZ5v6qDo5CAguB3ih2)** · `algovision.html` (open directly in any browser)

## What it does

AlgoVision helps you learn DSA by watching algorithms execute step by step, instead of only reading about them.

- **Visualizer** — run real algorithms (not scripted animations) on a bar chart or a graph, with play, pause, step-forward, reset, speed control, and live comparison/swap counts.
- **Algorithms catalog** — searchable, filterable cards (by category and difficulty) for all 10 implemented algorithms.
- **Data Structures** — interactive Array (insert, delete, search, update) and Linked List (insert at head/tail, delete, search) playgrounds, each with a live "why this operation" explanation panel.
- **Learn** — a W3Schools-style tutorial page: sidebar topic menu, explanation, real-world example, pseudocode, complexity table, pros/cons, and a "Try it Yourself" link into the live visualizer.
- **Quiz** — 500 questions across 50 sets of 10. Take a random set or pick a specific one; your best score is saved.
- **Accounts** — local demo login/signup (stored in the browser only, not a real backend). Progress is tracked per account.
- **Dashboard** — algorithms explored, best quiz score, and last-visualized algorithm, shown on the home page.
- **Dark / light mode**, saved across visits.

## Algorithms implemented

| Category  | Algorithms |
|-----------|------------|
| Sorting   | Bubble Sort, Selection Sort, Insertion Sort, Merge Sort, Quick Sort |
| Searching | Linear Search, Binary Search |
| Graph     | Breadth-First Search, Depth-First Search, Dijkstra's Algorithm |

Graph algorithms run on a fixed 9-node weighted graph rendered as SVG, with a selectable start node.

## Tech stack

- HTML5, CSS3, vanilla JavaScript (ES6+) — no frameworks, no build tools, no dependencies
- `localStorage` for theme preference, accounts, and per-account progress/quiz scores
- No backend — everything runs client-side in one file

## Running it

Just open `algovision.html` in a browser. There's nothing to install or configure.

## Project structure

Everything lives in one file, organized internally by section:

```
algovision.html
├── <style>   — CSS (design tokens, layout, component styles)
├── <body>    — nav, home, algorithms catalog, data structures, learn, visualizer, quiz, about
└── <script>  — nav routing, theme, auth, progress tracking,
                sorting/searching step generators, graph (BFS/DFS/Dijkstra) step generators,
                array/linked-list operations, 500-question quiz bank, rendering
```

## Known limitations / roadmap

Not yet built:
- Stack, Queue, and Binary Search Tree playgrounds
- Step-by-step "Learning Mode" with next/previous controls
- Dynamic Programming algorithms
- A real backend (accounts and progress are local to the browser only)

## Credits

Built iteratively with Claude. Color palette, "Try it Yourself" styling, and the Array/Linked List explanation-panel pattern were inspired by W3Schools' tutorial layout.
