# Artificial Intelligence's 1st Programming Exercise
## The travelling salesman problem
This is my attempt at solving the first programming exercise of Artificial Intelligence's course (PCS3438) at the Polytechnic School of the University of São Paulo in 2018. In this exercise, we're supposed to solve the travelling salesman problem (TSP), which asks the following question: "Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city and returns to the origin city?" The TSP can be modelled as an undirected weighted graph, such that cities are the graph's vertices, paths are the graph's edges, and a path's distance is the edge's weight.

As with other NP-hard problems, the solutions can be computed by the following methods:
* Devising exact algorithms, which work reasonably fast only for small problem sizes.
* Devising "suboptimal" or heuristic algorithms, i.e., algorithms that deliver either seemingly or probably good solutions, but which could not be proved to be optimal.
* Finding special cases for the problem ("subproblems") for which either better or exact heuristics are possible.

## Solutions of the problem
### Exact solution
The most direct solution would be to try all permutations (ordered combinations) and see which one is cheapest (using brute force search). The running time for this approach lies within a polynomial factor of <img src="https://latex.codecogs.com/gif.latex?{\displaystyle&space;O(n!)}" title="{\displaystyle O(n!)}" />, the factorial of the number of cities, so this solution becomes impractical even for only 20 cities.

One of the earliest applications of dynamic programming is the Held–Karp algorithm that solves the problem in time <img src="https://latex.codecogs.com/gif.latex?{\displaystyle&space;O(n^{2}2^{n})}" title="{\displaystyle O(n^{2}2^{n})}" />.

Improving these time bounds seems to be difficult. Other approaches include:

* Various branch-and-bound algorithms, which can be used to process TSPs containing 40-60 cities.
* Progressive improvement algorithms which use techniques reminiscent of linear programming. Works well for up to 200 cities.
* Implementations of branch-and-bound and problem-specific cut generation (branch-and-cut); this is the method of choice for solving large instances.

### Heuristic and approximation algorithms
Various heuristics and approximation algorithms, which quickly yield good solutions have been devised. Modern methods can find solutions for extremely large problems (millions of cities) within a reasonable time which are with a high probability just 2–3% away from the optimal solution.

## References
[1] https://en.wikipedia.org/wiki/Travelling_salesman_problem
