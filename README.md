# forest-biomass-estimation-ml
Integrating GEDI LiDAR and multisource remote sensing data with ensemble machine learning for aboveground biomass estimation in northeastern Bangladesh.


# Integrating GEDI LiDAR and Multisource Remote Sensing Data with Ensemble Machine Learning for Aboveground Biomass Estimation

## Overview

Monitoring forest aboveground biomass density (AGBD) is essential for understanding forest carbon stocks and supporting sustainable forest management. However, the effective integration of multisource remote sensing data and the application of advanced ensemble learning techniques remain underexplored in forest biomass estimation, particularly in Bangladesh. Furthermore, reliance on conventional validation approaches may lead to optimistic performance estimates following hyperparameter tuning. Addressing these gaps, this study develops an integrated framework combining GEDI LiDAR, Sentinel-1 SAR, Sentinel-2 optical imagery, and terrain information with machine learning, ensemble learning, nested cross-validation, and explainable AI (SHAP) to estimate AGBD across three northeastern forests of Bangladesh.

## Study Areas

The study focuses on three protected forest areas in northeastern Bangladesh:

- Lawachara National Park
- Satchari National Park
- Rema-Kalenga Wildlife Sanctuary

## Research Objectives
This study aims to develop a multisource remote sensing framework integrating optical, microwave, LiDAR, and terrain data with machine learning for AGBD estimation in protected forests of northeastern Bangladesh.  The specific objectives are to:
- Compare the predictive performance of five machine learning algorithms: Random Forest (RF), XGBoost (XGB), Support Vector Regression (SVR), LightGBM (LGBM), and CatBoost.
- Assess the contribution of multisource feature fusion to biomass estimation.
- Evaluate model robustness through nested five-fold cross-validation.
Additionally, seven ensemble learning strategies, comprising three linear averaging methods and four nonlinear stacking approaches, are benchmarked to investigate their potential to improve prediction accuracy.

## Data Sources and Predictors

Remote sensing datasets covering 2021–2023 were processed using Google Earth Engine (GEE).

Major data sources include:

- GEDI LiDAR: Relative height (RH95), canopy cover, and plant area index (PAI).
- Sentinel-2: Multispectral surface reflectance bands and vegetation indices.
- Sentinel-1: VV and VH backscatter.
- Terrain: Elevation and slope.

## Methodology

The workflow consists of:

1. Remote sensing data acquisition and preprocessing using Google Earth Engine.
2. Predictor extraction and dataset preparation.
3. Feature selection and multicollinearity assessment.
4. Machine learning model development and hyperparameter optimization.
5. Nested five-fold cross-validation.
6. Ensemble learning using averaging, optimized weighting, and stacking approaches.
7. Model evaluation and statistical comparison.
8. Model interpretation using SHAP.

## Machine Learning Algorithms

Five individual machine learning algorithms were evaluated:

- Random Forest (RF)
- CatBoost
- Extreme Gradient Boosting (XGBoost)
- LightGBM
- Support Vector Regression (SVR)

Ensemble approaches included simple averaging, inverse-MSE weighting, optimized weighted averaging, and stacking-based methods.

## Key Results

CatBoost achieved the best individual model performance:

- R² = 0.732
- RMSE = 32.51 Mg ha⁻¹

Simple Average Ensemble (SAE) and Inverse-MSE Weighted Ensemble (IMSE) achieved the highest reported ensemble performance:

- R² = 0.740
- RMSE = 32.01 Mg ha⁻¹

SHAP analysis identified relative height (RH95), canopy cover, and plant area index (PAI) among the most influential predictors.

Statistical evaluation using the Friedman test confirmed significant differences among model prediction errors (χ² = 106.878, p < 0.001).

## Repository Structure

- `notebooks/`: Research workflow and model development notebooks.
- `results/`: Model evaluation and statistical results.
- `figures/`: Selected research visualizations.
- `tables/`: Final performance and feature importance tables.
- `data/`: Sample or processed data, subject to data availability and redistribution permissions.

## Tools and Technologies

- Google Earth Engine
- Python
- Google Colab
- Scikit-learn
- CatBoost
- XGBoost
- LightGBM
- SHAP
- Pandas, NumPy, Matplotlib and Seaborn

## Reproducibility

The notebooks document the major stages of the research workflow. Input datasets and any required preprocessing steps should be configured before running the experiments.

## Research Scope

This repository documents the computational workflow, modelling approaches, and selected results of the aboveground biomass estimation study.

## Citation

If you use this work, please cite the associated research article when it becomes available.

**Status:** Research project / manuscript (update when published).
