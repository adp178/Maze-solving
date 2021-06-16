# Maze-solving

Exploration of various search algorithms (DFS, BSF, A*) in the application of path planning using the environment of a maze on fire.
Implemented local search algorithms of genetic search and hill-climbing in order to discover hard to solve mazes
Simulated a system in which the agent tries to solve the problem in a dynamic environment.

# Part - 1: Environments and Algorithms
A maze is be a square grid of cells / locations, where each cell is either empty or occupied. An agent wishes to travel from the upper left corner to the lower right corner, along the shortest path possible. The agent can only move from empty cells to neighboring empty cells in the up/down direction, or left/right - each cell has potentially four neighbors. Search for a path from corner to corner, using each of the following algorithms:

Depth-First Search
Breadth-First Search
A_star: where the heuristic is to estimate the distance remaining via the Euclidean Distance
A_star: where the heuristic is to estimate the distance remaining via the Manhattan Distance

For any specifed map, applying one of these search algorithms either returns failure, or a path from start to goal in terms of a list of cells taken.

# Part - 2: Analysis and Comparisons

Having coded five path-generating algorithms, we want to analyze and compare their performance. Answered the following questions:

* Find a map size (dim) that is large enough to produce maps that require some work to solve, but small enough that you can run each algorithm multiple times for a range of possible p values. How did you pick a dim?
* For p = 0.2, generate a solvable map, and show the paths returned for each algorithm. Do the results make sense?
Given dim, how does maze-solvability depend on p? For a range of p values, estimate the probability that a maze will be solvable by generating multiple mazes and checking them for solvability. What is the best algorithm to use here? Plot density vs solvability, and try to identify as accurately as you can the threshold p0 where for p < p0, most mazes are solvable, but p > p0, most mazes are not solvable.
* For p in [0; p0] as above, estimate the average or expected length of the shortest path from start to goal. You may discard unsolvable maps. Plot density vs expected shortest path length. What algorithm is most useful here?
* Is one heuristic uniformly better than the other for running A_star? How can they be compared? Plot the relevant data and justify your conclusions.
* Do these algorithms behave as they should?
* For DFS, can you improve the performance of the algorithm by choosing what order to load the neighboring rooms into the fringe? What neighbors are `worth' looking at before others? Be thorough and justify yourself.
* On the same map, are there ever nodes that BD-DFS expands that A_star doesn't? Why or why not? Give an example, and justify.
* How does the threshold probability p0 depend on dim?

# Part - 3: Generating Hard Mazes
In this part, we have generated hard to solve mazes. Three possible ways you might quantify hard are: a) how long the shortest path is, b) the total number of nodes expanded during solving, and c) the maximum size of the fringe at any point in solving.

We designed and implemented local search algorithms of

* Genetic Algorithm
* Hill Climbing to discover hard to solve mazes
