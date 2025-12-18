# Python Programming Task 3

This folder contains the third module of the internship. This section moves into more complex **Algorithmic Thinking**, utilizing simulation, interval checking, and advanced optimization techniques like **Dynamic Programming**.

## 📂 File Contents

### `Programming Task - 3(for Advance (EDA) Python Programmers .ipynb`

This notebook tackles 5 problems that focus on optimization and logical constraints.

* **Optimization**:
    * *Maximum Product of Two Elements*: Finding the two largest numbers in an array without sorting.
* **Combinatorics & Logic**:
    * *Count Number of Teams*: Identifying strictly increasing or decreasing triplets in a sequence.
* **Intervals**:
    * *Number of Students Doing Homework*: Checking if a query time falls within start and end time ranges.
* **Simulation & Bitwise**:
    * *Number of Steps to Reduce a Number to Zero*: Simulating a process based on even/odd conditions.
* **Dynamic Programming / Bit Manipulation**:
    * *Counting Bits*: Generating an array representing the number of 1s in the binary representation of numbers using the relationship `dp[i] = dp[i >> 1] + (i & 1)`.

## 🧠 What I Learned
* **Optimization vs Brute Force**: Solving "Max Product" by tracking the top two maximums in a single pass ($O(n)$) rather than sorting ($O(n \log n)$).
* **Dynamic Programming Patterns**: Understanding how to use previous results (`dp`) to solve the "Counting Bits" problem efficiently.
* **Interval Logic**: Handling time ranges and conditional checks within arrays.

## 🛠 Prerequisites
* Python 3.x
* Jupyter Notebook

## 🚀 How to Run
1.  Navigate to this folder.
2.  Launch Jupyter Notebook: `jupyter notebook`
3.  Open `Programming Task - 3(for Advance (EDA) Python Programmers .ipynb` to execute the cells.
