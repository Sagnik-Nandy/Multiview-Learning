# Multi-Modal Factor Regression for Multi-View Data Prediction

This repository contains code and resources for predicting response variables in a multi-modal factor regression setting, where data consists of observed covariates \((X_i, Z_i)\) and response \(y_i\) values. This approach models the response \(y_i\) as linearly dependent on a latent factor \(u_i\), with \(X_i\) and \(Z_i\) serving as co-variates that offer complementary information and are conditionally independent given \(u_i\).

## Model Overview
The multi-modal factor regression model is defined as:
\[
X_i = \frac{\lambda}{n} v u_i + w_i, \quad Z_i = \frac{\mu}{n} \widetilde{v} u_i + \widetilde{w}_i, \quad y_i = \alpha u_i + \varepsilon_i,
\]
where \(u_i\) are latent factors, \(v\) and \(\widetilde{v}\) are factor loadings, and noise terms are independently distributed.

## Key Contributions

1. **Prediction Algorithm for Query Subjects**: 
   - A fully data-adaptive algorithm using Approximate Message Passing (AMP) to estimate latent factors from observed data. 
   - We propose two point predictors for the query response \(y_*\): 
     - **Early Fusion Predictor**: Combines information from both covariates \(x_*\) and \(z_*\) for prediction.
     - **Late Fusion Predictor**: Constructs separate predictions from \(x_*\) and \(z_*\) and combines them optimally.
   - Asymptotic analysis of prediction errors under squared loss is provided.

2. **Prediction Risk Analysis**:
   - Analytical evaluation of prediction risk in the multi-view cooperative learning framework (details in progress).

3. **Numerical Comparisons**:
   - Empirical comparisons of proposed predictors with alternative methods (details in progress).

## Repository Structure

- `Code/`: Code for the AMP algorithm and prediction methods.
- `Results/`: Stores outputs and performance metrics for empirical evaluations.
- `References/`: Contains citations and additional resources.
- `Draft/`: Working drafts and documentation.
