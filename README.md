Credit Card Fraud Detection – Machine Learning Project

This repository presents a complete machine learning pipeline for detecting fraudulent credit card transactions. The project focuses on solving the problem of extreme class imbalance using SMOTE and evaluates multiple models with appropriate performance metrics.

The primary goal is to improve fraud detection by maximizing Recall and F1-score for the minority class, rather than relying on misleading accuracy values.

--------------------------------------------------

Problem Statement

Credit card fraud detection is a highly imbalanced classification problem where fraudulent transactions represent a very small fraction of total data. Traditional models tend to predict the majority class, leading to poor fraud detection.

This project addresses:
- Severe class imbalance
- High cost of false negative predictions
- Model evaluation using suitable metrics

--------------------------------------------------

Dataset Overview

The dataset contains anonymized credit card transactions.
Target variable:
Class 0 → Legitimate transaction
Class 1 → Fraudulent transaction

Fraud cases account for less than 1 percent of the total observations, making this a real-world imbalanced dataset.

--------------------------------------------------

Methodology

1. Data Exploration
Class distribution analysis using logarithmic scale visualization.
Comparison of transaction amounts between normal and fraudulent transactions.

2. Data Preprocessing
Train-test split with stratification to preserve class distribution.
Feature scaling applied where required.

3. Baseline Models
Logistic Regression
Random Forest Classifier

Models were first trained without imbalance handling to establish baseline performance.

4. Imbalanced Data Handling
SMOTE was applied only on the training set to generate synthetic samples for the minority class and avoid data leakage.

5. Model Training After SMOTE
Logistic Regression trained on scaled SMOTE data.
Random Forest trained on SMOTE data without scaling.

6. Evaluation and Comparison
Models evaluated using:
Confusion Matrix
Precision
Recall
F1-score

Final comparison focuses on the fraud class performance.

--------------------------------------------------

Models Used

Logistic Regression
Random Forest Classifier
SMOTE (Synthetic Minority Over-sampling Technique)

--------------------------------------------------

Evaluation Metrics

Recall and F1-score were prioritized due to the critical importance of detecting fraudulent transactions.
Accuracy was intentionally avoided as a primary metric.

--------------------------------------------------

Results Summary

SMOTE significantly improved Recall for the fraud class.
Logistic Regression achieved very high Recall but lower Precision.
Random Forest achieved a more balanced performance between Recall and F1-score.
False negatives were reduced substantially, which is essential in fraud detection systems.

--------------------------------------------------

Project Structure

creditcard.csv
fraud_detection.py
README.md
requirements.txt
.gitignore

--------------------------------------------------

How to Run

1. Install dependencies
pip install -r requirements.txt

2. Place the dataset file creditcard.csv in the project directory.

3. Run the Python script or notebook to train and evaluate the models.

--------------------------------------------------

Key Notes

SMOTE is applied only to the training data.
Feature scaling is used only for Logistic Regression.
The project emphasizes real-world evaluation metrics for imbalanced classification problems.

--------------------------------------------------

Author

Mohamed Terra
Computer Engineering – Data Science and Machine Learning
