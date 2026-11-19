# Multiple Linear Regression on California Housing

> Course: Programming for Descriptive and Predictive Analytics · Unit 03 · Semester 1

## Overview

A full multiple linear regression workflow on the 20,640-row California Housing dataset. The notebook connects theory and practice: assumptions of the linear model, ordinary least squares versus Ridge/Lasso/Elastic Net, exploratory analysis, multicollinearity checks, standardized fitting, inference with `statsmodels`, residual diagnostics and error metrics.

## Repository structure

- `notebooks/multiple-linear-regression.ipynb` - solved notebook with executed outputs and plots.

## Methods

- EDA with correlation heatmaps and distribution plots.
- Variance Inflation Factor (`statsmodels.stats.outliers_influence.variance_inflation_factor`) to diagnose multicollinearity.
- `StandardScaler` + `LinearRegression` from scikit-learn.
- `statsmodels.OLS` for coefficient p-values and confidence intervals.
- Residual Q-Q plot and normality testing; MSE, RMSE, MAE and R-squared.

## Results

After dropping `Latitude` and `Longitude`, the standardized model reaches **R-squared = 0.5397** and **RMSE = 0.7829**. Residuals show the usual departure from perfect normality expected for housing prices, which is discussed in the notebook.

## Data

The dataset is fetched at runtime with `sklearn.datasets.fetch_california_housing()`; no copyrighted or large data file is stored here. The first execution needs an internet connection.

## Requirements

`numpy`, `pandas`, `matplotlib`, `seaborn`, `scikit-learn`, `statsmodels`, `scipy` and `jupyter`.

## How to run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/multiple-linear-regression.ipynb
```

Saved outputs are kept as evidence of the executed experiment. They can be removed with `nbstripout` if a smaller history is preferred.

---
Author: Karla Maria Monroy Alvarez
