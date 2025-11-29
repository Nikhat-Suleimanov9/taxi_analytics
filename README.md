# Taxi Surge Pricing Prediction

Dataset source:
https://www.kaggle.com/datasets/arashnic/taxi-pricing-with-mobility-analytics

Workflow Summary

1. EDA
Missing value analysis
Distribution plots, boxplots, heatmaps
Chi-Square & ANOVA statistical tests
Correlation heatmaps
Gender independent from all main features
Type_of_Cab & Destination_Type strongly influence surge pricing

2. Preprocessing
Missing value handling
One-Hot Encoding for categorical data
Scaling
Stratified train/validation/test splits

3. Feature Engineering
Customer_Loyalty
Customer_Experience_Score
Trip_Efficiency_Score
Var_Mean (Var2, Var3)
All validated via ANOVA.

4.Modeling:

| Model                      | Accuracy            |
| -------------------------- | ------------------- |
| Dummy Classifier           | 43.1                |
| Logistic Regression (OvR)  | 68                  |
| Decision Tree              | 67                  |
| KNN                        | 66                  |
| Voting Classifier(OvR, DT, KNN) | 67.94             |
| **Neural Network (Keras)** | ⭐ **Best Model** ⭐  |

Architecture of NN:

Dense(32) → BN → ReLU
Dense(16) → BN → ReLU
Dense(8) → BN → ReLU
Dense(3) → Softmax


To run the project:
pip install -r requirements.txt
jupyter notebook taxi-pricing-project.ipynb


Deep learning performed best for surge pricing prediction, outperforming traditional ML models.
Feature engineering and proper preprocessing played a key role in improving accuracy.


