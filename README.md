﻿# Scheduling-with-Linear-Programming
 
Overview

This project aims to solve the Hybrid Flow Shop Scheduling Problem (HFSP) with dedicated machines using Linear Programming. The code uses the GurobiPy library to solve the linear programming problem. It also provides a basic user interface using Tkinter that allows the input to be provided manually or using an Excel file. The output is presented in the form of a Gantt diagram.

Input of the program

The inputs for the program include:
 Matrix of processing times Pij
 Dedicated machine stages
 Assignment of jobs to the machines in the dedicated resource stage
 
Decision variables

The decision variables used in the program are:
 Tij: Start time of job j in stage i
 Yihj: 1 if job h precedes job j in stage i, 0 otherwise
 
Model

 The objective of the model is to minimize the makespan (Cmax), subject to the following constraints:
 M1: Consistency of the start times of a job when moving from one stage to the next
     T i+1 j -T ij ≥ pij
 M2: Ordering of jobs in a given stage i
     Yihj + Yijh =1
 M3: Consistency of start times of jobs on the same stage i, except for the dedicated machine stage
     Tij –Tih ≥ pih + M (Yihj -1)
     Tij –Tih ≥ pih + M (Yihj -1)
 M4: Makespan constraint
     Tmj+ pnj ≤Cmax
     
Usage

 To use the HFSP scheduling algorithm, follow these steps:
 1- Install the required libraries including GurobiPy.
 2- Clone the repository.
 3- Run the main.py script.
 4- Provide the input manually or using an Excel file.
 5- The algorithm will output the solution in the form of a Gantt chart.
 
Credits

  This project is based on the research presented in "Decision Support System for Hybrid Flow Shop Scheduling Problem" (2022) by Ala Zammiti, Aymen Benali, Hejer KHlif     Hachicha and Sana Bouajaja in Mathematical Methods of Operations Research. We would like to acknowledge the contribution of Ala Zammiti to the development of the HFSP     scheduling algorithm.
