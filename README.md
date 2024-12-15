# Parkinson’s Disease Telemonitoring Project

Parkinson's disease affects millions globally, with no definitive cure. This project aims to improve patient care by predicting the progression of Parkinson's disease based on voice data. 
It explores non-invasive methods for monitoring Parkinson’s disease progression through remote telemonitoring.
The dataset used in this study was collected from 42 patients over six months, including 16 biomedical voice measurements and demographic information (e.g., age, gender). 

## Dataset
- **Source**: The dataset comprises 5,875 voice recordings from telemonitoring devices used by patients in their homes.
- **Features**:
  - 16 biomedical voice measurements.
  - Patient demographics such as age and sex.
  - Time since recruitment (test_time).
- **Target Variable**: `Total_UPDRS` (Unified Parkinson's Disease Rating Scale score).
- **Preprocessing**:
  - Dropped redundant `Jitter` and `Shimmer` features based on correlation analysis.
  - Applied **One-Hot Encoding** for categorical variables.
  - Applied **Standardization** for continuous variables.

---

## Methods
### Data Splitting
- **Group-based splitting** to avoid data leakage across patients.
  - 80% for training and validation, 20% for testing.
  - Cross-validation with **GroupKFold**.

### Machine Learning Models
The following models were evaluated:
- **Linear Regression**
- **Random Forest**
- **Support Vector Machine (SVM)**
- **XGBoost**
- **K-Nearest Neighbors (KNN)**

### Evaluation Metric
- **Root Mean Squared Error (RMSE)**: Used to measure prediction accuracy.

Required library versions:

- python=3.10.5
- matplotlib=3.5.2
- pandas=1.4.2
- scikit-learn=1.1.1
- numpy=1.22.4
- xgboost=1.5.1
- shap=0.40.0
- jupyter_client=7.3.1
- jupyter_core=4.10.0
- jupyterlab=3.4.2
- jupyter_server=1.17.0
- jupytext=1.13.8
- rise=5.7.1
- plotly=5.8.0
- ipywidgets=7.7.0
