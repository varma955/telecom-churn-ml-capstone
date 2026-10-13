# Telecom Customer Churn — Machine Learning Capstone

Open `telecom_churn_capstone.ipynb` in Jupyter Notebook. The modified dataset is in `data/`.

## Setup
Run this in a notebook cell or terminal:

```bash
pip install -r requirements.txt
```

Then choose **Kernel → Restart Kernel and Run All Cells**. The notebook includes regression (10 models), classification (10 models), clustering (2 algorithms), missing-value detection/imputation, IQR outlier detection/capping, model evaluation and visualizations.

The regression training cell handles missing/non-numeric target rows directly without a custom cleaning function. It does not fill target labels artificially.


## Streamlit prediction interface

This project now includes a simple web interface to predict customer churn. The app uses the included trained Random Forest model (`models/churn_model.joblib`).

### Run on Windows

1. Extract the ZIP file.
2. Open Command Prompt or PowerShell in the extracted project folder.
3. Install dependencies:
   ```bash
   python -m pip install -r requirements.txt
   ```
4. Start the interface:
   ```bash
   python -m streamlit run app.py
   ```
5. Your browser should open the local app. If not, open the local URL printed in the terminal (usually `http://localhost:8501`).

To retrain the interface model using the included dataset, run `python train_model.py` first. The interface is a demonstration and not a substitute for human review.
