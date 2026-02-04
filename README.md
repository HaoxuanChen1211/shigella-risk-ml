Predicting Childhood Diarrheal Risk in Bangladesh Using DHS Data
Overview

This project develops and evaluates machine-learning models to predict recent childhood diarrheal illness in Bangladesh using nationally representative Demographic and Health Survey (DHS) data. The analysis focuses on children under five years of age and integrates household water, sanitation, hygiene (WASH), socioeconomic, and demographic factors to assess their predictive contribution. The goal is methodological: to evaluate the extent to which commonly available household and contextual variables can support risk prediction for a relatively rare health outcome.

Data

·Source: Bangladesh Demographic and Health Survey (DHS), Children’s Recode (KR)

·Sample size: 8,784 children under five

·Outcome: Caregiver-reported diarrhea in the last two weeks

·Key features:

  ·Child age and sex

  ·Maternal education

  ·Household wealth index

  ·Water source and sanitation type

  ·Toilet sharing and water access characteristics

  ·Urban–rural residence and region

·Data are de-identified and accessed through the DHS Program under standard academic use conditions.

Methods

·Constructed a binary target variable for recent diarrhea, excluding “don’t know” responses

·Applied survey sampling weights to account for complex survey design

·Preprocessed data using median imputation for numeric variables and mode imputation with one-hot encoding for categorical variables

·Trained and compared:

  ·Regularized logistic regression (interpretable baseline)

  ·Random forest classifier (nonlinear baseline)

·Evaluated performance using ROC-AUC, precision–recall AUC, confusion matrices, and classification reports

Results

·Models achieved modest discrimination (ROC-AUC ≈ 0.63–0.64), indicating limited but non-random predictive signal

·Precision–recall performance was low (PR-AUC ≈ 0.07–0.08), reflecting the rarity of the outcome (~5% prevalence)

·Logistic regression improved sensitivity at the cost of precision, while the random forest favored majority-class accuracy at default thresholds

·Findings suggest that household WASH and socioeconomic variables alone are insufficient for high-precision prediction of diarrheal illness

Interpretation

This project highlights both the potential and the limitations of using cross-sectional household survey data for predictive modeling of rare health outcomes. While standard WASH and socioeconomic indicators contain some signal, stronger performance likely requires richer behavioral, environmental, or temporal data, as well as careful threshold selection aligned with public health use cases.


Tools

Python, pandas, scikit-learn, matplotlib
