Energy Efficiency Analysis: Building Load Prediction

An end-to-end Machine Learning study comparing various regression algorithms to predict Heating Load and Cooling Load in residential buildings based on architectural geometry.
Dataset Source

The study utilizes the Energy Efficiency Dataset from the UCI Machine Learning Repository.

    Link: UCI Energy Efficiency Dataset

    Citation: Tsanas, A., & Xifari, A. (2012). Accurate quantitative estimation of energy performance of residential buildings.

Project Overview

Predicting energy demand early in the design phase allows architects to optimize buildings for sustainability. This project benchmarks seven different models to find the most reliable estimator for thermal loads.
Features (8 Building Parameters):

    Relative Compactness, Surface Area, Wall Area, Roof Area, Overall Height, Orientation, Glazing Area, Glazing Area Distribution.

Target Variables:

    y1: Heating Load (kWh/m^2)

    y2: Cooling Load (kWh/m^2)

Technical Implementation

    Preprocessing: Feature scaling via StandardScaler.

    Models Evaluated: Linear Regression, Ridge, Lasso, k-Nearest Neighbors, Random Forest, Decision Tree, and Gradient Boosting.

    Evaluation Metrics: R2 Score, Mean Absolute Error (MAE), and Root Mean Squared Error (RMSE).

Key Results
## Model Performance Benchmarks

## Target Comparison ($R^2$ Scores)

| Algorithm | Heating ($R^2$) | Cooling ($R^2$) |
| :--- | :---: | :---: |
| Gradient Boosting | **0.981** | **0.981** |
| k-Nearest Neighbors | 0.935 | 0.935 |
| Linear Regression | 0.907 | 0.907 |
| Random Forest | 0.906 | 0.906 |
| Decision Tree | 0.520 | 0.520 |

The study identifies Overall Height and Relative Compactness as the primary drivers of energy demand.
Conclusions

    Model Accuracy: Gradient Boosting is the most effective model for this dataset, capturing complex non-linear interactions that linear models missed.

    Structural Impact: Building height and compactness have a far greater impact on energy load than orientation or glazing distribution.

    Model Stability: The significant failure of the single Decision Tree (R2≈0.49) compared to Random Forest (R2≈0.90) highlights the importance of using Ensemble Methods for building energy data.

Requirements

To reproduce this study, install the following dependencies:
Bash

      pip install pandas numpy scikit-learn matplotlib seaborn joblib jupyter

License

This project is licensed under the MIT License - see the LICENSE file for details.
