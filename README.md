# # Water Jug Problem Solver (C++)

## Overview
This C++ program solves the **Water Jug Problem** — a classic puzzle where you must measure an exact volume of water using two jugs of given capacities.  
It uses **simulation of jug operations** to reach the target amount, trying both approaches:
1. Starting with filling Jug X first.
2. Starting with filling Jug Y first.

The program prints the step-by-step sequence of actions for each method.

---

## How It Works
- **Two jugs** with capacities `X` and `Y` are given.
- The **goal volume** is entered by the user.
- If the goal is **not achievable** (based on the greatest common divisor rule), the program terminates early.
- Two solving methods are tried:
  - **X-first strategy**
  - **Y-first strategy**
- Each method performs:
  - Filling a jug completely
  - Emptying a jug completely
  - Pouring water from one jug to the other until one is empty or the other is full
- Stops when the goal volume is reached in either jug.

---

### Example Run

Enter capacity of jug X: 3
Enter capacity of jug Y: 5
Enter goal volume: 4

--- Solving starting with X ---
Step 0: (0, 0)
Step 1 - Fill X: (3, 0)
Step 2 - Pour X->Y: (0, 3)
Step 3 - Fill X: (3, 3)
Step 4 - Pour X->Y: (1, 5)
Step 5 - Empty Y: (1, 0)
Step 6 - Pour X->Y: (0, 1)
Step 7 - Fill X: (3, 1)
Step 8 - Pour X->Y: (0, 4)
Goal 4 reached in 8 steps.

--- Solving starting with Y ---
Step 0: (0, 0)
Step 1 - Fill Y: (0, 5)
Step 2 - Pour Y->X: (3, 2)
Step 3 - Empty X: (0, 2)
Step 4 - Pour Y->X: (2, 0)
Step 5 - Fill Y: (2, 5)
Step 6 - Pour Y->X: (3, 4)
Goal 4 reached in 6 steps.

### Use Case
This program can be used for:

Solving classic algorithmic puzzles in AI and operations research
Demonstrating the GCD-based feasibility rule for water jug problems
Teaching basic state simulation and search techniques in problem-solving

## Compilation & Execution
```bash
g++ water_jug.cpp -o water_jug
./water_jug

