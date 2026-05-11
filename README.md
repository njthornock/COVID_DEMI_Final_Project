# COVID-19 Risk Prediction Using Patient-Reported Data and Causal Analysis

## About the Project

This repository contains my final project for HAP 823: Causal Analysis & Comparative Effectiveness. The project uses the COVIDCARE patient dataset and the DEMI knowledgebase to estimate the risk of PCR-confirmed COVID-19 using patient-reported symptoms, home-testing information, and causal/temporal ordering.

The project was completed entirely in Python using a Jupyter notebook.

## Repository Contents

- `notebooks/COVID_DEMI_Final_Project.ipynb`  
  Main Jupyter notebook containing the full project workflow.

- `data/COVIDCARE_FORSUBMISSION_MIT_CLEANED_Phase_II_2021-12-03.csv`  
  COVIDCARE patient dataset used for analysis and prediction modeling.

- `data/COVIDCARE_DEMI_knowledgebase_v4.csv`  
  DEMI knowledgebase file used to analyze relationships between variables.

- `requirements.txt`  
  Python libraries needed to run the notebook.

## Project Workflow

The notebook includes the following steps:

1. Loading the COVIDCARE patient dataset and DEMI knowledgebase
2. Creating an analytic dataset with known PCR results
3. Assigning variables to temporal tiers
4. Applying temporal rules to the DEMI knowledgebase
5. Calculating association measures
6. Preparing model-ready data
7. Creating interaction terms from symptom and home-testing variables
8. Comparing logistic regression, LASSO logistic regression, and gradient boosting
9. Creating an interactive COVID prediction function

## Results Summary

The original dataset included 822 patient records and 472 variables. After excluding records with missing PCR results, the analytic dataset included 559 patients: 501 PCR-negative cases and 58 PCR-positive cases.

Three models were compared: logistic regression, LASSO logistic regression, and gradient boosting. Gradient Boosting performed best overall, with the highest accuracy and ROC AUC and the lowest log loss.

The final notebook includes a simple interactive prediction function that allows a user to select a patient record from the test set and return the predicted probability of PCR-confirmed COVID-19, the predicted class, and the actual PCR result.

## Notes

This project is a notebook-based demonstration for a course assignment. It is not intended to replace clinical judgment, diagnostic testing, or medical evaluation.

## Author

Natalie Thornock  
George Mason University  
Spring 2026
