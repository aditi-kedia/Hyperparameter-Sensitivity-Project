# Hyperparameter Sensitivity Analysis in Machine Learning

## Overview

This project investigates how sensitive machine learning models are to changes in hyperparameters across different datasets. Instead of focusing only on best-performing configurations, this study analyzes **performance variability**, which reflects model robustness and tuning effort.

## Key Idea

Hyperparameter sensitivity is measured as the **variance of performance metrics** (Accuracy, F1-score, AUC) across different hyperparameter settings.

## Datasets

We evaluated models on five datasets from the UCI Machine Learning Repository:

* Iris
* Wine Quality
* Breast Cancer Wisconsin (Diagnostic)
* Heart Disease (Cleveland)
* Adult

These datasets vary in size, class balance, and complexity, allowing us to study how dataset characteristics influence sensitivity. 

## Models Evaluated

* Logistic Regression
* k-Nearest Neighbours (KNN)
* Decision Trees
* Support Vector Machines (SVM)
* Multi-Layer Perceptron (MLP)

## Methodology

* Preprocessing:

  * Handling missing values
  * Encoding categorical variables
  * Feature standardization
* Evaluation:

  * Cross-validation (5-fold / 10-fold)
* Sensitivity Metric:

  * Variance of Accuracy, F1-score, and AUC across hyperparameter configurations

## Key Findings

### Model Sensitivity

* **Most sensitive models:**

  * MLP (high sensitivity to learning rate, alpha)
  * SVM (sensitive to C and gamma)

* **Most stable models:**

  * Logistic Regression
  * KNN
  * Decision Trees

### Dataset Impact

* **Most sensitive datasets:**

  * Heart Disease
  * Breast Cancer

* **Most stable datasets:**

  * Wine Quality
  * Adult

### Hyperparameter Insights

* Highly sensitive:

  * Regularization parameters (e.g., C, alpha)
  * Learning rate (MLP)
* Less sensitive:

  * Solver choices
  * Activation functions

These trends show that **model complexity and dataset characteristics strongly influence tuning sensitivity**. 

## Results

Detailed experiment results, including sensitivity tables and plots, are available in the notebooks.

Key observations from the analysis:

* Linear and distance-based models are more stable
* Neural networks and kernel methods show high variability
* Larger datasets reduce performance variance


## How to Run

1. Clone the repository
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Run the notebooks in Jupyter/Colab

## Contributors

* Aditi Kedia
* Chahat Gupta

## Notes

This project was developed as part of a Machine Learning course and focuses on understanding robustness and tuning behavior rather than optimizing performance.
