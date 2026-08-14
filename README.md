# Customer Churn Prediction System

## 📌 Project Overview
This project predicts whether a telecom customer is likely to churn (leave the service) using machine learning models trained on customer demographic, account, and service usage features.

## 🎯 Problem Statement
Customer retention is crucial for telecommunication companies. Acquiring new customers costs significantly more than retaining existing ones. The goal is to build an accurate classification pipeline to flag high-risk customers proactively.

## 📊 Dataset Description
- **Source**: [Telco Customer Churn Dataset (Kaggle)](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- **Rows**: 7,043 | **Columns**: 21
- **Key Features**: `tenure`, `Contract`, `MonthlyCharges`, `TotalCharges`, `InternetService`, `PaymentMethod`.

## 🛠️ Data Preprocessing & EDA Findings
1. **Cleaning**: Converted `TotalCharges` from string to numeric and imputed missing values using median.
2. **Encoding**: One-Hot Encoded categorical attributes and mapped binary target `Churn` (Yes=1, No=0).
3. **Class Balancing**: Applied **SMOTE** to handle the target class imbalance (approx 73% No Churn vs 27% Churn).
4. **Key EDA Insights**:
   - Month-to-month contract holders have the highest churn rate.
   - Customers with short tenure (<12 months) are significantly more vulnerable to churn.

## 🤖 Models Implemented & Performance
| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| **Logistic Regression** | ~75.2% | ~53.1% | ~78.5% | ~63.3% |
| **Random Forest Classifier** | ~78.6% | ~59.4% | ~64.2% | ~61.7% |

*Note: Random Forest demonstrated superior overall accuracy and balanced precision-recall score.*

## 🚀 How to Run locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/your-username/customer-churn-prediction.git](https://github.com/your-username/customer-churn-prediction.git)
   cd customer-churn-prediction