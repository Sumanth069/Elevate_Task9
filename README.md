# Elevate_Task9

Credit card fraud detection is a critical real-world problem due to the extreme imbalance between legitimate and fraudulent transactions.
This project builds a machine learning model using Random Forest to detect fraudulent credit card transactions and compares its performance with a baseline Logistic Regression model.

# Objectives

Handle a highly imbalanced dataset

Build a baseline classification model

Train an ensemble learning model (Random Forest)

Evaluate models using appropriate metrics

Identify important features contributing to fraud detection

Save the trained model for reuse

# Dataset

Source: Kaggle – Credit Card Fraud Detection Dataset

Total Records: 284,807

Fraud Cases: 492 (≈ 0.17%)

Features:

V1 – V28: PCA-transformed numerical features

Amount: Transaction amount

Class: Target variable

0 → Legitimate

1 → Fraud

# Tools & Technologies

Python

Google Colab

Pandas, NumPy

Scikit-learn

Matplotlib

Joblib

# Methodology

Load dataset from Google Drive in Colab

Inspect data and handle missing target values

Perform stratified train-test split

Train Logistic Regression as a baseline model

Train Random Forest Classifier

Evaluate models using:

Precision

Recall

F1-score

Plot feature importances

Save the trained model using joblib

# Evaluation Metrics

Accuracy is not suitable due to class imbalance.
The following metrics are used instead:

Precision

Recall

F1-score

These metrics better represent fraud detection performance.

# Results

Logistic Regression provided a basic benchmark.

Random Forest achieved:

Better fraud detection capability

Higher recall and F1-score

Improved handling of non-linear patterns

Feature importance analysis highlighted key indicators of fraud.

# Model Saving

The trained Random Forest model is saved as:

credit_card_fraud_rf.pkl


This allows:

Model reuse

Faster inference

Deployment readiness

# How to Run (Google Colab)

Open Google Colab

Mount Google Drive

Place creditcard.csv in MyDrive

Run the notebook cells sequentially

Train the model and save .pkl file

# Output

<img width="1168" height="491" alt="Image" src="https://github.com/user-attachments/assets/3e15adb9-a22a-48c4-8f8b-c51126afe656" />

<img width="518" height="258" alt="Image" src="https://github.com/user-attachments/assets/0126a056-1588-47ad-8e9b-9cbf0493bf17" />

<img width="1095" height="715" alt="Image" src="https://github.com/user-attachments/assets/5c271900-dcac-4b9d-943b-eb404221a9e8" />
