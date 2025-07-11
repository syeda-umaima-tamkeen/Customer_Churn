# Predicting Customer Churn Using Machine Learning

**Project by:** Syeda Umaima Tamkeen

## 📝 Summary

In this project, I developed a classification model to **predict customer churn** based on usage patterns and demographics. The objective was to determine whether a customer will leave the service, helping businesses proactively retain valuable customers.

I implemented **Logistic Regression**, **Random Forest**, and **Gradient Boosting** models. After hyperparameter tuning, the **Random Forest** model achieved high performance and provided actionable insights for churn prediction.

---

## 🔍 Key Steps

### 1. Data Exploration
- Loaded and analyzed a dataset with customer demographic and usage features.
- Visualized distributions of churners and non-churners.
- Explored relationships between features like `MonthlyCharge`, `DayMins`, and churn.

### 2. Data Preprocessing
- Handled missing values.
- Converted categorical variables (e.g., `ContractRenewal`, `DataPlan`) using one-hot encoding.
- Standardized continuous features like `DataUsage` and `OverageFee`.

### 3. Feature Engineering
- Applied `StandardScaler` to continuous variables.
- Generated new insights from customer service call data and other predictors.

### 4. Model Training
- Trained and compared three models:
  - Logistic Regression
  - Random Forest
  - Gradient Boosting
- Used an 80/20 train-test split for evaluation.

### 5. Model Evaluation
- Evaluated models using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - AUC-ROC Score
- **Best Model:** Random Forest
  - Accuracy: **93.1%**
  - Precision (Churn=1): **88%**
  - Recall (Churn=1): **63%**
  - F1-Score (Churn=1): **0.74**
  - AUC-ROC Score: **0.93**

---

## ⚙️ Model Fine-Tuning

Used `GridSearchCV` to tune Random Forest hyperparameters:

| Parameter           | Value |
|---------------------|--------|
| n_estimators         | 200    |
| max_depth            | 30     |
| min_samples_split    | 5      |
| min_samples_leaf     | 2      |

These adjustments improved the model’s balance between precision and recall while maintaining high overall accuracy.

---

## ✅ Results

**Final Model (Random Forest) Metrics:**
- Accuracy: **93.1%**
- Precision: **88%**
- Recall: **63%**
- F1-Score: **0.74**
- AUC-ROC: **0.93**

---

## 📌 Conclusion

The **Random Forest model** performed exceptionally well in predicting customer churn. Although there was a slight trade-off in recall, the model offers significant value for businesses aiming to retain customers.

**Future work may include:**
- Addressing class imbalance using **SMOTE** or similar techniques.
- Exploring **ensemble stacking** for further performance gains.

This project demonstrates how machine learning can effectively drive real-world business decisions and optimize retention strategies.




