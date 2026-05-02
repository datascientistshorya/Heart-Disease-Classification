# 🫀 Heart Disease Prediction — End-to-End ML Project

## 📌 Overview
This project builds a machine learning pipeline to predict heart disease using clinical data. The focus is on **high recall (sensitivity)** to minimize false negatives, which is critical in medical diagnosis.

---

## 📊 Dataset
The dataset includes patient-level clinical features such as:
- Age, Cholesterol, Blood Pressure
- Maximum Heart Rate (thalach)
- ST depression (oldpeak)
- Chest Pain Type (cp), Thalassemia (thal), etc.

**Target Variable:**
- 0 → No disease  
- 1 → Heart disease  

---

## 🔍 Exploratory Data Analysis (EDA)
Key findings:
- Higher age, cholesterol, and BP → higher risk  
- Lower max heart rate → strong disease indicator  
- Oldpeak shows strong separation  
- Moderate multicollinearity observed  

---

## 🛠️ Feature Engineering
Engineered features to improve model performance:
- Risk indicators: `high_chol`, `high_bp`, `low_thalach`
- Interaction features: `chol_bp`, `stress_index`
- Age binning for risk segmentation
- Composite `risk_score`

---

## ⚙️ Preprocessing Pipeline
- Train-test split (stratified)
- Standard scaling (numerical features)
- One-hot encoding (categorical features)
- Pipeline-based implementation (no data leakage)

---

## 🤖 Models Implemented

### 1. Logistic Regression
- Baseline model
- ROC-AUC ~0.86
- Recall improved via threshold tuning

### 2. Linear Discriminant Analysis (LDA) ⭐
- Accuracy: **82%**
- Recall: **94%**
- Best model for minimizing false negatives

### 3. Quadratic Discriminant Analysis (QDA)
- Failed due to multicollinearity
- Highlighted dataset limitations

### 4. K-Nearest Neighbors (KNN)
- ROC-AUC: **0.88 (highest)**
- Strong ranking ability but lower recall than LDA

---

## 📈 Model Evaluation
- ROC Curve → ranking performance
- Precision-Recall Curve → clinical relevance
- Confusion Matrix → error analysis

---

## 🧠 Key Insights
- Dataset is mostly **linearly separable**
- Feature engineering significantly boosts performance
- LDA outperforms more complex models
- ROC-AUC alone is not sufficient for medical problems
- Threshold tuning improves real-world usability

---

## 🏆 Final Model Selection
**LDA** chosen as best model due to:
- Highest recall (0.94)
- Lowest false negatives
- Stable and interpretable performance

---

## 🚀 Future Work
- Try ensemble models (Random Forest, XGBoost)
- Hyperparameter tuning (GridSearchCV)
- Model deployment (Flask/Streamlit)
- Explainability using SHAP

---

## 📌 Conclusion
This project demonstrates that **simple, well-tuned models with strong feature engineering outperform complex models** in structured medical datasets, especially when optimizing for recall and patient safety.

## Author

https://www.linkedin.com/in/shorya-bisht-a20144349/

