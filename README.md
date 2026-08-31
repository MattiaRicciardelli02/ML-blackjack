# Blackjack Reinforcement Learning

This project explores the use of **Reinforcement Learning (RL)** to train an autonomous agent to play **Blackjack**.

The goal is to investigate how an agent can learn a playing strategy through interaction with the environment, without being explicitly programmed with an optimal Blackjack strategy.

Two different Reinforcement Learning approaches are implemented and compared:

- **Q-Learning**
- **Deep Q-Network (DQN)**

## Project Overview

Blackjack can be modeled as a sequential decision-making problem in which an agent observes the current state of the game, chooses an action, and receives a reward based on the final outcome of the hand.

The agent improves its strategy by repeatedly playing games and learning from the rewards obtained.

This project studies two different ways of estimating the value of actions.

### Q-Learning

The first approach uses **Q-Learning**, a model-free Reinforcement Learning algorithm.

Q-Learning learns an action-value function:

Q(s, a)

which represents the expected future reward of taking action `a` while in state `s`.

The values are stored explicitly in a **Q-table** and updated as the agent interacts with the Blackjack environment.

This approach is particularly suitable when the state and action spaces are relatively small and discrete.

### Deep Q-Network (DQN)

The second approach uses a **Deep Q-Network (DQN)**.

Instead of storing Q-values explicitly in a table, DQN uses a **neural network** to approximate the Q-function:

Q(s, a; θ)

where `θ` represents the parameters of the neural network.

The network receives a representation of the current Blackjack state and estimates the expected value associated with the possible actions.

This makes it possible to study how a Deep Reinforcement Learning approach behaves on the same problem solved with traditional Q-Learning.

## Objective

The main objective of the project is to compare a **tabular Reinforcement Learning approach** with a **Deep Reinforcement Learning approach** on the same Blackjack environment.

In particular, the project investigates:

- how an agent learns a Blackjack strategy through experience;
- the evolution of its performance during training;
- the differences between Q-Learning and DQN;
- the advantages and limitations of using a neural network instead of a Q-table.

## Repository Structure

```text
ML-Blackjack/
│
├── blackjack_q_learning.ipynb   # Q-Learning implementation
├── blackjack_DQN.ipynb          # Deep Q-Network implementation
└── README.md
