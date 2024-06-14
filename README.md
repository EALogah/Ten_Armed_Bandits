# Part 1:  Ten_Armed_Bandits
## Overview

This repository contains the implementation of various bandit learning algorithms to solve the k-armed bandit problem. The algorithms include:

1. Greedy with non-optimistic initial values.

2. Epsilon-greedy with various epsilon values.

3. Optimistic initial values with a greedy approach.

4. Gradient bandit algorithm with different learning rates.

# Part 2: 
 Non-Stationary Bandit Algorithms 

## Overview

This part is an overview of the multi-armed bandit algorithms, focusing on their performance under non-stationary conditions.

## Algorithms

### Optimistic Greedy

- **Description**: Begins with an optimistic initial value for action estimates to encourage exploration.
- **Initialization**: All action values are initialized to a high value (e.g., 5.0).
- **Action Selection**: Always selects the action with the highest estimated value.
- **Update Rule**: Incrementally updates the value of the selected action based on the observed reward.

### Epsilon-Greedy with Fixed Step Size

- **Description**: Balances exploration and exploitation using a fixed probability Epsilon of selecting a random action.
- **Initialization**: All action values are initialized to zero.
- **Action Selection**: With probability Epsilon, a random action is selected; otherwise, the action with the highest estimated value is chosen.
- **Update Rule**: Uses a fixed step size alpha to update the value of the selected action.

### Epsilon-Greedy with Decreasing Step Size

- **Description**: Similar to the fixed step size variant but uses a step size that decreases over time.
- **Initialization**: All action values are initialized to zero.
- **Action Selection**: With probability Epsilon, a random action is selected; otherwise, the action with the highest estimated value is chosen.
- **Update Rule**: Uses the average of all observed rewards for the selected action, with the step size decreasing as more rewards are observed.

## Non-Stationary Changes

### Gradual Drift

- **Mechanism**: The mean of the reward distribution drifts gradually.

### Mean-Reverting Change

- **Mechanism**: The mean of the reward distribution reverts to a long-term mean.

### Abrupt Shifts

- **Mechanism**: The mean of the reward distribution changes abruptly at random intervals.


- **Experiments**: Each algorithm was run for 1000 experiments with 10,000 steps each.
- **Metrics**: The distribution of rewards at the terminal step (10,000) was analyzed to evaluate the performance.


# Requirements
Python 3.x

NumPy

Matplotlib

Seaborn

# Installation
Clone the repository and install the required packages:

# Usage
Run the main script to execute the bandit algorithms and generate the plots:

# Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

# License
This project is licensed under the MIT License.



