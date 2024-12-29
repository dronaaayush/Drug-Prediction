# Drug-Prediction
This project uses a Decision Tree Classifier to predict which of five drugs a patient might respond to, based on features like Age, Sex, Blood Pressure, Cholesterol, and Sodium-to-Potassium ratio (Na_to_K). It automates drug prescription, helping in the decision-making process using patient health data.


Drug Prescription Prediction Using Decision Tree Classifier

Overview

This project aims to predict the appropriate drug for a future patient based on their health profile using a machine learning model. The dataset consists of patients suffering from the same illness and contains features like Age, Sex, Blood Pressure, and Cholesterol. The target variable is the drug that each patient responded to, which is one of five possible drugs: Drug A, Drug B, Drug C, Drug X, and Drug Y.

A Decision Tree Classifier is used to predict which drug a new patient might respond to based on their features.

Dataset
The dataset contains the following features:
- Age: The age of the patient.
- Sex: The gender of the patient (Male or Female).
- Blood Pressure (BP): Blood pressure level (Low, Normal, or High).
- Cholesterol: Cholesterol level (Low or High).
- Na_to_K: Sodium-to-Potassium ratio in the blood.
- Drug: The drug the patient responded to (Drug A, Drug B, Drug C, Drug X, or Drug Y).

  
Objective
The goal of the project is to:
1. Train a multiclass classification model to predict the drug a patient might respond to based on their features.
2. Use a Decision Tree Classifier to build the model.
3. Evaluate the model's performance using accuracy and other classification metrics.
4. Predict drug prescriptions for new patients based on their health data.

   
Project Structure
- drug_prediction_model.ipynb : The main Python script that loads the dataset, preprocesses it, trains the Decision Tree model, and evaluates the model.
- predict.csv: The dataset containing the patient data.
- README.md: This file, providing an overview of the project.

  
Steps Involved
1. Data Preprocessing:
- Converted categorical variables (Sex, BP, Cholesterol, Drug) into numerical values using Label Encoding.
- Split the dataset into training and testing sets to evaluate the model's performance.

2. Model Training:
- Trained a Decision Tree Classifier on the preprocessed data.
- Used the train_test_split function to separate the data into a training set and a test set.

3. Model Evaluation:
- Evaluated the performance of the model on the test data using classification metrics such as accuracy, precision, recall, and F1-score.

4. Drug Prediction:
- Used the trained model to predict which drug a new patient might respond to, given their health data.

  
How to Run
1. Clone this repository to your local machine.
   ```bash
   git clone https://github.com/your-username/drug-prescription-prediction.git
   ```

2. Install the required libraries (if not already installed).
   ```bash
   pip install -r requirements.txt
   ```

3. Run the main script to train the model and make predictions.
   ```bash
   python drug_prediction_model.py
   ```

4. (Optional) Use the script to predict for a new patient by modifying the new_patient input in the code.
Example Output
After training the model, you will see a classification report with metrics such as precision, recall, and F1-score for each drug class.
For example, for a new patient with the following features:
- Age: 45
- Sex: Male
- Blood Pressure: High
- Cholesterol: High
- Na_to_K: 15.5

The model might predict the appropriate drug as:
```
Predicted drug for the new patient: Drug Y
```
Results
The model provides accurate predictions on the test dataset, with high accuracy and low error in classifying the appropriate drug for each patient.
The Decision Tree Classifier is a simple but effective model for multiclass classification in this scenario.
