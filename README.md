# Taxi Surge Pricing Prediction

**Dataset source:**
https://www.kaggle.com/datasets/arashnic/taxi-pricing-with-mobility-analytics

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook taxi-pricing-project.ipynb
```

## Taxi Data Analytcs Report 
The detailed report can be found here: [Taxi Data Analytcs Report ]( https://docs.google.com/document/d/11oT2UQd1-iDaByhOLQb_IHUd7USbty1TcE12Aj7qU6U/edit?usp=sharing)

## Workflow Summary

### 1. EDA
-Missing value analysis<br>
-Distribution plots, boxplots, heatmaps<br>
-Chi-Square & ANOVA statistical tests<br>
-Correlation heatmaps<br>

Key finding:<br>
-**Gender** independent from all main features<br>
-**Type_of_Cab** & **Destination_Type** strongly influence surge pricing<br>

### 2. Preprocessing
-Missing value handling<br>
-One-Hot Encoding for categorical data<br>
-Scaling<br>
-Stratified train/validation/test splits<br>

### 3. Feature Engineering
-Customer_Loyalty<br>
-Customer_Experience_Score<br>
-Trip_Efficiency_Score<br>
-Var_Mean (Var2, Var3)<br>
-All validated via ANOVA.<br>

### 4. Modeling:

| Model                      | Accuracy            |
| -------------------------- | ------------------- |
| Dummy Classifier           | 43.1                |
| Logistic Regression (OvR)  | 67.78                  |
| Decision Tree              | 67.44                  |
| KNN                        | 66.48                  |
| Voting Classifier(OvR, DT, KNN) | 67.94             |
| **Neural Network (Keras)** | **68.34**  |

Architecture of NN:

Dense(32) → BN → ReLU<br>
Dense(16) → BN → ReLU<br>
Dense(8) → BN → ReLU<br>
Dense(3) → Softmax

Deep learning performed best for surge pricing prediction, outperforming traditional ML models. 
Feature engineering and proper preprocessing played a key role in improving accuracy. 

Additionally, this Neural Network model did not only achieve the highest score in my evaluation, but outperfomed all the other models from other public notebooks available on the Kaggle website 






