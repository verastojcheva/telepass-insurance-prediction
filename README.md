# Telepass Insurance Purchase Prediction

This project builds and compares three binary classification models:
- Logistic Regression
- Decision Tree
- Random Forest

The goal is to predict whether a customer will purchase an insurance policy after receiving a quote using the Telepass dataset.

## Approach
All available features are used. Preprocessing includes:
- encoding categorical variables
- converting date variables into numeric features
- imputing missing values
- scaling features for logistic regression

## Evaluation
Models are evaluated using:
- Log-loss (primary metric, since probability quality is important)
- ROC-AUC (ranking performance)
- Accuracy (secondary metric)

A 5-fold stratified cross-validation is used to ensure reliable out-of-sample evaluation.

## Results
- Logistic Regression achieved the lowest log-loss (best calibrated probabilities)
- Random Forest achieved the highest ROC-AUC (best ranking performance)
- Decision Tree performed worst due to overfitting

## Files
- `Telepass_Insurance_Prediction_Notebook.ipynb` – full analysis, models, and results
- `Telepass.xlsx` – dataset

## Conclusion
Random Forest is the preferred model for this task, as it captures non-linear relationships and provides better ranking of customers by purchase likelihood. Logistic Regression remains useful when well-calibrated probabilities are required.

## Note
Dataset provided as part of course assignment.
