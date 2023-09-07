# Credit Card Fraud Detection

## Objective
Detect credit card fraud using machine learning techniques and evaluate model performance on an imbalanced dataset.

## Data Source
The dataset used for this project is sourced from Kaggle. You can access it [here](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud).
 

The dataset is highly imbalanced between legitimate and fraudulent transactions. The dataset consists of:
- Legitimate Transactions: 284,315
- Fraudulent Transactions: 492

## Data Preprocessing and Data Exploration
- Checked for Null Values
- Countplot
- Correlation and Heatmap
- Statistical Summary
- Feature Scaling
- Splitting the Dataset into Train and Test Data

## Methodology
### Algorithms Used
1. Logistic Regression
2. Random Forest Classifier
3. XG Boost Classifier
4. XG Boost Classifier (WITH SMOTE Oversampling)

### Results (Without Resampling)
| Model                | Accuracy | F1 Score | Precision | Recall | ROC-AUC Score |
|----------------------|----------|----------|-----------|--------|---------------|
| Logistic Regression  | 0.999192 | 0.735632 | 0.876712  | 0.6337 | 0.816753      |
| Random Forest        | 0.999491 | 0.844920 | 0.918605  | 0.7822 | 0.891028      |
| XG Boost             | 0.999614 | 0.884211 | 0.943820  | 0.8317 | 0.915798      |

### Results (With SMOTE Resampling)
| Model                | Accuracy | F1 Score | Precision | Recall | ROC-AUC Score |
|----------------------|----------|----------|-----------|--------|---------------|
| XG Boost (with SMOTE)| 0.999403 | 0.833333 | 0.825243  | 0.8416 | 0.920634      |

## Conclusion
When dealing with an imbalanced dataset, applying SMOTE oversampling improved ROC-AUC Score but led to a significant decrease in precision. The XG Boost model without resampling provided the most balanced performance for credit card fraud detection in this scenario.

