# Complete-Guide-to-Categorical-Data-Encoding-in-Python-One-Hot-Pipelines-Missing-Values-
# 🚀 Categorical Data Encoding in Python

This project demonstrates how to handle and encode categorical data in Python using **Pandas** and **Scikit-learn**. It covers real-world preprocessing techniques including:

- One-Hot Encoding
- Label Encoding
- Handling Missing Values
- High Cardinality Issues
- Pipelines & Column Transformers

---

## 📂 Dataset Overview

We work with a sample dataset containing:

- City 🌆
- Country 🌍
- Population 👥
- Continent 🌎

---

## ⚙️ Features Covered

### 1️⃣ One-Hot Encoding (Pandas)
Convert categorical variables into binary columns.

```python
pd.get_dummies(df['City'], prefix='City')
