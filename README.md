# Azubi_assessment-Esther

This project is a complete end-to-end machine learning solution developed to predict whether a client will subscribe to a term deposit based on their personal, financial, and campaign-related attributes. The solution was built using Python, trained and evaluated in Google Colab, and deployed using Streamlit Cloud for real-time prediction.

## Project Overview
-Dataset:bank-additional-full

- Goal:Predict if a client will subscribe (`yes` or `no`) to a term deposit (`y` column).

- Type: Binary classification problem.

- Model Deployed: Random Forest Classifier (after evaluating multiple models).

- Web App: Built using Streamlit to allow users to input client data and get instant predictions.


## Project Structure

project-root/

│

app.py # Streamlit app script
preprocessing.py # Data preprocessing script
modeling.py # Model training & evaluation
random_forest_model.pkl # Trained model (joblib serialized)
scaler.pkl # Scaler used on numerical inputs
model_columns.pkl # Model column structure for input formatting
requirements.txt # Python dependencies for deployment
README.md # Project summary and documentation

### Key Steps
#### 1. Exploratory Data Analysis (EDA)

- Analyzed the target distribution and class imbalance.

- Visualized correlations and category-wise behavior.

- Investigated patterns across job, marital status, education, housing, etc.

#### 2. Data Preprocessing

- One-hot encoded categorical variables.

- Scaled numerical features using `StandardScaler`.

- Split data into training and test sets.

- Addressed class imbalance using `SMOTE` for training set only.


#### 3. Modeling

- Tested multiple models: Logistic Regression, Random Forest, etc.

- Chose Random Forest for its better balance of performance and interpretability.

- Evaluated using: Accuracy, Precision, Recall, F1-score, ROC-AUC.

- Used original imbalanced test set to reflect real-world performance.


#### 4. Deployment

- Saved model using `joblib`.

- Built a user-friendly interface with Streamlit.

- Deployed the app on Streamlit Cloud.


## How to Use the App

Visit the deployed app here (https://azubiassessment-esther-vejg9vmgle3aa6esc74g79.streamlit.app/)

### Steps:

1. Enter client details such as age, duration of call, campaign contacts, etc.

2. Click "Predict".

3. Get an instant prediction on whether the client is likely to subscribe.


## Requirements to run locally:
```bash

pip install -r requirements.txt

streamlit run app.py
