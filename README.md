# Fraud-Detection-Prediction-App

This project aims to build a machine learning model to detect fraudulent financial transactions, and deploy it using a user-friendly Streamlit web interface.

---

## 📌 Overview

### 🔎 Notebook: `analysis_model.ipynb`
A Jupyter Notebook that performs:

- **Data Exploration & Cleaning**: Reads and cleans the transaction dataset.
- **Visualization**: Uses seaborn/matplotlib to explore relationships between features and fraud, e.g.:
  - `Fraud Rate by Transaction Type`
    ![image](https://github.com/user-attachments/assets/d3115c2f-b356-48e9-86f6-ceaeb9449085)
  - Distribution of `amount` (log-transformed)
    ![image](https://github.com/user-attachments/assets/d1592193-8d77-4745-9037-1743e2fcdc78)
  - Boxplots of `amount` vs `isFraud`
    ![image](https://github.com/user-attachments/assets/37134167-bbeb-49df-9c01-4b1a36781adc)

- **Feature Engineering**: Transforms categorical and numerical variables.
- **Model Training**: Builds a machine learning pipeline using `RandomForestClassifier` or similar.
- **Model Export**: Saves the pipeline as `fraud_detection_pipeline.pkl` for use in the app.

---

### 💻 App: `app.py`
A simple Streamlit interface that:

- Takes user input for transaction details:
  - `type` (e.g. TRANSFER, CASH_OUT, etc.)
  - `amount`
  - `oldbalanceOrg`, `newbalanceOrig`
  - `oldbalanceDest`, `newbalanceDest`
- Loads the trained `.pkl` model
- Predicts whether the transaction is fraudulent
- Displays the result in a friendly way

---


