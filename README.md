# Lab 2 - Dynamic Programming  
## GridWorld MDPs, Value Iteration & Policy Iteration

## Overview

This project explores **Dynamic Programming (DP)** methods for solving **Markov Decision Processes (MDPs)** using a custom GridWorld environment and standard benchmarks.

### 1. Custom GridWorld Environment
- Configurable **N × N grid** (e.g., 4×4)
- Supports:
  - Deterministic transitions
  - Stochastic transitions (80–10–10 probability split)
- Implements full transition model:

  \[
  P(s', r \mid s, a)
  \]

- Features:
  - Absorbing goal state
  - Configurable reward structure

---

### 2. Dynamic Programming Algorithms
- **Value Iteration (VI)**
- **Policy Iteration (PI)**

Both methods include:
- Synchronous updates
- In-place updates

Uses:
- Tabular value function:  
  \[
  V(s)
  \]
- Policy representation:  
  \[
  \pi(s)
  \]

---

### 3. Experiments & Visualization
- Evaluations on:
  - Deterministic GridWorld
  - Stochastic GridWorld
  - `FrozenLake-v1` environment

#### Visualizations
- Value function heatmaps
- Policy visualization (quiver plots)
- Convergence curves (Δ vs iteration)
- Runtime and iteration comparisons

---

## Setup

Install required dependencies:

```bash
pip install numpy matplotlib gymnasium
```

## Load Libraries
```python
import numpy as np
import matplotlib.pyplot as plt
import gymnasium as gym
import time
```

## Key Settings
- **Discount Factor (γ):**  
  γ = 0.9 − 0.99  

- **Convergence Threshold (θ):**  
  θ = 10⁻⁶  

- **Rewards:**  
  `step_reward = -1`, `goal_reward = 10`  
  **or**  
  `step_reward = 0`, `goal_reward = 1`  

## Summary
- **Value Iteration:** gradual convergence, slower in stochastic settings  
- **Policy Iteration:** fewer iterations, faster convergence  
- **Stochastic environments:** smoother values, more conservative policies  

