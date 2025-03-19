# Credit Risk Classification Report

## Overview of the Analysis

In this analysis, I evaluated the performance of various machine learning models to classify credit risk in a dataset. The goal was to predict whether an applicant for credit would be classified as a "high-risk" or "low-risk" customer, indicating whether they are likely to default on a loan or not.

- **Target variable:**
  - `0` for low-risk customer (no default).
  - `1` for high-risk customer (default).
  
### Variables and Data

- **Target variable:** The financial risk classification of customers (either `0` for low-risk or `1` for high-risk).
- **Features:** The dataset contained various features such as income, credit history, loan amount, etc.
- **Value counts:** There was an imbalance in the target variable, with more low-risk (`0`) than high-risk (`1`) cases.

### Machine Learning Process

1. **Data Preprocessing:**
   - Handled missing values, scaled numerical features, and encoded categorical variables.
   
2. **Model Selection:** 
   - Used `Logistic Regression` for classification.
   
3. **Model Training:** 
   - Split the dataset into training and testing subsets. The model was trained using the training set and evaluated using cross-validation.
   
4. **Model Evaluation:** 
   - Evaluated the model based on metrics such as accuracy, precision, recall, and F1-score.
   
5. **Model Tuning:**
   - Optimized hyperparameters to improve performance.

### Algorithms Used:

- **Logistic Regression:** A simple and interpretable model suitable for binary classification tasks.

---

## Results

### Logistic Regression Model

- **Accuracy:** 99.26%
- **Precision (class 0):** 1.00
- **Recall (class 0):** 0.99
- **F1-Score (class 0):** 1.00
- **Precision (class 1):** 0.84
- **Recall (class 1):** 0.94
- **F1-Score (class 1):** 0.89
- **Macro Avg Precision:** 0.92
- **Macro Avg Recall:** 0.97
- **Macro Avg F1-Score:** 0.94
- **Weighted Avg Precision:** 0.99
- **Weighted Avg Recall:** 0.99
- **Weighted Avg F1-Score:** 0.99

The logistic regression model showed a high accuracy score of 99.26%, indicating that the model correctly classified the majority of customers. However, while the precision for the low-risk class (`0`) was perfect at 1.00, the precision for the high-risk class (`1`) was lower at 0.84. This suggests that the model is more likely to classify high-risk customers as low-risk, despite performing well in recall for the high-risk class (0.94).

---

## How Well Does the Logistic Regression Model Predict Both the `0` (Healthy Loan) and `1` (High-Risk Loan) Labels?

**Answer:**  
The logistic regression model excels at predicting healthy loans (`0`) with near-perfect accuracy and performs well on high-risk loans (`1`), though precision (84%) slightly lags behind recall (94%). While it effectively identifies high-risk loans, there’s room to reduce false positives. Overall, the model is highly effective with strong accuracy and recall.

---

## Summary

The Logistic Regression model performed excellently in terms of overall accuracy, but there are some key trade-offs in precision and recall for the different classes. While the recall for the high-risk class is relatively high (0.94), the precision is lower at 0.84, indicating a higher number of false positives for the high-risk class. This could potentially be problematic in a real-world scenario where accurately identifying high-risk customers (minimizing false negatives) is crucial.

### Recommendation:
- **Best Model:** The Logistic Regression model performs very well in terms of overall accuracy and recall for the high-risk class, but for better performance, I would consider using models like Random Forest or XGBoost to achieve better precision for the high-risk class.
  
If minimizing false positives in the high-risk class is critical, further tuning of the model or experimenting with other algorithms might be required to find a better balance between precision and recall.

---

## Conclusion

The logistic regression model demonstrates solid performance in classifying credit risk, but there is still room for improvement, particularly in reducing false positives for high-risk customers. Future work could focus on exploring additional algorithms like Random Forest and XGBoost for better precision and recall balance.
