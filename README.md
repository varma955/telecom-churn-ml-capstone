# Telecom Customer Churn Prediction Using Machine Learning

## Project Overview

This project uses machine learning techniques to analyse telecom customer data, predict customer churn, and identify patterns in customer behaviour.

Customer churn occurs when a customer stops using a company's services. Predicting churn can help telecom companies identify customers who may leave and make better customer-retention decisions.

The project includes data preprocessing, exploratory data analysis, regression, classification, clustering, model evaluation, visualisations, and a Streamlit web interface for churn prediction.

## Objectives

- Analyse telecom customer data and identify useful patterns.
- Handle missing values and detect and manage numerical outliers.
- Implement and compare multiple machine learning algorithms.
- Predict customer churn using classification models.
- Predict monthly charges using regression models.
- Group similar customers using clustering.
- Present churn predictions through a simple web interface.

## Technologies Used

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Visualisation:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Notebook Environment:** Jupyter Notebook
- **Web Interface:** Streamlit
- **Model Storage:** Joblib

## Machine Learning Algorithms

The capstone notebook includes the following algorithm groups:

| Task | Number of algorithms | Purpose |
|---|---:|---|
| Regression | 10 | Predict monthly charges |
| Classification | 10 | Predict customer churn |
| Clustering | 2 | Group similar customers |

The algorithms are trained and evaluated using suitable metrics to compare their performance.

## Dataset

The project uses the modified Telco Customer Churn dataset stored in the `data/` directory.

The dataset contains customer and service information, including tenure, contract type, payment method, monthly charges, and churn status.

The modified dataset includes missing values and numerical outliers for demonstrating data-cleaning techniques.

**Target variables:**
- `MonthlyCharges` — regression target.
- `Churn` — classification target.

Clustering is performed without using the churn labels during training.

## Project Structure

```text
telecom-churn-ml-capstone/
│
├── data/
│   └── WA_Fn-UseC_-Telco-Customer-Churn_with_missing_outliers.csv
│
├── models/
│   └── churn_model.joblib
│
├── telecom_churn_capstone.ipynb
├── app.py
├── train_model.py
├── requirements.txt
└── README.md
```

*Note: The files shown above should match the files actually present in your repository.*

## Installation and Setup

### 1. Download or clone the repository

```bash
git clone https://github.com/varma955/telecom-churn-ml-capstone.git
cd telecom-churn-ml-capstone
```

Alternatively, download the repository as a ZIP file and extract it.

### 2. Install the dependencies

Open a terminal in the project folder and run:

```bash
python -m pip install -r requirements.txt
```

### 3. Open the Jupyter Notebook

Run:

```bash
python -m notebook
```

Open `telecom_churn_capstone.ipynb` in Jupyter Notebook.

### 4. Run the notebook

Select **Kernel → Restart Kernel and Run All Cells**.

Run the cells from top to bottom to load the dataset, preprocess the data, train the models, evaluate their performance, and generate the visualisations.

Ensure that the dataset path in the notebook matches the location of your CSV file.

## Data Preprocessing

The notebook demonstrates the following preprocessing steps:

- Inspecting the dataset structure and data types.
- Detecting missing values and applying suitable imputation.
- Detecting numerical outliers using the Interquartile Range (IQR) method.
- Capping outliers where appropriate.
- Encoding categorical features.
- Scaling numerical features where required.
- Splitting the data into training and testing sets.
- Using preprocessing pipelines to keep transformations consistent.

Missing or non-numeric regression target values are handled without artificially filling in target labels.

## Model Evaluation

Different metrics are used for each machine learning task.

### Regression

- R-squared (R²)
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)

### Classification

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- ROC-AUC

### Clustering

- Silhouette Score
- Davies–Bouldin Index
- Calinski–Harabasz Score

The results help compare algorithms and understand their strengths and limitations.

## Streamlit Prediction Interface

The project includes a simple Streamlit web interface for predicting customer churn. The interface uses the trained Random Forest model stored at `models/churn_model.joblib`.

### Run on Windows

**Step 1:** Open Command Prompt or PowerShell in the project folder.

**Step 2:** Install the dependencies:

```bash
python -m pip install -r requirements.txt
```

**Step 3:** Start the application:

```bash
python -m streamlit run app.py
```

**Step 4:** Open the local URL displayed in the terminal. It is usually:

```text
http://localhost:8501
```

### Retrain the prediction model

To retrain the model using the included dataset, run:

```bash
python train_model.py
```

Make sure the dataset path and required dependencies are configured correctly before running the script.

## Expected Outcomes

- A cleaned and analysed telecom customer dataset.
- Comparative results for regression, classification, and clustering algorithms.
- Visualisations that help explain customer patterns and model performance.
- A trained Random Forest churn model for the Streamlit interface.
- A practical demonstration of machine learning applied to telecom customer data.

## Future Improvements

- Improve model performance through hyperparameter tuning.
- Add more customer behaviour features.
- Improve the interface with clearer prediction explanations.
- Deploy the application to a cloud platform.
- Monitor model performance on new customer data.

## Disclaimer

This project is developed for academic and educational purposes. Model predictions are estimates and should not be treated as guaranteed outcomes or used as the sole basis for customer-related decisions.

## Author

**Machine Learning Capstone Project**

GitHub Repository: https://github.com/varma955/telecom-churn-ml-capstone
