# 8-Puzzle Solver (A* Algorithm)

This project implements the **A* Search Algorithm** to solve the 8-puzzle problem. It compares three different heuristic functions to evaluate their efficiency in finding the optimal path from a start state to a goal state.

## 📋 Table of Contents
- [The Problem](#-the-problem)
- [Heuristics](#-heuristics)
- [A* Pseudocode](#-a-pseudocode)
- [Input Format](#-input-format)
- [Results Comparison](#-results-comparison)

## 🧩 The Problem
The 8-puzzle is a sliding puzzle that consists of a frame of numbered square tiles in random order with one tile missing. The object of the puzzle is to place the tiles in order by making sliding moves that use the empty space.

## 🧠 Heuristics

- **h1: Misplaced Tiles**  
  Counts the number of tiles that are not in their target position.
- **h2: Manhattan Distance ($P(n)$)**  
  Calculates the sum of the horizontal and vertical distances of each tile from its goal position.
- **h3: Nilsson's Sequence Score ($3S(n) + P(n)$)**  
  A more sophisticated heuristic that adds a penalty for tiles that are out of sequence along the perimeter of the grid.

## 🤖 A* Pseudocode
The algorithm uses an `OPEN` list (priority queue) and a `CLOSED` list to track states:
1. Put the start node `s` on `OPEN` and compute $f(s)$.
2. Remove the node `n` with the smallest $f$ from `OPEN` and put it on `CLOSED`.
3. If `n` is the goal, reconstruct the path.
4. Otherwise, expand `n` and process successors, updating path costs and parent pointers for rediscovered states.

## 📂 Input Format
The program reads from `astar_in.txt`. Blank tiles are represented by `*` or `0`.
```text
start
2 1 6
4 * 8
7 5 3
goal
1 2 3
8 * 4
7 6 5
```

## 📊 Results Comparison
For the provided sample input, all heuristics found an optimal solution of **18 moves**. However, the search effort varied significantly:

| Heuristic | Nodes Expanded ($E$) |
| :--- | :--- |
| Misplaced Tiles ($h_1$) | 1487 |
| Manhattan Distance ($h_2$) | 165 |
| Nilsson Sequence Score ($h_3$) | 45 |

Nilsson's Sequence Score proved to be the most efficient heuristic for pruning the search space.*italicized text*# 8-Puzzle Solver (A* Algorithm)

This project implements the **A* Search Algorithm** to solve the 8-puzzle problem. It compares three different heuristic functions to evaluate their efficiency in finding the optimal path from a start state to a goal state.

## 📋 Table of Contents
- [The Problem](#-the-problem)
- [Heuristics](#-heuristics)
- [A* Pseudocode](#-a-pseudocode)
- [Input Format](#-input-format)
- [Results Comparison](#-results-comparison)

## 🧩 The Problem
The 8-puzzle is a sliding puzzle that consists of a frame of numbered square tiles in random order with one tile missing. The object of the puzzle is to place the tiles in order by making sliding moves that use the empty space.

## 🧠 Heuristics

- **h1: Misplaced Tiles**  
  Counts the number of tiles that are not in their target position.
- **h2: Manhattan Distance ($P(n)$)**  
  Calculates the sum of the horizontal and vertical distances of each tile from its goal position.
- **h3: Nilsson's Sequence Score ($3S(n) + P(n)$)**  
  A more sophisticated heuristic that adds a penalty for tiles that are out of sequence along the perimeter of the grid.

## 🤖 A* Pseudocode
The algorithm uses an `OPEN` list (priority queue) and a `CLOSED` list to track states:
1. Put the start node `s` on `OPEN` and compute $f(s)$.
2. Remove the node `n` with the smallest $f$ from `OPEN` and put it on `CLOSED`.
3. If `n` is the goal, reconstruct the path.
4. Otherwise, expand `n` and process successors, updating path costs and parent pointers for rediscovered states.

## 📂 Input Format
The program reads from `astar_in.txt`. Blank tiles are represented by `*` or `0`.
```text
start
2 1 6
4 * 8
7 5 3
goal
1 2 3
8 * 4
7 6 5
```

## 📊 Results Comparison
For the provided sample input, all heuristics found an optimal solution of **18 moves**. However, the search effort varied significantly:

| Heuristic | Nodes Expanded ($E$) |
| :--- | :--- |
| Misplaced Tiles ($h_1$) | 1487 |
| Manhattan Distance ($h_2$) | 165 |
| Nilsson Sequence Score ($h_3$) | 45 |

Nilsson's Sequence Score proved to be the most efficient heuristic for pruning the search space.
