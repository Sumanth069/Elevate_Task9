**1. Introduction**



Credit card fraud is a major challenge in financial systems due to the high imbalance between legitimate and fraudulent transactions. Traditional accuracy-based evaluation fails in such scenarios, making it necessary to apply advanced machine learning techniques and appropriate evaluation metrics.



This project focuses on building a fraud detection system using Random Forest, an ensemble learning algorithm, and comparing its performance with a baseline Logistic Regression model.





**2. Dataset Description**



Dataset: Credit Card Fraud Detection Dataset (Kaggle)



Total Transactions: 284,807



Fraudulent Transactions: 492 (≈ 0.17%)



Legitimate Transactions: 284,315



Features:



V1 to V28: PCA-transformed numerical features



Amount: Transaction amount



Class: Target variable



0 → Legitimate transaction



1 → Fraudulent transaction



The dataset is highly imbalanced, which makes it suitable for studying real-world fraud detection problems.





**3. Data Preprocessing**



The following preprocessing steps were performed:



Loaded the dataset into Google Colab using Google Drive.



Checked for missing values in the target variable.



Identified 1 row with a missing target label (Class).



Removed rows with missing target labels, as supervised learning requires complete labels.



Separated features (X) and target (y).



Performed stratified train-test split to preserve fraud ratio:



80% training data



20% testing data





**4. Methodology**



**4.1** Baseline Model – Logistic Regression



A Logistic Regression model was trained as a baseline to:



Provide a reference point



Compare performance with an ensemble model



**4.2** Random Forest Classifier



Random Forest was chosen because:



It combines multiple decision trees (ensemble learning)



It handles non-linear patterns effectively



It reduces overfitting compared to single decision trees



Model Parameters:



n\_estimators = 100



random\_state = 42



n\_jobs = -1





**5. Evaluation Metrics**



Due to extreme class imbalance, accuracy was not used.



Instead, the following metrics were used:



Precision



Recall



F1-score



These metrics better reflect the model’s ability to correctly detect fraud.





**6. Results and Analysis**



**6.1** Logistic Regression (Baseline)



Performed reasonably on legitimate transactions



Lower recall for fraud cases



Missed several fraudulent transactions



**6.2** Random Forest



Achieved higher recall and F1-score for fraud detection



Better captured complex transaction patterns



Outperformed Logistic Regression across key metrics



**6.3** Feature Importance



Feature importance analysis revealed that a subset of PCA-transformed features contributed most to fraud detection, highlighting Random Forest’s ability to identify key indicators automatically.





**7. Model Persistence**



The trained Random Forest model was saved using joblib:



credit\_card\_fraud\_rf.pkl





This enables:



Model reuse



Deployment readiness



Future inference without retraining





**8. Conclusion**



This project successfully demonstrates:



Handling of highly imbalanced datasets



Use of stratified sampling



Comparison between baseline and ensemble models



Importance of proper evaluation metrics in fraud detection



Random Forest proved to be more effective than Logistic Regression in identifying fraudulent transactions, making it suitable for real-world fraud detection systems

