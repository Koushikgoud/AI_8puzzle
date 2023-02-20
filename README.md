# AI_8puzzle
This is a simple AI agent which solves the 8-puzzle game given the initial state and goal state

In this, I tried to implement the A* algorithm using Manhattan distance as a heuristic. (Actual state -> goal state) 

Step-1: Define the initial state and goal state of the 8-puzzle problem.

Step-2: Define the Manhattan distance heuristic function.
A Manhattan heuristic function is used in pathfinding problems. It is a distance metric that measures Manhattan distance (horizontal and vertical distance) in a grid-like structure just like an 8-puzzle. This heuristic function returns the total Manhattan distance h(n) i.e., it measures the number of steps required for a tile to reach the correct position as in the goal state from the current position in the current state. This distance is checked for all the misplaced tiles and added to return the overall Manhattan distance of a particular state.

Step-3: Create a priority queue data structure to store the states.
In our case, we are using min-heap data structure which is implemented by using heapq python library.
  1. Add the initial state to the priority queue with a priority of 0. 
  2. While the priority queue is not empty, do the following:
    a. Pop the state with the lowest priority from the priority queue.
    b. If the popped state is the goal state, return the solution.
    c. Generate all the valid successor states of the popped state.
    d. For each successor state, calculate the priority using the formula f(n) = g(n) + h(n),
      where g(n) is the cost to reach the state and h(n) is the Manhattan distance heuristic. e. Add the successor state to the priority queue with its           priority.
  3. If the priority queue becomes empty and a solution has not been found, return failure.
