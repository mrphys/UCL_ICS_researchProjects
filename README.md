# UCL Institute of Cardiovascular Science iBSc and MSc Independent Research Project Matching Process

## Overview

This page documents the process used for the UCL Institute of Cardiovascular Science iBSc and MSc Cardiovascular Science programmes to match students and supervisors for their independent research project modules. A workflow for the process can be seen below, followed by more detailed instructions and templates for each step of the process.

### Workflow

<img src = "https://github.com/scottchiesa/Project_Matching_Algorithm/blob/patch-1/Flowcharts.jpeg">

## Call for Proposals
### Generating a PDF List of Projects to Offer to Students

1) Potential supervisors submit project proposals using form such as that shown in following [MS Form](https://forms.office.com/e/3XSMBR9YRP)
2) Once complete, all proposals downloaded as Excel sheet similar to that shown in 'ProjectList.xlsx' and filtered to separate iBSc and MSc projects.
3) 'ProjectList.xlsx' merged with 'ProjectList_MailMerge.doc' to create PDF booklet to circulate to students on respective programmes.

## Allocation of Projects
### Student Selection of Preferred Projects

1) Students with pre-arranged projects (e.g. clinical students already working with pre-existing supervisor, students who have arranged external project) removed from allocation process.
2) All remaining students select top six desired projects from list of available projects in order of preference using form such as that shown in following [MS Form](https://forms.office.com/e/EpW7UzMGwj)
3) Once complete, all preferences downloaded as Excel sheet similar to that shown in 'AllProjectData.xlsx'.

### Matching of Students and Projects

Here we use a mathematical optimizer to 'best' match between the students choices to the research projects available. We have used Google's open source software suite for optimization, OR-Tools, which provides an MPSolver wrapper for solving linear programming and mixed integer programming problems. This is a mixed integer programming (MIP) problem Since the constraints are linear, this is a linear optimization problem in which the solutions are required to be integers. More information about algorithm can be found here: https://developers.google.com/optimization/mip/mip_example. We use the MIP solver 'SCIP' (Solving constraint integer problems). https://www.scipopt.org which is currently one of the fastest non-commercial solvers for mixed integer programming. SCIP is a framework for Constraint Integer Programming oriented towards the needs of mathematical programming experts who want to have total control of the solution process and access detailed information down to the guts of the solver. In SCIP the problem is successively divided into smaller subproblems (branching) that are solved recursively.(details of the algorithm can be found here: https://www.scipopt.org/doc/html/WHATPROBLEMS.php )

1) Upload ‘FINAL_MatchingAlgorithm_MSc2022.ipynb’ to a Colab Notebook on Google Drive using https://colab.research.google.com/
2) Upload 'AllProjectData.xlsx' to a folder on the same Google Drive ensuring that line of code in opening section of .ipynb file points to this folder and file.
3) Run Code to generate new file called ‘AllProjectData_time_date.xlsx’

## 
