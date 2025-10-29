# Educationnal Trajectory-Based Recommender System (TBRS) Notebook

This notebook explores the application of **control theory** and **Model Predictive Control (MPC)** to the design of **Educationnal Trajectory-Based Recommender Systems (ETBRS)**, as presented in:

> **E. Schaffter, A. Bounekkar, and E. Negre**,  
> *Trajectory-Based Recommender Systems as Control Systems*,  

A TBRS models the learner’s progression as a **dynamical system**:

$$
x(t{+}1) = A\,x(t) + B\,u(t)
$$

where:
- \(x(t)\) represents the learner’s **competence state** at time \(t\),
- \(u(t)\) represents the **recommended resources or actions**,
- matrices \(A\) and \(B\) encode the **learning dynamics** and the effect of recommendations.

---

## Objectives

This notebook demonstrates how to:

- Simulate **learning trajectories** under different recommendation policies.  
- Implement **Model Predictive Control (MPC)** to guide the learner toward a **target competence vector**.  
- Visualize **state evolution**, **control actions**, and **system convergence**.  

---

## Conceptual Framework

TBRS extends traditional recommender systems by introducing **temporal and goal-oriented dynamics**.  
Rather than predicting isolated ratings, it computes an **optimal trajectory** of recommendations that minimizes a quadratic cost function.

This formalism enables:
- **Constrained recommendations** (e.g., prerequisite ordering, cognitive load control)  
- **Adaptive re-optimization** at each step (receding horizon)  
- **Evaluation of long-term effectiveness** instead of short-term accuracy

---

