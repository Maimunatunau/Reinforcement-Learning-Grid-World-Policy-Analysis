# Reinforcement Learning: Grid World Policy Analysis

## Overview

This task involves analyzing a variant of the grid world problem where an agent navigates a grid while maximizing rewards. The agent must select movement actions based on transition probabilities and expected utilities.

## Grid World Environment

- **States:** The grid consists of regular states, inaccessible states (black-shaded), and terminal states (grey-shaded).
- **Rewards:**
  - Non-terminal states: -0.2 per step
  - Terminal states: Defined by their given values
- **Movement Constraints:**
  - Allowed movements: Up, Down, Left, Right (no diagonal movement)
  - Movement probability:
    - Intended direction: 80% probability
    - Perpendicular move (left or right of intended direction): 20% probability (10% each)
  - If an invalid move is attempted (out of grid or into an inaccessible state), the agent stays in place.

## Objective

- **Derive the policy** that results in the displayed utility values.
- **Illustrate the policy** as a diagram.
- **Explain action selection** for the three highlighted states.

## Methodology

1. **Understanding Utility Values:**
   - The displayed utilities are the result of a policy evaluation process.
   - These values represent the expected long-term reward for each state under the policy.
2. **Deriving the Policy:**
   - The optimal policy selects the action that maximizes the expected utility.
   - For each state, the best action is determined using the Bellman equation:
     \[ U(s) = R(s) + \gamma \sum_{s'} P(s'|s,a) U(s') \]
   - Where:
     - \(U(s)\) is the utility of state \(s\)
     - \(R(s)\) is the immediate reward for \(s\)
     - \(\gamma\) is the discount factor
     - \(P(s'|s,a)\) is the transition probability
3. **Explaining the Three Highlighted States:**
   - Compute expected utility for each possible action.
   - Compare values to select the action with the highest expected return.

## Results: Refer to the results file

## Future Work

- Extend the analysis to incorporate discount factors and varying reward structures.
- Implement policy iteration or value iteration in Python for further insights.



This project is part of my reinforcement learning portfolio. Feedback and discussions are welcome!

