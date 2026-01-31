# Diabetes Prediction using Machine Learning

## 📌 Overview
This project predicts **Diabetes Risk** using Machine Learning models on a large healthcare dataset.  
The objective is to analyze lifestyle and medical indicators to determine whether a person is likely to have diabetes.  
The project covers **EDA, hypothesis testing, preprocessing, feature engineering, model training, and dimensionality reduction**.

---

## 📊 Dataset
- **Source:** CDC Diabetes Health Indicators – UCI Machine Learning Repository
- **Rows:** 253,680
- **Columns:** 22 Health & Lifestyle Features
- **Target Variable:** `Diabetes_binary` (0 = No Diabetes, 1 = Diabetes)
- **Duplicate Rows:** 24,206
- **Total Data Points:** ~5.58 Million
- **Data Type:** int64

---

## ❓ Problem Statement
To analyze adult US population health data and predict diabetes likelihood based on demographic and lifestyle parameters using statistical and machine learning techniques.

---

## 🔍 Exploratory Data Analysis
- Severe **class imbalance** (≈ 86% Non-Diabetic, 14% Diabetic)
- Strong correlations with:
  - `DiffWalk`
  - `GenHlth`
  - `PhysHlth`
- Weak correlation with lifestyle features such as fruits and vegetables.

---

## 🧪 Hypothesis Testing
Statistical tests applied:
- **Welch T-Test** – BMI mean differences
- **Chi-Square Tests** – Independence with Diabetes:
  - Smoking
  - Physical Activity
  - High Blood Pressure
  - Cholesterol
  - Income
  - Education
  - Fruits & Vegetables
  - Alcohol Consumption
  - Heart Disease

Most null hypotheses were rejected, indicating significant associations.

---

## ⚙️ Data Preprocessing
- **SMOTE** – Handled class imbalance.
- **Feature Engineering**
  - `CardioRisk = HighBP + HighChol`
  - `HealthyDiet = Fruits + Veggies`
- **Scaling** – Standardization for better convergence.
- **Dimensionality Reduction** – Johnson–Lindenstrauss (JL) Lemma via Random Projection.

---

## 🤖 Models Implemented
| Model | Accuracy |
|------|---------|
| Logistic Regression | ~86.5% |
| Decision Tree | ~86.6% |
| Bagging | ~86.6% |
| Random Forest | ~85.8% |
| Linear SVM | ~86.4% |

### After JL Dimensionality Reduction
- Accuracy drop was minimal (~0.3–0.5%)
- **Average Training Time Improvement:** ~71%

---

## ⏱ Time Complexity
- **Logistic Regression:** `O(N · D)`
- **Decision Tree:** `O(N log N · D)`
- **Random Forest:** `O(K · N log N · D)`

Where:
- `N` = Number of Samples  
- `D` = Number of Features  
- `K` = Number of Trees  

---

## 🏁 Conclusion
- Logistic Regression achieved performance comparable to complex models.
- JL Lemma reduced dimensionality with minimal accuracy loss.
- Simpler models proved efficient and reliable for healthcare prediction.

---

## 🚀 Future Work
- Advanced Feature Selection
- Deep Learning Models
- Real-time Prediction API
- Cross-Country Dataset Comparison

---



---

## 🛠 Tech Stack
- Python
- Scikit-learn
- Pandas / NumPy
- Matplotlib / Seaborn


---

## 📜 License
This project is for academic and research purposes only.
