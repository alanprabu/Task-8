Phishing Website Detection Using SVM
Project Overview

This project implements a Machine Learning-based Phishing Website Detection System using a Support Vector Machine (SVM) classifier. The model is trained on the PhiUSIIL Phishing URL Dataset and predicts whether a website is phishing or legitimate based on various URL and website-related features.

Objective

The primary goal of this project is to:

Detect phishing websites using machine learning.
Train an SVM classification model on website feature data.
Evaluate model performance using common classification metrics.
Visualize results through a Confusion Matrix and ROC Curve.
Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
Dataset

Dataset: PhiUSIIL Phishing URL Dataset

The dataset contains website-related features and labels indicating whether a website is phishing or legitimate.

Data Preprocessing

The following preprocessing steps are performed:

Load the CSV dataset.
Remove records with missing labels.
Drop non-numeric and irrelevant columns:
URL
Domain
TLD
Title
Label
Convert target labels into binary values.
Replace infinite values with NaN.
Fill missing values using median values.
Select only numerical features for model training.
Model

The classifier used is:

Linear Support Vector Machine (LinearSVC)

Pipeline Components:

StandardScaler
LinearSVC

Model Parameters:

Python
LinearSVC(
C=1.0,
class_weight="balanced",
random_state=42,
max_iter=5000
)

The dataset is split into:

Training Set: 80%
Test Set: 20%
Evaluation Metrics

The model is evaluated using:

Confusion Matrix
Precision
Recall
F1-Score
ROC-AUC Score
Classification Report
Visualizations
Confusion Matrix

Displays the number of correctly and incorrectly classified phishing and legitimate websites.

ROC Curve

Illustrates the classifier's ability to distinguish between phishing and legitimate websites at different thresholds.

Project Structure
Plain Text
├── ML task 9.py
├── PhiUSIIL_Phishing_URL_Dataset.csv
└── README.md
How to Run
1. Install Dependencies
Shell
pip install pandas numpy matplotlib seaborn scikit-learn
2. Update Dataset Path

Modify the dataset path if necessary:

Python
df = pd.read_csv("PhiUSIIL_Phishing_URL_Dataset.csv")
3. Execute the Script
Shell
python "ML task 9.py"
Expected Output

The program produces:

Dataset summary
Class distribution
Trained SVM model
Confusion Matrix visualization
Precision, Recall, F1-Score, and ROC-AUC values
Classification Report
ROC Curve visualization
Learning Outcomes

Through this project, you will learn:

Data preprocessing techniques
Feature selection
Machine Learning classification with SVM
Model evaluation and performance metrics
Data visualization for classification models
