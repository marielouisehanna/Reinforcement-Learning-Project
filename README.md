
# Reinforcement Learning Project

## Overview

This project explores and compares three strategies for balancing exploration and exploitation in Reinforcement Learning. The aim is to analyze their performance using a custom crawler implementation. The strategies implemented and evaluated include:

1. **Fixed Epsilon-Greedy Strategy** (provided in the base code).
2. **Decreasing Epsilon-Greedy Strategy**.
3. **Optimistic Exploration Function** using a custom formula.

The project measures the cumulative regret of these methods to determine their effectiveness over multiple runs.

---

## Objective

The key goals of this project are:

- Implement and compare the performance of different exploration strategies.
- Measure cumulative regret for each method to understand the trade-off between exploration and exploitation.
- Analyze how exploration strategies affect learning in a reinforcement learning environment.

---

## Exploration Strategies

1. **Fixed Epsilon-Greedy**:
   - Uses a constant epsilon value to decide between exploration and exploitation.

2. **Decreasing Epsilon-Greedy**:
   - Dynamically reduces epsilon over time as the agent learns.

3. **Optimistic Exploration Function**:
   - Uses the formula:

     \[
     f(u, n) = u + \frac{k}{\sqrt{n}}
     \]

     Where:
     - \( u \): Q-value.
     - \( n \): Visit count.
     - \( k \): Optimism factor, tuned to balance the level of exploration for less-visited states.

---

## Tasks Completed

### 1. Understand the Base Code
- Reviewed the provided crawler implementation.
- Identified the implementation of the epsilon-greedy strategy.

### 2. Implement Exploration Strategies
- **Decreasing Epsilon**:
  - Modified the epsilon-greedy approach to reduce epsilon as a function of the episode number.
- **Optimistic Exploration Function**:
  - Implemented the custom exploration function and tuned the parameter \( k \).

### 3. Compare the Strategies
- Conducted experiments to measure and plot cumulative regret for all strategies.
- Analyzed results to understand the impact of each method.

---

## Results and Analysis

- **Cumulative Regret**:
  - Measured and plotted regret for each method across multiple episodes.
- **Performance**:
  - Discussed the impact of exploration strategies on learning efficiency and regret minimization.
- **Parameter Tuning**:
  - Explored the effect of different \( k \) values on the performance of the optimistic exploration function.

---

## Deliverables

1. **Code Implementation**:
   - Contains the crawler implementation with all three strategies integrated.

2. **Video Explanation**:
   - Demonstrates the code modifications for each strategy.
   - Explains the results using visual plots of cumulative regret.

---

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/marielouisehanna/Reinforcement-Learning-Project.git
   cd Reinforcement-Learning-Project
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the crawler with different strategies:
   - Fixed Epsilon:
     ```bash
     python crawler.py --strategy fixed
     ```
   - Decreasing Epsilon:
     ```bash
     python crawler.py --strategy decreasing
     ```
   - Optimistic Exploration:
     ```bash
     python crawler.py --strategy optimistic --k <value>
     ```

4. Generate plots:
   ```bash
   python plot_results.py
   ```

---

## Contributors

- **Sarah Fakih**
- **Mona el Hajj Chehade**
- **MarieLouise Hanna**


---

