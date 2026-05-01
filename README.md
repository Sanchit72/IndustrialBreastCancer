# IndustrialBreastCancer
Skip to content
Sanchit72
IndustrialBreastCancer
Repository navigation
Code
Issues
Pull requests
Agents
Actions
Projects
Wiki
Security and quality
Insights
Settings
Commit 6004a99
Sanchit72
Sanchit72
authored
8 minutes ago
Verified
Initial commit
main
0 parents  commit 
6004a99
1 file changed

+1
Lines changed: 1 addition & 0 deletions
File tree
Filter files…
README.md
Search within code
 
‎README.md‎
+1
Lines changed: 1 addition & 0 deletions


Original file line number	Diff line number	Diff line change
@@ -0,0 +1 @@
# IndustrialBreastCancer
1 commit comments
Comments
1
 (1)
Sanchit72 commented now
@Sanchit72
Sanchit72
now
Owner
Author
🧠 Breast Cancer Prediction using Machine Learning
📌 Overview

This project demonstrates an end-to-end Machine Learning pipeline for predicting breast cancer diagnosis (Benign vs Malignant) using the Breast Cancer Wisconsin dataset.

It follows industry best practices such as:

Automated preprocessing using Pipelines
Handling missing values with SimpleImputer
Using Random Forest Classifier as a robust baseline model
Model persistence using Joblib
Data visualization for better interpretability
🚀 Features
End-to-end ML pipeline implementation
Handles missing data effectively
High accuracy (~97% on test data)
Feature importance visualization
Model saving & loading for reuse
🛠️ Tech Stack
Python
Pandas
NumPy
Matplotlib
Scikit-learn
Joblib
📦 Installation

Install required dependencies:

pip install pandas numpy matplotlib scikit-learn joblib
📊 Dataset Information
Source: Breast Cancer Wisconsin Dataset (UCI ML Repository)
🔢 Features (10)
Clump Thickness
Uniformity of Cell Size
Uniformity of Cell Shape
Marginal Adhesion
Single Epithelial Cell Size
Bare Nuclei
Bland Chromatin
Normal Nucleoli
Mitoses
🎯 Target
2 → Benign
4 → Malignant
🔄 Workflow

Data Preparation
Convert raw dataset to .csv format
Replace missing values (?) with NaN
Convert all features to numeric types
Train-Test Split
70% Training / 30% Testing
Stratified sampling for balanced classes
Pipeline Construction
Step 1: SimpleImputer(strategy="median")
Step 2: RandomForestClassifier(n_estimators=300)
Model Training & Evaluation
Accuracy Score
Confusion Matrix
Classification Report
Model Persistence
Save model using Joblib
Load model for future predictions
▶️ Running the Project
Step 1: Prepare CSV (Run once)
from breast_cancer_pipeline import data_file_to_csv
data_file_to_csv()
Step 2: Train & Evaluate Model
python breast_cancer_pipeline.py
📈 Expected Output
Train Accuracy :: 1.0
Test Accuracy :: 0.97
Classification Report:
precision recall f1-score support
...

Confusion Matrix:
[[...]]
Model saved as: bc_rf_pipeline.joblib
Example Prediction: 2 (Benign) or 4 (Malignant)
📊 Visualizations
Feature Importance Plot (Random Forest)
Confusion Matrix Visualization
💾 Model Storage

Saved model file:

bc_rf_pipeline.joblib
Load Model Example:
from breast_cancer_pipeline import load_model

model = load_model("bc_rf_pipeline.joblib")
🔮 Sample Prediction
sample = test_x.iloc[[0]]
pred = model.predict(sample)

print("Prediction:", pred[0])

Output: 2 (Benign) or 4 (Malignant)
👨‍💻 Author

Sanchit Ashok Kale
📅 Date: 01 May 2026

Comment
You're receiving notifications because you're subscribed to this thread.

