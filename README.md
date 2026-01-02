# Predicting Severe Flu After Vaccination

## Overview
This project builds and evaluates machine learning models to predict severe flu
within six months of vaccination in a cohort of 1,000 patients. Multiple classification
approaches were considered, including logistic regression, boosting, and support vector
machines with linear and radial kernels.

Model performance was assessed using area under the ROC curve (AUC) with 10-fold
cross-validation, balancing predictive accuracy and interpretability.

## Data
- **Source:** Columbia University (P8106: Data Science II course materials)
- **Sample size:** 1,000 patients
- **Response variable:** Severe flu incidence within six months of vaccination (binary)
- **Predictors:** Demographic variables, smoking history, BMI, comorbidities
  (diabetes, hypertension), blood pressure, and LDL cholesterol

## Methods
- Data preprocessing and exploratory analysis in R
- Feature distribution analysis and response balance checks
- Supervised classification models: logistic regression, boosting, and SVMs
- Model comparison using cross-validated AUC

## Results
- Support vector machines with a linear kernel achieved the highest AUC, though
  performance differences across models were modest
- Logistic regression was selected as the final model to prioritize interpretability
  with minimal loss in predictive performance
- Current smoking status and higher BMI were associated with increased risk of severe flu

Selected visualizations are available in the accompanying PDF report and the `output/` directory.

## Limitations and Future Work
- Severity criteria for flu outcomes are imprecisely defined
- Lack of timing information between vaccination and infection may limit predictive power
- Future work could incorporate time-to-event modeling and additional clinical features

## Reproducibility
All analyses were conducted in R. The R Markdown file contains code to preprocess the data,
train models, and evaluate performance using the `caret`, `kernlab`, and `ggplot2` packages.
