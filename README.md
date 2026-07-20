🚢 Titanic Survival Prediction

A machine learning project that predicts passenger survival on the Titanic using the classic Kaggle Titanic dataset. The project covers exploratory data analysis, data cleaning, and a logistic regression model trained to classify survival outcomes.

📌 Overview

Using passenger data (class, sex, age, fare, family aboard, embarkation point), this project builds a binary classifier to predict whether a passenger survived the Titanic disaster. It's built as a single Jupyter notebook (Titanc_ML.ipynb) that can be run end-to-end in Google Colab or locally.

📊 Dataset
Source: Titanic - Machine Learning from Disaster (Kaggle)
Features used: Pclass, Sex, Age, SibSp, Parch, Fare, Embarked
Target: Survived (0 = did not survive, 1 = survived)
🔍 Exploratory Data Analysis
Checked for missing values across all columns
Visualized overall survival distribution
Compared survival by gender
Compared survival by passenger class
🧹 Data Cleaning & Preprocessing
Imputed missing Age values with the median
Imputed missing Embarked values with the mode
Dropped non-predictive columns: Name, Ticket, Cabin, PassengerId
One-hot encoded categorical features (Sex, Embarked)
Split data into training and test sets (80/20)
Standardized features using StandardScaler
🤖 Model
Algorithm: Logistic Regression (scikit-learn)
Train/test split: 80% train, 20% test (random_state=42)
📈 Results
Metric	Score
Accuracy	81.0%
Precision (Survived)	0.79
Recall (Survived)	0.74
F1-score (Survived)	0.76

Confusion Matrix:

	Predicted: No	Predicted: Yes
Actual: No	90	15
Actual: Yes	19	55

The model correctly classifies about 4 out of 5 passengers in the test set, performing slightly better at identifying non-survivors than survivors.

🛠️ Tech Stack
Python
pandas, numpy
matplotlib, seaborn
scikit-learn (LogisticRegression, StandardScaler, train_test_split, evaluation metrics)
opendatasets (for downloading the Kaggle dataset directly)
