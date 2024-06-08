# README

## Project Overview

This repository contains the code in the study "Machine learning-based diagnostic prediction of minimal change disease: model development study." The study aims to develop predictive models to identify MCD among nephrotic syndrome patients based on demographic, blood test, and urine test variables. The original data is not shared, so please use the code with your data.

## Predictor Variables

Age, albumin, eGFR, T-chol, IgG, C3, Urine RBC, and UP/day were selected as predictors based on clinical insights and literature.

## Data Preprocessing

Missing values were addressed using multivariate imputation by chained equations (MICE). 

## Outcome Measures

Nephrologists and renal pathologists assigned the definitive diagnoses. MCD was labeled as 1, and other diagnoses were labeled as 0.

## Model Development and Evaluation

Five models were developed: TabPFN, LightGBM, Random Forest, Artificial Neural Network, and Logistic Regression. Bayesian optimization with stratified 5-repeated 5-fold cross-validation was used for hyperparameter tuning. Performance metrics included AUROC, AUPRC, and Brier score. Model calibration was evaluated using calibration plots, and clinical utility was assessed by decision curve analysis.

## Model Interpretations

The SHapley Additive exPlanations (SHAP) method was used to interpret the models, providing consistent and locally accurate attribution values for each predictor variable.

## Repository Structure

- `00_data_preprocessing.ipynb`: Code for the data preprocessing steps, including handling missing values using multivariate imputation by chained equations.
- `01_mode_development.ipynb`: Code for hyperparameter tuning using Bayesian optimization with stratified 5-repeated 5-fold cross-validation for all models.
- `02_model_evaluation.ipynb`: Code for internal validation of the models, including performance metrics calculation like AUROC, AUPRC, and Brier score.
- `03_model_interpretations.ipynb`: Code for interpreting the models using the SHAP method to provide attribution values for each predictor variable.
