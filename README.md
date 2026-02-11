I can't directly create a Markdown file (`.md`) or push files to GitHub using this app, but I can generate the content for your **README.md** based on the project files. You can copy and paste the following content into a file named `README.md` in your project's root directory before pushing to your repository.

-----

# Master's Project Report: Equitable Optimization

## Authors

  * Mohammed Aroui
  * Nolwenn Pigeon

## Academic Year

2022/2023 - Semester 1

## Project Overview

This Master's project in Optimization (MOGPL) focuses on finding **efficient and equitable** solutions for various optimization problems. The primary goal is to maximize an objective function $f(x)$ that incorporates a **fairness criterion** based on the **Lorenz vector**, which allows for achieving a balanced utility vector $z(x)$.

The approach involved:

1.  Linearizing the fairness function to make it solvable using Linear Programming (LP).
2.  Applying this equitable linear model to three distinct decision-making problems.

## Project Structure

The implementation code is in the notebook [projetMOGPL.ipynb](https://drive.google.com/open?id=1BTgWxUr_yw4Wh52-jtBkJto0oqhN34GR) (FileChip1) and should be executed sequentially. The detailed report is available in the PDF file [Mogpl\_Proj.pdf](https://drive.google.com/open?id=1KIwr9itmiGB09DaEvfV94-Fb3u3hlOui) (FileChip2).

| Section      | Application                            | Main Objective                                                                               | Key Result (Example)                                                                                                                                                         |
| :----------: | :------------------------------------: | :------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| **Part I**   | Linearization of $f$                   | Develop the dual model to solve the fairness function using LP.                              | The dual formulation successfully computed the Lorenz vector for $(4,7,1,3,9,2)$, yielding $\\{1.0, 3.0, 6.0, 10.0, 17.0, 26.0\\}$.                                          |
| **Part II**  | Equitable Sharing of Indivisible Goods | Assign $p$ indivisible objects to $n$ individuals to maximize an equitable utility function. | For $n=3, p=6$ with $w=(3,2,1)$, the solution obtained is $(335, 340, 325)$ (balanced), contrasting with the inequitable solution from average maximization $(0, 760, 240)$. |
| **Part III** | Multicriteria Project Selection        | Select projects under a budget constraint, optimizing for the equity of utilities.           | With $w=(2,1)$, the solution selects projects $x=(1,0,0,1)$ for a utility vector $(21,20)$ (balanced).                                                                       |
| **Part IV**  | Robust Path Finding in a Graph         | Find a path that minimizes the total cost equitably across multiple uncertain scenarios.     | A robust path was found with a cost of $(10, 10)$ across the two scenarios, demonstrating balance.                                                                           |

## Technologies Used

  * **Modeling:** Linear Programming (LP) and Mixed Integer Programming (MIP).
  * **Implementation:** Python (in the IPython Notebook).
  * **Solver:** [Gurobi Optimizer](https://www.gurobi.com/) (via the `gurobipy` library).
