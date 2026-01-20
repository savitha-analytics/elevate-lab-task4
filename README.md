# 📊 Task 4: Feature Encoding & Scaling  
**Dataset:** Adult Income Dataset

---

## 🧾 Overview
This task focuses on preparing the **Adult Income dataset** for machine learning by converting categorical data into numerical form and scaling numerical features. Proper encoding and scaling improve model performance and ensure compatibility with various ML algorithms.

---

## 🛠 Tools Used
- **Python**
  - Pandas
  - Matplotlib
  - Seaborn  
- **Alternative:** Tableau Public (for visualization)

---

## 📂 Dataset Description
The Adult Income dataset predicts whether an individual's income exceeds **$50K/year** based on demographic and employment attributes.

**Target Variable:** `income`

---

## 1️⃣ Identify Feature Types

### 🔢 Numerical Features
- age  
- fnlwgt  
- educational-num  
- capital-gain  
- capital-loss  
- hours-per-week  

### 🔠 Categorical Features
- workclass  
- education  
- marital-status  
- occupation  
- relationship  
- race  
- gender  
- native-country  

---

## 2️⃣ Label Encoding (Ordered Categorical Data)

**Applied to:** `education`

**Reason:**  
Education levels have a natural hierarchy (Preschool → Doctorate).  
Label Encoding preserves this order by converting categories into ordered numerical values.

---

## 3️⃣ One-Hot Encoding (Nominal Categorical Data)

**Applied to:**  
- workclass  
- marital-status  
- occupation  
- relationship  
- race  
- gender  
- native-country  

**Reason:**  
These features do not have any intrinsic order.  
One-Hot Encoding prevents the model from learning false ordinal relationships.

---

## 4️⃣ Feature Scaling (StandardScaler)

**Scaled Numerical Features:**
- age  
- fnlwgt  
- educational-num  
- capital-gain  
- capital-loss  
- hours-per-week  

**Why Scaling?**
- Features exist in different ranges
- Prevents large-value features from dominating model learning

**Method Used:**  
StandardScaler (mean = 0, standard deviation = 1)

---

## 5️⃣ Model Readiness Comparison

### ❌ Before Scaling
- Uneven feature ranges
- Slower convergence
- Poor performance for distance-based algorithms

### ✅ After Scaling
- Uniform feature scale
- Faster training
- Improved accuracy and stability

---

## 6️⃣ Impact of Scaling on ML Algorithms

### 🚀 Algorithms That Benefit from Scaling
- Logistic Regression
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)
- Neural Networks

### 🌳 Algorithms Less Affected by Scaling
- Decision Trees
- Random Forest
- Gradient Boosting

---

## 7️⃣ Output

The final processed dataset is saved as:
adult_encoded_scaled.csv

This dataset is fully numeric and ready for machine learning models.

---

## 📌 Summary
- Correctly identified numerical and categorical features
- Applied Label Encoding where order exists
- Used One-Hot Encoding for unordered categories
- Scaled numerical features using StandardScaler
- Improved dataset readiness for ML models
- Saved the processed dataset for reuse

---

## 🚀 Next Steps
- Train classification models
- Perform feature selection
- Hyperparameter tuning
- Model deployment

---
