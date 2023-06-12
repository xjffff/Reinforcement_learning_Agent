# Reinforcement_learning_Agent
This repository contains the code and resources for the research project on Reinforcement Learning for Tactic Portfolio Allocation.

## Introduction
Portfolio management is a critical aspect of finance, as it plays a vital role in wealth growth for both individuals and large entities. This project focuses on the optimization of portfolio allocation using reinforcement learning techniques. Traditional theories, such as the mean-variance optimization model by Markowitz and the capital growth theory by Hakansson and Ziemba, have provided valuable insights into portfolio selection. However, the question remains whether reinforcement learning agents can outperform traditional financial experts. Unlike humans, reinforcement learning agents make decisions based on trained policies derived from historical data, eliminating emotional biases.

Machine learning, particularly reinforcement learning, has gained significant attention in portfolio management. This project explores the application of continuous-action reinforcement learning algorithms to address the stocks portfolio optimization problem. The benchmark for comparison is the Markowitz mean-variance model. The project utilizes the FinRL library, which provides a reinforcement learning environment for portfolio management.

## Problem Statement and Data Structure
The project assumes a set of risky assets, including equity, bonds, and derivatives, and a risk-free asset. The goal is to optimize the investor's final capital by actively reallocating positions while considering transaction costs, risk-free rates, and other constraints.

The project utilizes a Markov Decision Process (MDP) framework to formulate the problem. The MDP is defined by the state space, action space, state transition probability matrix, reward function, and discount factor. The action space represents the percentage of wealth distribution in each asset, forming a continuous action space. The state space consists of today's price and technical indicator matrix, including moving averages, momentum indicators, and covariance.

The reward function is designed to evaluate the performance of the reinforcement learning agent. Two different reward structures are implemented to test convergence. The A2C (Advantage Actor-Critic) algorithm, a model-free, on-policy reinforcement learning algorithm, is utilized for training the actor and critic networks.

## Baseline Model
Two baseline models are used for comparison:

1. Uniform Buy and Hold: The initial capital is equally divided and invested in all assets for the entire trading period.
2. Markowitz Mean-Variance Optimization Model: This classical approach to portfolio management considers the expected return and variance of each asset. The goal is to maximize the expected return while maintaining a specified level of risk.
