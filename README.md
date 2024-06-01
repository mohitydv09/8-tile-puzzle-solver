# 8 Sliding Tile Puzzle Solver

This project implements the following path planning algorithms to solve the 8-sliding tile puzzle problem:
- Breadth-First Search (BFS),
- Iterative Deepening Depth-First Search (IDDFS), and
- A* search with two heuristics: number of wrong tiles and Manhattan distance.

## Usage

To run the solver, use the following command:
```
python3 sliding_puzzle.py <initial_state>
```
where `<initial_state>` is a string representing the initial state of the puzzle, with 0 representing the blank space. 
For example input like:

```sh
python sliding_puzzle.py 123864705
```
will output result like:
```
['D']
BFS took 0.00003004074096679688 seconds
['D']
IDDFS took 0.00005030632019042969 seconds
['D']
A* using num_wrong_tiles took 0.00004506111145019531 seconds
['D']
A* using manhattan_dist took 0.00004076957702636719 seconds
```
The resulting path is also prined by the code : `['D']`  for all the algorithms in the above example.

## Goal

This implementation solves for the below shown final goal:

<table>
  <tr>
    <td>1</td>
    <td>2</td>
    <td>3</td>
  </tr>
  <tr>
    <td>8</td>
    <td>.</td>
    <td>4</td>
  </tr>
  <tr>
    <td>7</td>
    <td>6</td>
    <td>5</td>
  </tr>
</table>

This can be modified when initializing the Problem class. Provide the desired end goal as:
```sh
problem_instance = Problem(intial_state, goal=<tuple_of_desired goal>
```
See Problem Class for more detail.

## Notes

- The code assumes the input is a valid 8-puzzle configuration and does not check for solvability.
- The initial and goal states are represented as tuples of integers.
