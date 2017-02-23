# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: The naked twins strategy is describe as follows. We first identify pairs of boxes within the same unit as naked twins if they satisfy the following properties: (1)Each box in a pair can fill in two possible numbers (2) The two numbers that the two boxes in the same pair can fill in are identical. If the two properties are satisfied, we can conclude that if any of the two numbers appear in another box in the same unit, excluding the two boxes identified as naked twins, it can be deleted from the possible-number-list in that box.

This strategy can be applied on top of the "only-one-choice" and the "elimination" strategies to further reduce the search space.

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: To solve the diagonal Sudoku, we can simply include the "diagonal unit" into the unit list. In the code, these two units are: ['A1','B2','C3','D4','E5','F6','G7','H8','I9'] and ['A9','B8','C7','D6','E5','F4','G3','H2','I1']. By incorporating these two units, during the elimination and the search procedure, numbers 1 through 9 are required to appear exactly once.

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

##### Optional: Pygame

Optionally, you can also install pygame if you want to see your visualization. If you've followed our instructions for setting up our conda environment, you should be all set.

If not, please see how to download pygame [here](http://www.pygame.org/download.shtml).

### Code

* `solutions.py` - You'll fill this in as part of your solution.
* `solution_test.py` - Do not modify this. You can test your solution by running `python solution_test.py`.
* `PySudoku.py` - Do not modify this. This is code for visualizing your solution.
* `visualize.py` - Do not modify this. This is code for visualizing your solution.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the ```assign_values``` function provided in solution.py

### Data

The data consists of a text file of diagonal sudokus for you to solve.