# House_Price_Prediction.
Project 1 - Week 1
# 🏠 House Price Prediction (California Housing)

## 📌 Project Overview
This project focuses on predicting house prices using the **California Housing dataset**. The goal is to build a regression model and compare the performance of standard Linear Regression against Regularized Linear Models (**Lasso** and **Ridge**) to understand the impact of regularization on model performance and overfitting.

## 📂 Dataset
* **Source:** Scikit-Learn (`sklearn.datasets.fetch_california_housing`)
* **Description:** The dataset contains data on housing in California districts, including features like median income, house age, average rooms, etc.
* **Target Variable:** Median House Value.

## 🛠️ Technologies Used
* **Python 3.x**
* **Pandas & NumPy** (Data Manipulation)
* **Scikit-Learn** (Model Building & Evaluation)
* **Matplotlib/Seaborn** (Visualization)

## ⚙️ Models & Approach
We trained and evaluated three different regression models:

1.  **Linear Regression:** The baseline model without regularization.
2.  **Lasso Regression (L1):** Adds a penalty equal to the absolute value of the magnitude of coefficients. (Useful for feature selection).
3.  **Ridge Regression (L2):** Adds a penalty equal to the square of the magnitude of coefficients. (Useful for preventing large coefficients).

## 📊 Results & Comparison
The models were evaluated using **RMSE** (Root Mean Squared Error) and **R² Score**.

| Model | RMSE (Lower is better) | R² Score (Higher is better) |
| :--- | :--- | :--- |
| **Linear Regression** | 0.745581 | 0.575788 |
| **Lasso (L1)** | 0.824396 | 0.481361 |
| **Ridge (L2)** | 0.745557 | 0.575816 |

### 📝 Key Observations
* **Linear Regression vs. Ridge:** The performance of Ridge Regression is almost identical to the standard Linear Regression in this specific case, suggesting that the baseline model didn't suffer significantly from high variance due to large coefficients.
* **Lasso Performance:** Lasso performed worse (lower R² and higher RMSE). This indicates that aggressively shrinking coefficients to zero (feature selection) might have removed useful information from this specific dataset.
* **Regularization:** While regularization helps generalization, in this specific dataset/split, the standard model was already quite robust.

## 🚀 How to Run
1.  **Install Dependencies:**
    ```bash
    pip install pandas numpy scikit-learn matplotlib
    ```
2.  **Run the Notebook:**
    Open `House_Price_Prediction.ipynb` in Jupyter Notebook or Google Colab and execute the cells sequentially.

## 📜 License
This project is for educational purposes.
