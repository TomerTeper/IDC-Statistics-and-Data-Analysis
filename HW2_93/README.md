
# Homework 2: Data Exploration, Independence, and Distributions

## Overview
This homework consists of five main questions focusing on data exploration, independence, conditional independence, and distribution analysis. You will work with the `Diabetes` dataset, probability theory, Markov chains, normal distributions, and binomial distributions.

## Key Topics Covered
- Data exploration and visualization
- Correlation analysis
- Independence and conditional independence
- Normally distributed random variables
- Central Limit Theorem (CLT)
- Markov chains and transition matrices
- Ordered statistics and binomial distributions

## Questions Overview

### Question 1: Data Exploration and Visualization (Practical)
You will explore the `Diabetes` dataset from `sklearn`, perform visualizations, and analyze correlations between features.

**Tasks**:
1. Describe the dataset and its features.
2. Produce histograms and boxplots for all features.
3. Generate a correlation matrix and identify highly correlated features.
4. Create scatter plots with marginal histograms for two pairs of features with the highest correlation.
5. Report two interesting trends in the data, including the relationship between BMI and diabetes progression, and the effect of age on diabetes progression.

### Question 2: Independence and Conditional Independence (Theoretical)
This question examines the joint distribution of discrete random variables and explores the number of parameters needed to define these distributions under different independence assumptions.

**Tasks**:
- Define the joint distribution of \(X\), \(Y\), and \(Z\).
- Compute the number of parameters required when \(X\), \(Y\), and \(Z\) are independent.
- Determine how conditional independence between \(X\) and \(Y\) given \(Z\) changes the number of parameters.
- Provide an example where unconditional independence does not imply conditional independence.

### Question 3: Normally Distributed Salaries (Theoretical)
You will work with normally distributed salary data from a fictional company in Randomistan.

**Tasks**:
- Calculate the percentage of employees earning less than 50,000 RCU.
- Calculate the percentage of employees earning between 50,000 and 77,500 RCU.
- Determine the percentage of employees earning more than 115,000 RCU.
- Estimate how many of the 1000 employees earn more than 150,000 RCU.

### Question 4: Central Limit Theorem for Markov Chains (Practical)
You will simulate 1000 trajectories using a Markov chain model for dice rolls, and analyze the resulting distribution of averages.

**Tasks**:
- Simulate trajectories of dice rolls with 30 and 500 rolls per trajectory.
- Plot histograms of the averages and fit normal distributions.
- Calculate the covariance between the first and subsequent dice rolls.

### Question 5: Distributions and Sampling (Practical)
You will analyze the behavior of sorted observations from a sample and compute probabilities related to ordered statistics.

**Tasks**:
- Calculate the probability that all samples exceed a certain threshold.
- Derive the distribution of the number of samples below a threshold.
- Write code to compute the index \(\lambda(n)\) for which the probability that the sorted sample is below the threshold exceeds 90%.
- Run experiments to validate your findings.



