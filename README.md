
# RISC-V CPU Implementation with Path Planning Algorithm

This project involves the implementation of a RISC-V CPU in Verilog to execute a path planning algorithm. The CPU is designed to read start and end points from data memory, perform computations for path planning, and then write the node points connecting the start and end points back into the data memory.

## Overview

The primary goal of this project is to integrate a RISC-V CPU with path planning algorithms, enabling the computation of paths between given points within a hardware environment. The CPU's design includes modules for instruction execution, data memory management, and control flow, facilitating the execution of different path planning algorithms.

## Path Planning Algorithms

### Dijkstra's Algorithm

**Description:**
Dijkstra's algorithm is a graph search algorithm used to find the shortest path from a single source vertex to all other vertices in a weighted graph. It works well for graphs with non-negative edge weights.

**Algorithm Steps:**
1. Initialize distances from the source vertex to all other vertices as infinity and the distance to the source vertex as 0.
2. Create a priority queue or set to store vertices and their tentative distances.
3. While the priority queue is not empty:
   - Extract the vertex with the minimum tentative distance.
   - For each neighboring vertex:
     - Update the distance if a shorter path is found.
     - Update the priority queue with the updated distances.
4. The shortest path to all vertices from the source vertex is determined.

### A* Algorithm

**Description:**
A* (A-star) algorithm is a heuristic-based search algorithm used for finding the shortest path between two nodes in a graph. It uses a combination of the actual cost from the start node and an estimated cost to the target node.

**Algorithm Steps:**
1. Initialize the start node and the goal node.
2. Create open and closed sets to keep track of visited nodes and potential nodes to visit.
3. Initialize the open set with the start node and set its estimated cost to the goal node.
4. While the open set is not empty:
   - Extract the node with the lowest estimated cost.
   - If the current node is the goal node, the path is found.
   - Otherwise, expand the node and update costs for neighboring nodes.
5. The shortest path from the start node to the goal node is determined.

### Flood-Fill Algorithm

**Description:**
The flood-fill algorithm is a technique used to determine connected regions in a grid and fill them with a specific color or value. It's often used in image processing and maze-solving scenarios.

**Algorithm Steps:**
1. Choose a starting point in the grid.
2. Define the conditions for "filling" (e.g., neighboring cells with the same value).
3. Recursively or iteratively visit neighboring cells and mark or change their values based on the conditions.
4. Continue until all connected cells meeting the conditions are processed.

## Implementation Details

The RISC-V CPU design in Verilog includes modules for instruction fetch, decode, execution, and interfacing with data memory. The path planning algorithms are implemented as software routines that the CPU executes.

## How to Use

### Pre-requisites
- Verilog simulator or FPGA development environment.
- RISC-V toolchain for compiling and running the Verilog code.

### Steps
1. **Simulation/Implementation**: Load the RISC-V CPU Verilog code into your simulation environment or FPGA.
2. **Compile and Load Path Planning Algorithm**: Compile and load the path planning algorithm into the CPU's memory.
3. **Run Simulation/Execute on FPGA**: Start the simulation or execute the design on the FPGA.
4. **Monitor Data Memory**: Observe the data memory to inspect the start, end, and computed node points forming the path.

## Acknowledgments

This project draws inspiration from the need to integrate computational algorithms into hardware implementations for path planning and navigation.

