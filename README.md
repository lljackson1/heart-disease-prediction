# Heart Disease Prediction Analysis
**Tools:** R, RMarkdown | **Course:** S&DS 2300 Data Analysis, Yale University (Spring 2026)

## Overview
This project analyzes clinical data from 746 patients across five international medical 
institutions to identify predictors of heart disease. The analysis covers the full 
statistical workflow from data cleaning and exploratory analysis through regression 
modeling and binary logistic regression.

## Dataset
The Heart Failure Prediction Dataset was sourced from 
[Kaggle](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction) 
(fedesoriano, 2021). It contains 12 clinical variables including age, sex, chest pain 
type, resting blood pressure, cholesterol, and maximum heart rate.

## Methods
- **Data Cleaning:** Identification and removal of physiologically impossible values 
(cholesterol and RestingBP of 0), factor conversion
- **Descriptive Analysis:** Histogram, boxplot, and scatterplot with fitted regression lines
- **Basic Tests:** Pearson correlation, Welch t-test, bootstrap confidence intervals, 
permutation test
- **Multiple Regression:** Manual backwards stepwise selection with Box-Cox 
transformation analysis and residual diagnostics
- **Binary Logistic Regression:** Manual backwards stepwise selection with odds ratio 
interpretation and deviance analysis

## Key Findings
- Exercise-related clinical measurements (MaxHR, ST slope, exercise-induced angina) 
were among the strongest predictors of both maximum heart rate and heart disease presence
- Male patients had approximately 6 times the odds of heart disease compared to female 
patients (OR = 6.00, p < 0.001)
- Asymptomatic chest pain was associated with significantly higher odds of heart disease 
compared to all other chest pain types, consistent with known clinical patterns
- The final logistic regression model achieved substantial improvement over the null 
model (deviance reduction: 1032 → 491, AIC = 510)

## Files
- `2300HeartDiseaseProject.Rmd` — Full analysis in RMarkdown
- `heart.csv` — Raw dataset
- `2300HeartDiseaseProject.pdf` — Knitted report

## Requirements
R packages used: `ggplot2`, `car`, `MASS`, `questionr`
