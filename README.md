🧠 Breast Cancer Prediction using Machine Learning
📌 Project Overview

This project demonstrates an end-to-end machine learning pipeline for predicting breast cancer diagnosis (Benign vs Malignant) using the Breast Cancer Wisconsin dataset.

It follows industrial best practices by:

Automating preprocessing with Pipelines
Handling missing values using SimpleImputer
Using Random Forest Classifier as a robust baseline
Saving & loading trained models using Joblib
Providing data visualization for interpretability
📦 Dependencies

Install the required Python packages before running the project:

pip install pandas numpy matplotlib scikit-learn joblib
📊 Dataset Information

Source: UCI Machine Learning Repository - Breast Cancer Wisconsin Dataset

🔢 Features (10)
ClumpThickness
UniformityCellSize
UniformityCellShape
MarginalAdhesion
SingleEpithelial CellSize
Bare Nuclei
BlandChromatin
NormalNucleoli
Mitoses
🎯 Target
2 = Benign
4 = Malignant
🔄 Workflow
1. Data Preparation
Convert raw data file to .csv with headers
Replace missing values (?) with NaN
Ensure numeric type conversion for all feature columns
2. Train-Test Split
Split into 70% training and 30% testing
Use stratified sampling to preserve class balance
3. Pipeline Construction
Step 1: SimpleImputer(strategy="median") for missing values
Step 2: RandomForestClassifier(n_estimators=300) for classification
4. Model Training & Evaluation
Metrics used:
Accuracy
Confusion Matrix
Classification Report
Feature Importance Plot shows most influential features
5. Model Saving & Loading
Save model using Joblib
Load model for future predictions without retraining
▶️ Running the Project
Step 1: Prepare CSV (Only Once)
from breast_cancer_pipeline import data_file_to_csv
data_file_to_csv()
Step 2: Train & Evaluate Model
python breast_cancer_pipeline.py
📈 Expected Output
Train Accuracy :: 1.0
Test Accuracy :: 0.97

Classification Report:
precision    recall    f1-score    support
...

Confusion Matrix:
[[...]]
Model saved to: bc_rf_pipeline.joblib
Loaded model prediction for first test sample: 2
📊 Visualizations
Feature Importance (Random Forest)
Confusion Matrix using Matplotlib
💾 Model Storage

The trained model is saved as:

bc_rf_pipeline.joblib
Load Model Example:
from breast_cancer_pipeline import load_model

model = load_model("bc_rf_pipeline.joblib")
🔮 Sample Prediction
sample = test_x.iloc[[0]]
pred = model.predict(sample)

print("Prediction:", pred[0])  
# Output: 2 (Benign) or 4 (Malignant)
👨‍💻 Author

Sanchit Ashok Kale
📅 Date: 01/05/2026
