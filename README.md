# Artificial Intelligence Nanodegree
## Introductory Project: Diagonal Sudoku Solver

# Question 1 (Naked Twins)
Q: How do we use constraint propagation to solve the naked twins problem?  
A: Constraint Propagation is all about using local constraints in a space (in the case of Sudoku, the constraints of each square) to dramatically reduce the search space. As we enforce each constraint, we see how it introduces new constraints for other parts of the board that can help us further reduce the number of possibilities.

   It is to use constraints recursively to reduce number of possibilities.
   
   For this project, the constraint is naked twins. 
   
   The strategy in solution.py is to first find all boxes with 2 values and then set boxes with same 2 values as naked_twins.    Then remove these 2 values from peers to both of this twin.    
   ![naked-twins-2](https://user-images.githubusercontent.com/21303325/27258913-960ee440-53cc-11e7-82e0-416a070fc2ab.png)
   

# Question 2 (Diagonal Sudoku)
Q: How do we use constraint propagation to solve the diagonal sudoku problem?  
A: We create a flag for diagonal sudoku. If it is diagonal sudoku, we create two additional units as the diagonals of the grid. Thus, the corresponding diagonal entries are included in peers. 

### Install

This project requires **Python 3**.

We recommend students install [Anaconda](https://www.continuum.io/downloads), a pre-packaged Python distribution that contains all of the necessary libraries and software for this project. 
Please try using the environment we provided in the Anaconda lesson of the Nanodegree.

### Visualizing

To visualize your solution, please only assign values to the values_dict using the `assign_value` function provided in solution.py
