# Creditcard_Fraud_Detection

1. Introduction and Goal
•	Introduction:
o	The rapid growth of digital transactions has led to an increase in credit card fraud, posing significant financial risks to consumers and institutions. Effective fraud detection systems are essential to mitigate these risks.
o	This project leverages machine learning techniques to develop and evaluate models for detecting fraudulent transactions in a dataset of credit card transactions.
•	Goal:
o	The primary goal of this project is to build a robust credit card fraud detection system that can accurately identify fraudulent transactions.
o	To achieve this, multiple machine learning models will be trained and evaluated, with the best-performing model selected for deployment.

2. Dataset Overview
•	Dataset:
o	The dataset contains credit card transactions, including 284,807 rows and 31 columns, where each row represents a transaction and columns represent various attributes of the transaction, including a 'Class' column indicating fraud (1) or non-fraud (0).

3. Data Exploration
•	Top and Bottom Rows:
o	Displayed the first and last 5 rows to understand the data structure and contents.
•	Data Shape:
o	The dataset comprises 284,807 transactions (rows) and 31 attributes (columns).
•	Data Information:
o	All columns are numeric, with no missing values.

4. Data Preprocessing
•	Null Values:
o	Confirmed there are no null values in the dataset.
•	Feature Scaling:
o	Applied standard scaling to the 'Amount' column to normalize transaction amounts.
•	Duplicate Values:
o	Identified and removed 1,081 duplicate rows, resulting in 283,726 unique transactions.
•	Time Column:
o	Converted the 'Time' column from float to integer type for consistency.

5. Handling Imbalanced Data
•	Class Distribution:
o	Identified significant class imbalance with 283,253 non-fraudulent transactions and only 473 fraudulent transactions.
•	Undersampling:
o	Balanced the dataset by undersampling non-fraudulent transactions to match the number of fraudulent transactions, resulting in 946 transactions (473 fraud and 473 non-fraud).

6. Feature Matrix and Target Variable
•	Feature Matrix (X):
o	Extracted all columns except 'Class'.
•	Target Variable (Y):
o	Used the 'Class' column as the target variable.

7. Train-Test Split
•	Split the balanced dataset into training (80%) and testing (20%) sets to ensure the model is evaluated on unseen data.

8. Model Training and Evaluation
•	Logistic Regression (LR):
o	Achieved training accuracy: 94.18%
o	Test accuracy: 93.68%
o	Precision, Recall, and F1 scores for both training and test sets indicate good performance.
•	Decision Tree (DT):
o	Training accuracy: 94.18%
o	Test accuracy: 88.42%
o	Slightly lower performance compared to logistic regression.
•	Random Forest (RF):
o	Training accuracy: 100%
o	Test accuracy: 92.63%
o	Excellent performance on training data but slightly lower on test data due to potential overfitting.

9. Model Comparison
•	Compared the accuracy of the three models using a bar plot, highlighting logistic regression as the best-performing model for this dataset.

10. Model Deployment
•	Saving the Model:
o	Saved the logistic regression model using Joblib for future predictions.
•	Loading and Prediction:
o	Loaded the saved model and demonstrated a prediction, indicating whether a transaction is legitimate or fraudulent.

11. Conclusion
•	Successfully implemented and evaluated three machine learning models for credit card fraud detection.
•	Logistic regression model showed the best performance and was selected for deployment.
•	Future improvements could include exploring more advanced techniques for handling imbalanced data and incorporating additional features or data sources.

12. Future Work
•	Explore Advanced Techniques:
o	Implement more sophisticated methods like SMOTE (Synthetic Minority Over-sampling Technique) for balancing the dataset.
•	Feature Engineering:
o	Investigate new features that could improve model performance.
•	Model Optimization:
o	Fine-tune hyperparameters and explore other algorithms such as Gradient Boosting or Neural Networks.


