# 🚀 Categorical Data Encoding in Python

A complete hands-on project demonstrating how to handle and encode categorical data using **Pandas** and **Scikit-learn**. This repository covers everything from basic encoding techniques to advanced preprocessing pipelines used in real-world machine learning workflows.

---

## 📌 Table of Contents

* Introduction
* Dataset Overview
* Techniques Covered
* Installation
* Usage
* Project Workflow
* Output Examples
* Key Learnings
* Best Practices
* Future Improvements
* Contributing
* License

---

## 📖 Introduction

Categorical data is a crucial part of most real-world datasets. Machine learning models require numerical input, so converting categorical features into a usable format is an essential preprocessing step.

This project demonstrates:

* One-Hot Encoding
* Label Encoding
* Handling Missing Values
* High Cardinality Issues
* Scikit-learn Pipelines
* Column Transformers

---

## 📂 Dataset Overview

The dataset used in this project is a sample dataset containing:

| Feature    | Description            |
| ---------- | ---------------------- |
| City       | Name of the city       |
| Country    | Country name           |
| Population | Population of the city |
| Continent  | Continent of the city  |

---

## ⚙️ Techniques Covered

### 🔹 1. One-Hot Encoding (Pandas)

Converts categorical values into binary columns.

**Example:**

```python
pd.get_dummies(df['City'], prefix='City')
```

✅ Best for low-cardinality data
❌ Can create too many columns

---

### 🔹 2. High Cardinality Problem

When a column has many unique values, One-Hot Encoding creates too many features.

**Example:**

```python
df['UniqueID'] = np.arange(len(df))
```

⚠️ Problems:

* Increased memory usage
* Slower training
* Risk of overfitting

---

### 🔹 3. Handling Missing Values

Missing values are handled before encoding.

**Using Pandas:**

```python
df.fillna('Unknown')
```

**Using Scikit-learn:**

```python
SimpleImputer(strategy='most_frequent')
```

---

### 🔹 4. Label Encoding

Converts categories into numeric labels.

```python
LabelEncoder()
```

✅ Useful for ordinal data
❌ Not suitable for nominal data

---

### 🔹 5. Column Transformer

Applies transformations to specific columns.

```python
ColumnTransformer([
    ('onehot', OneHotEncoder(handle_unknown='ignore'), ['City'])
])
```

---

### 🔹 6. Pipeline (Automation)

Automates preprocessing steps.

```python
Pipeline([
    ('imputer', SimpleImputer(strategy='most_frequent')),
    ('preprocessor', ColumnTransformer(...))
])
```

✅ Clean workflow
✅ Reusable
✅ Production-ready

---

### 🔹 7. Inverse Transformation

Recover original labels from encoded values.

```python
label.inverse_transform(encoded_values)
```

---

## 🛠️ Installation

Install required libraries:

```bash
pip install pandas numpy scikit-learn
```

---

## ▶️ Usage

1. Clone the repository:

```bash
git clone https://github.com/your-username/categorical-encoding.git
```

2. Navigate to the project:

```bash
cd categorical-encoding
```

3. Run the Python script:

```bash
python main.py
```

---

## 🔄 Project Workflow

1. Create dataset using Pandas
2. Apply One-Hot Encoding
3. Demonstrate high cardinality issue
4. Handle missing values
5. Apply Label Encoding
6. Build preprocessing pipeline
7. Transform dataset
8. Recover original values

---

## 📊 Output Examples

### ✅ One-Hot Encoded Data

* City_New York → 1/0
* City_London → 1/0

### ⚠️ High Cardinality Example

* Unique ID creates many columns

### 🔄 Pipeline Output

* Clean and transformed dataset ready for ML

---

## 🧠 Key Learnings

* One-Hot Encoding works best for low-cardinality features
* Label Encoding is useful for ordered categories
* Pipelines simplify preprocessing workflows
* Missing values must be handled before encoding
* High-cardinality features should be treated carefully

---

## 💡 Best Practices

✔ Use `handle_unknown='ignore'` in OneHotEncoder
✔ Use pipelines for production-ready code
✔ Avoid One-Hot Encoding for high-cardinality features
✔ Consider advanced techniques like:

* Target Encoding
* Frequency Encoding

---

## 🚀 Future Improvements

* Add Target Encoding implementation
* Add Frequency Encoding
* Use real-world datasets
* Integrate with ML models
* Add visualization of encoded data

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Commit your changes
4. Submit a pull request

---

## ⭐ Support

If you found this project helpful:

* ⭐ Star the repository
* 📢 Share with others

---

## 📜 License

This project is open-source and available under the MIT License.

---

## 👨‍💻 Author

**Radhe**

* YouTube: @learn.pywithradhe
* Instagram: @learn.pywithradhe
* Telegram: https://t.me/learnpywithradhe

---

🔥 *Happy Learning & Keep Coding!*
