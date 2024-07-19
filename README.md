# Grid World Optimal Policy Calculation

This project contains Python code to calculate optimal policies in a grid world using three different methods: Bellman Optimality Equation, Policy Iteration, and Value Iteration. The project uses a 5x5 grid and defines actions and rewards for specific states.

## Table of Contents

- [Overview](#overview)
- [Setup](#setup)
- [Usage](#usage)
- [Methods](#methods)
  - [Bellman Optimality Equation](#bellman-optimality-equation)
  - [Policy Iteration](#policy-iteration)
  - [Value Iteration](#value-iteration)
- [Results](#results)
- [License](#license)

## Overview

The goal of this project is to find the optimal policy for an agent navigating a 5x5 grid. The agent can move up, down, left, or right, and certain cells in the grid have rewards or penalties. The agent's objective is to maximize its cumulative reward.

## Setup

1. Ensure you have Python installed (preferably Python 3.7 or higher).
2. Install the required libraries using pip:
    ```sh
    pip install numpy matplotlib
    ```

## Usage

1. Clone this repository or download the files.
2. Run the Python script to see the results of the optimal policies.
    ```sh
    python grid_world_optimal_policy.py
    ```
3. The script will calculate and display the optimal policies using three different methods and plot the results using `matplotlib`.

### Rewards
- Default reward for each step is `-0.2`
- Specific rewards:
  - Blue square (at [0, 1]): `5`
  - Green square (at [1, 2]): `2.5`

### Terminal States
- Terminal states are at positions `[2,4]` and `[4, 0]`

### Actions
- The agent can move up, down, left, or right.


### Parameters
- `size`: Size of the grid (default is `5`)
- `episodes`: Number of episodes to run (default is `1000`)
- `gamma`: Discount factor (default is `0.95`)
- `epsilon`: Exploration factor for ε-soft policy (default is `0.1`)

## Methods

### Bellman Optimality Equation

This method uses the Bellman Optimality Equation to calculate the optimal state values iteratively. It updates the value function until it converges to a stable state.

### Policy Iteration

This method involves two main steps: policy evaluation and policy improvement. The policy evaluation step calculates the value function for a given policy, and the policy improvement step updates the policy based on the value function. These steps are repeated until the policy becomes stable.

### Value Iteration

This method updates the value function iteratively using a combination of policy evaluation and policy improvement. It converges faster than the policy iteration method by updating the value function directly without the explicit policy improvement step.

## Results

The optimal policies for each method are printed and plotted using `matplotlib`. The arrows in the plots represent the optimal actions for each state in the grid.

---

### Notes

1. The grid size, rewards, and transition probabilities are hard-coded but can be modified as needed.
2. The convergence threshold for iterative methods is set to \(1e-10\) for precise results.

---
