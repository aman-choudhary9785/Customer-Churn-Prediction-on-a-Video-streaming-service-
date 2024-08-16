
## Observations
- Data doesn't contain any null values
- There is no significant correlation between the predictor columns
- No distinctions can be drawn for churned or non-churned customers on the basis of visualizations

## Approach
- Converted all categorical column values to integers using one-hot encoding
- Calculated mutual information for predictor variables with respect to Churn
- Spliited the model into training and testing sets and set out 20% data for making predictions
- Trained an XGBoost model on the training data with default hyperparams and got ROC-AUC score of 0.738
- Tuned the hyperparameters with Optuna and increased the ROC-AUC to 0.746
- Used the tuned model to make predictions on the test data and got a final score of 0.748
