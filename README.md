# 📊 Customer Churn Prediction Using Machine Learning

This project presents a machine learning-based solution to predict customer churn in the banking sector using supervised learning models. The goal is to identify customers who are likely to leave a bank, enabling early intervention and customer retention strategies. 

The study uses a publicly available dataset from Kaggle and compares multiple classification models—Logistic Regression, Support Vector Machine (SVM), Decision Tree, and Random Forest. Feature selection, data balancing, and performance evaluation metrics were applied to develop and validate the models.

---

## 📌 Project Objectives

- Predict whether a customer will churn (i.e., leave the bank).
- Apply data preprocessing, feature selection, and data balancing techniques.
- Train and evaluate different machine learning models.
- Compare model performances using metrics such as Accuracy, Precision, Recall, and F1-score.
- Identify the best-performing model for churn prediction.

---

## 🧾 Dataset Overview

- **Source:** Kaggle (Churn Modelling Dataset)
- **Records:** 10,000 bank customers
- **Features:** 14 (e.g., CreditScore, Geography, Age, Balance, NumOfProducts, etc.)
- **Target Variable:** `Exited` (1 if customer left, 0 otherwise)
- **File Format:** CSV

> Note: The dataset contains a mix of categorical and numerical variables and shows class imbalance (more non-churners than churners), which was addressed through oversampling techniques.

---

## 🛠️ Technologies and Libraries

- **Python 3.x**
- **Jupyter Notebook**
- **Libraries Used:**
  - `pandas`, `numpy`: Data handling
  - `matplotlib`, `seaborn`: Data visualization
  - `scikit-learn`: Machine learning models & evaluation
  - `imbalanced-learn`: For handling class imbalance

---

## 🔍 Data Preprocessing and Feature Engineering

- Handled missing values and outliers.
- Label encoding for categorical variables.
- Standardized numerical features.
- Performed **Feature Selection** using mRMR (Minimum Redundancy Maximum Relevance).
- Applied oversampling (e.g., SMOTE) to balance the target classes.

---

## 📈 Exploratory Data Analysis (EDA)

- Plotted histograms for distribution of features like Age, Balance, Credit Score.
- Visualized relationships using pairplots and scatterplots.
- Correlation heatmap to identify feature interactions.
- Identified important predictors of churn.

---

## 🤖 Machine Learning Models Implemented

### 1. Logistic Regression (LR)
- Baseline model.
- Performed reasonably but had limitations with imbalance.

### 2. Decision Tree (DT)
- Easy to interpret but prone to overfitting.
- Accuracy: ~80.63%

### 3. Support Vector Machine (SVM)
- Achieved the best performance.
- Accuracy: **86.27%**
- F1 Score: **84.22%**

### 4. Random Forest (RF)
- Robust ensemble method.
- Accuracy: 86.07%
- Performed well but slightly below SVM.

---

## 📊 Model Evaluation Metrics

| Metric     | SVM     | Random Forest | Decision Tree | Logistic Regression |
|------------|---------|----------------|----------------|---------------------|
| Accuracy   | 86.27%  | 86.07%         | 80.63%         | 81.36%              |
| Precision  | 81.15%  | 75.00%         | 50.25%         | 55.76%              |
| Recall     | 38.36%  | 43.00%         | 52.00%         | 42.00%              |
| F1-Score   | 52.00%  | 54.00%         | 51.00%         | 47.86%              |

- Confusion matrices were used for visual analysis.
- ROC-AUC could be considered in future enhancements.

---

## 🧠 Key Findings

- **SVM** emerged as the most accurate and balanced model for this classification problem.
- Age and credit score were found to be top predictors of churn.
- Feature selection and oversampling improved model performance significantly.

---

## 📁 Repository Contents

```bash
📂 customer-churn-prediction-ml/
├── churn_prediction.ipynb        # Jupyter Notebook with full ML pipeline
├── GroupReport.docx              # Detailed project report
├── requirements.txt              # Python dependencies
└── README.md                     # Project documentation (this file)
