# Autonomous Vacuum Cleaner

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626.svg?style=for-the-badge&logo=Jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-%23ffffff.svg?style=for-the-badge&logo=Matplotlib&logoColor=black)

A visual simulation of an autonomous vacuum cleaner navigating a room to clean multiple dirt piles while avoiding obstacles. The robot's pathfinding is powered by the **A* (A-Star) Search Algorithm** and optimized using a **Minimum Spanning Tree (MST)** heuristic to calculate the most efficient cleaning route.

## Core Concepts

A* is a popular and powerful graph traversal and pathfinding algorithm. It is highly regarded because it is both *complete* (it will always find a solution if one exists) and *optimal* (it will find the shortest possible path). 

A* works by evaluating nodes based on two factors:
1.  **g-cost:** The exact cost of the path from the starting point to the current node.
2.  **h-cost (Heuristic):** An estimated cost from the current node to the final goal.

The algorithm calculates the total cost, **f = g + h**, and prioritizes exploring paths with the lowest 'f' value.

### Heuristic
In computer science, a heuristic is a function that ranks alternatives in search algorithms at each branching step based on available information to decide which branch to follow. It is essentially an "educated guess." 
In pathfinding, a heuristic estimates the distance remaining to the goal. A good heuristic makes the A* algorithm extremely fast by guiding it directly toward the target, preventing it from wasting time exploring bad directions. For an algorithm to remain optimal, the heuristic must be *admissible*, meaning it never overestimates the actual cost to reach the goal.

### Minimum Spanning Tree (MST)
A Minimum Spanning Tree is a subset of the edges of a connected, edge-weighted graph that connects all the vertices together, without any cycles, and with the minimum possible total edge weight.

Because of the logic that the vacuum needs to clean *multiple* pieces of dirt, finding the shortest path becomes a variation of the Traveling Problem. A simple heuristic (like finding the distance to the single nearest dirt pile) is "short-sighted." Using Prim's Algorithm to generate an MST creates a mathematical "web" that connects the robot and all remaining dirt piles. 

## Real-World Applications
* **Robotics & Autonomous Vehicles** 
* **Video Game AI** 
* **Network Routing** 
* **Circuit Board Design**
