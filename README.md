# Network Traffic Anomaly Detection

Anomaly detection system for network traffic using machine learning models, built as a part of the Bachelor of Technology final year project.

## Project Overview

As cyber-attacks become more complex, traditional rule-based Intrusion Detection Systems (IDS) often fail to detect sophisticated threats.  
This project builds an intelligent IDS using machine learning techniques, analyzing the **KDD Cup 1999** dataset to classify network connections as either normal or one of several attack types (DoS, Probe, R2L, U2R).

## Objectives
- Develop an ML-based Intrusion Detection System.
- Perform exploratory data analysis and feature engineering.
- Train and evaluate multiple ML models.
- Identify key features influencing detection.

## Dataset

- **Dataset:** [KDD Cup 1999 (10% Sample)](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)
- **Records:** ~494,021 entries
- **Features:** 41 input features + 1 target label
- **Classes:** Normal, DoS, Probe, R2L, U2R

## 🛠Preprocessing

- Missing Value Handling: None found
- Outlier Treatment: Capped at 99th percentile
- Feature Scaling: Min-Max Normalization
- Encoding: One-Hot Encoding for categorical features
- Feature Selection: Recursive Feature Elimination (RFE)

## Machine Learning Models Used

- Decision Tree
- Random Forest
- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Artificial Neural Network (MLPClassifier)

## Model Performance

| Model                | Accuracy | Precision | Recall | F1 Score |
|----------------------|----------|-----------|--------|----------|
| Random Forest        | 84.6%    | 0.84      | 0.85   | 0.84     |
| Decision Tree        | 82.7%    | 0.81      | 0.83   | 0.82     |
| Artificial Neural Network | 80.3% | 0.79    | 0.80   | 0.79     |
| Support Vector Machine | 77.8%  | 0.76      | 0.78   | 0.77     |
| Logistic Regression  | 75.4%    | 0.72      | 0.74   | 0.73     |

**Random Forest achieved the best results across all evaluation metrics.**

## Evaluation Metrics
- **Accuracy**  
- **Precision**  
- **Recall (Sensitivity)**  
- **F1 Score**  
- **Confusion Matrix**

## Key Observations
- Random Forest outperformed all other models.
- Feature engineering and preprocessing significantly boosted model performance.
- Class imbalance (especially R2L and U2R) affected detection precision.

## Future Improvements
- Apply SMOTE/ADASYN for handling class imbalance.
- Experiment with advanced models like XGBoost, LSTM, and Autoencoders.
- Deploy IDS for real-time monitoring using Flask API.
- Validate system using modern datasets (CIC-IDS2017, UNSW-NB15).

## 🛡References
- [KDD Cup 1999 Dataset](http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html)
- [GeeksforGeeks - IDS Using Machine Learning](https://www.geeksforgeeks.org/intrusion-detection-system-using-machine-learning-algorithms/)

