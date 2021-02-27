# Maze-SDL
Maze generator and solver using SDL 2.0


This program can generate, and solve automaticly a random maze with an entry and an exit already fixed.
The generation of the Maze is based on Kruskal's maze generator algorithm.
Kruskal’s algorithm is a method for producing a minimal spanning tree from a weighted graph.
This algorithm is a randomized version of Kruskal's algorithm:
-Create a list of all walls, and create a set for each cell, each containing just that one cell.

-For each wall, in some random order:

--If the cells divided by this wall belong to distinct sets:

---Remove the current wall.

---Join the sets of the formerly divided cells.

There are several data structures that can be used to model the sets of cells, I choosed the disjoint-set data structure to perform each union and find operation on two sets in nearly constant amortized time, so the running time of this algorithm is essentially proportional to the number of walls available to the maze.

For solving the Maze I choosed the Depth-first-search (DFS) method.
The algorithm starts at the root node (The start is from the exit), give it number 1, explores as far as possible with numbers along each branch before backtracking.
The algorithm ends when each cell is visited.

Last step in this program is exploring the maze from the entry by following the lowest number of adjacents cells.

# Test
Here is a test in the form of an animated gif:

![Test](https://user-images.githubusercontent.com/79026302/109402790-02be2c80-7959-11eb-8b1e-f96f5ffc0a7d.gif)
