# ML Titanic Survival Prediction

This project predicts whether a passenger survived the Titanic disaster based on their personal and travel information using machine learning techniques.  

---

## Project Overview
The goal of this project is to build a predictive model that can determine the likelihood of survival for Titanic passengers using features such as **age, sex, passenger class (Pclass), and port of embarkation (Embarked)**.  

The project includes data preprocessing, model building, evaluation, hyperparameter tuning, and final predictions on an unlabeled test set.  

---

## Dataset
- **Training Data:** Contains features and the target variable (`Survived`) indicating whether each passenger survived.  
- **Test Data:** Contains features only; the target variable is not provided.  

**Key features used:**
- **Numerical:** Age, Pclass  
- **Categorical:** Sex, Embarked  

---

## Steps Performed

### 1. Exploratory Data Analysis (EDA)
- Examined data distributions and missing values.  
- Visualized survival rates across different features (e.g., sex, Pclass).  
- Checked class imbalance.  

### 2. Data Preprocessing
- **Missing values:**  
  - Filled missing `Embarked` values with the most frequent value.  
  - Imputed missing `Age` values using predictive imputation (`IterativeImputer`).  
- **Encoding categorical features:**  
  - One-Hot Encoding for `Sex` and `Embarked`.  
- **Pipeline:**  
  - Constructed a preprocessing pipeline to handle numerical and categorical transformations consistently for both train and test data.  

### 3. Model Building
- Tested multiple models:  
  - Logistic Regression  
  - Random Forest  
  - XGBoost  
- Used **cross-validation** to ensure model robustness.  

### 4. Model Evaluation
- Evaluated models using:  
  - **Accuracy**  
  - **Precision**  
  - **Recall**  
  - **Confusion Matrix**  
- Selected the best-performing model based on cross-validation and evaluation metrics.  

### 5. Hyperparameter Tuning
- Performed **GridSearchCV** to optimize hyperparameters for each model.  
- Chose the final model with the highest cross-validation performance.  

### 6. Final Predictions
- Used the tuned model to predict survival for the unlabeled test dataset.  
- Generated a **submission file** suitable for Kaggle or further analysis.  

### 7. Feature Insights
- Examined **feature importance** to understand which attributes most influence survival.  
- Example insights:  
  - Females had a higher chance of survival.  
  - Passengers in higher classes (Pclass=1) were more likely to survive.  

---

## Tech Stack
- Python 3  
- Libraries: pandas, numpy, scikit-learn, XGBoost, matplotlib, seaborn  

---

