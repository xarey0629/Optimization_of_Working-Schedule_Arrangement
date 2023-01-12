# Scheduling Optimization
- 🍒 Midterm Project of Programming Design at National Taiwan University
- 👨‍💻 Instructed by Prof. Ling-Chieh Kung and Prof. Cheng-Yuan Ho
- 🏅 Rated ${1st}$ in 02 class, ${4th}$ in 50 teams

## Goal

- There are a total of  ${n_I}$  employees, and  ${n_K}$  represents the number of shift types.
- This program must schedule a shift schedule for  ${n_J}$  days in the following month.
- ${ min }$ ( labor shortage + ${w1}$ × unfulfilled leave requests + ${w2}$ × total excess overtime hours )

## Rules

- Each employee must have at least ${L}$ days of complete leave during the next ${n_J}$ days of scheduling.
- Each employee must have at least one day of complete leave within every consecutive seven days.
- Each employee can only be assigned exactly one shift type per day.

## Input

- The first row stores seven integers: ${n_I}$ , ${n_J}$ , ${n_K}$ , ${L}$ , ${w_1}$ , ${w_2}$ and ${R}$ .

- The following information is divided into three parts:

    1. Scheduling status of each time period for the ${n_K}$ types of shifts
        - Each column contains 24 integers, indicating the time periods that the k-th shift type needs to be on duty.
        - The ${n_K + 2}$ th column will always store the scheduling status of the 0th shift (complete leave)

    2. Manpower demand for each time period on ${n_J}$ days
        - Each column contains 24 integers, indicating the manpower demand for each time period on the ${j}$ th day.
        - In the input data, one column represents a day and one row represents a time period.

    3. Vacation requests
        - Each row contains R integers, which sequentially represent the employee numbers of the leave requests; sequentially representing the dates that the employees hope to take leave.
        -  For example, if ${i_1 = 3}$ and ${j_1 = 5}$, it means that the first leave request is from the third employee who hopes to take leave on the fifth day.

- Variable Range
    - ${10 ≤ n_I ≤ 100}$
    - ${n_J}$ ∈ {28, 29 ,30, 31}
    - ${5 ≤ n_K ≤ 30}$
    - L ∈ {8, 9, 10}
    - ${1 ≤ w_1 ≤ 100}$
    - ${1 ≤ w_2 ≤ 100}$
    - ${0 ≤ R ≤ n_in_j}$
    - ${s_{k,t}}$ ∈ {0, 1}
    - ${0 ≤ d_{j,t} ≤ n_I}$
