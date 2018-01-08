# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?

A: If 2 digits can only appear in 2 boxes within the same unit, then they must appear in those 2 boxes since, 
according to the rules of sudoku, all the digits have to appear in the unit. This means 2 things:
- No other digit can appear in those 2 boxes.
- The 2 digits cannot appear in the other boxes of the unit.
Applying these constraints helps reducing the search space.

In `naked_twins()`, we considered that we were solving a regular sudoku problem (not a diagonal sudoku) and
looked for twins in each row, column and square.


# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?

A: For the diagonal sudoku problem, we use the same constraint propagation method as for regular sudokus ("elimitate" and "only choice") but apply them to 2 extra units (the 2 diagonals), on top of rows, columns and squares. This reduces the search space more aggressively.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.


### Data

The data consists of a text file of diagonal sudoku for you to solve.
