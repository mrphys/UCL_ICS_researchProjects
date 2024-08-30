# UCL Institute of Cardiovascular Science iBSc and MSc in Cardiovascular Science Project Matching Algorithm

## Overview

This page documents the process used for the UCL Institute of Cardiovascular Science iBSc and MSc Cardiovascular Science programmes to match students and supervisors for their independent research project modules. A workflow for the process can be seen in the flowchart below. In short, however, the 



Code used for matching UCL ICS students to research projects for the iBSc and MSc for 2022
Here we use a mathematical optimizer to 'best' match between the students choices to the research projects available.

We have used Google's open source software suite for optimization, OR-Tools, which provides an MPSolver wrapper for solving linear programming and mixed integer programming problems.

This is a mixed integer programming (MIP) problem Since the constraints are linear, this is a linear optimization problem in which the solutions are required to be integers.

More information about algorithm can be found here: https://developers.google.com/optimization/mip/mip_example

We use the MIP solver 'SCIP' (Solving constraint integer problems). https://www.scipopt.org which is currently one of the fastest non-commercial solvers for mixed integer programming.

SCIP is a framework for Constraint Integer Programming oriented towards the needs of mathematical programming experts who want to have total control of the solution process and access detailed information down to the guts of the solver.

In SCIP the problem is successively divided into smaller subproblems (branching) that are solved recursively.(details of the algorithm can be found here: https://www.scipopt.org/doc/html/WHATPROBLEMS.php )
