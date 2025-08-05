# 🛋️ E-commerce Furniture Sales Prediction (2024)

This project predicts the number of furniture items sold using product data from AliExpress.

## 📌 Objective
To build a machine learning model that predicts how many units of a product will be sold based on:
- Price
- Product Title (text)
- Shipping Info (tagText)

---

## 🛠️ Tools & Technologies Used
- Python
- Jupyter Notebook
- Pandas, Seaborn, Scikit-learn
- TF-IDF (for text vectorization)

---

## 📦 Dataset Overview
- 2,000 products scraped from AliExpress
- Columns:
  - `productTitle`
  - `originalPrice` (dropped due to missing values)
  - `price`
  - `sold` (target variable)
  - `tagText` (shipping details)

---

## 📊 Project Pipeline

1. **Data Cleaning**
   - Dropped `originalPrice`
   - Cleaned `$` from `price`
   - Simplified shipping tags
2. **EDA**
   - Visualized `price`, `sold`, shipping distribution, price vs sold
3. **Feature Engineering**
   - TF-IDF vectorization on product titles
   - Encoded shipping tags
4. **Modeling**
   - Linear Regression
   - Random Forest Regressor
5. **Model Evaluation**
   - MSE & R² Score used for comparison

---

## 📈 Results

| Model               | MSE           | R² Score          |
|--------------------|---------------|-------------------|
| Linear Regression  | 13,557.91     | -1.47             |
| Random Forest      | 17,350.74     | -2.16             |

⚠️ Models performed poorly due to high imbalance and noise in the data. Can be improved by feature tuning and outlier handling.

---

## 📁 Folder Structure
Ecommerce_furniture_project/
├── Dataset/                  ← contains the CSV dataset
├── notebooks/                ← contains EDA + model training notebooks
├── Visuals/                  ← optional folder for EDA graphs (if saved)
├── README.md                 ← your project summary
└── requirements.txt          ← list of Python packages used



