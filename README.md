# Heart Disease Prediction

**Task Objective**
- Build a machine learning classifier to predict whether a patient has heart disease using clinical and diagnostic features. The notebook demonstrates preprocessing, exploratory data analysis (EDA), model training, and evaluation.

**Dataset Used**
- Source: `data/archive/heart.csv` (commonly known as the Cleveland Heart Disease dataset variant).
- Typical features: age, sex, chest pain type (`cp`), resting blood pressure (`trestbps`), cholesterol (`chol`), fasting blood sugar (`fbs`), resting ECG (`restecg`), maximum heart rate achieved (`thalach`), exercise-induced angina (`exang`), ST depression (`oldpeak`), slope, number of major vessels (`ca`), `thal`, and the target label `target` (0 = no heart disease, 1 = heart disease).
- Notes: The notebook inspects the data and reports no missing values in this CSV.

**Models Applied**
- Logistic Regression (primary model demonstrated).
- Evaluation metrics included: accuracy, precision/recall/F1 (classification report), confusion matrix, ROC curve and AUC.
- The notebook is structured so other classifiers (Random Forest, XGBoost, SVM, etc.) can be substituted easily.

**Key Results & Findings**
- Target distribution: the dataset in the notebook is relatively balanced between classes (similar counts of 0 and 1).
- Sex: heart disease appears more common in male patients in this dataset.
- EDA highlights: chest pain type (`cp`), maximum heart rate (`thalach`), exercise-induced angina (`exang`), and ST depression (`oldpeak`) show notable differences across `target` classes and are useful signals.
- Modeling: a Logistic Regression model is trained on standardized features; evaluation steps (accuracy, classification report, confusion matrix, ROC AUC) are included in the notebook. See the notebook for exact metric values and the feature importance (model coefficients) table.

**Reproduce / Run**
1. Create and activate a virtual environment (Windows PowerShell example):

```powershell
python -m venv venv
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
& "venv\Scripts\Activate.ps1"
```

2. Install required packages:

```powershell
pip install pandas numpy matplotlib seaborn scikit-learn jupyterlab
```

3. Launch Jupyter and run the notebook:

```powershell
jupyter lab
# open notebook/notebook/heart_disease_prediction.ipynb
```

4. All dataset files are under `data/archive/heart.csv`. Running the notebook cells in order reproduces the EDA, model training, and evaluation.

**Notes & Next Steps**
- To improve performance, try additional models (Random Forest, XGBoost), hyperparameter tuning, cross-validation, and feature engineering.
- Consider adding `requirements.txt` or a `conda` environment file for exact reproducibility.

---
Generated from the project notebook `notebook/heart_disease_prediction.ipynb`.
