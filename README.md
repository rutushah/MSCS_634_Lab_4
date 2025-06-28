# Lab 4: Regression Analysis with Regularization Techniques

**Author**: Rutu Ketankumar Shah  
**Course**: MSCS 634 – Advanced Big Data and Data Mining  
**Semester**: Summer 2025  

---

## 📌 Lab Objective

This lab explores several regression modeling techniques on the Diabetes dataset from `sklearn.datasets`. The main goals are to:

- Implement and evaluate Simple Linear Regression, Multiple Linear Regression, and Polynomial Regression models.  
- Apply Ridge and Lasso Regularization to control overfitting.  
- Measure model performance using MAE, MSE, RMSE, and R².  
- Visualize regression results for interpretability.  

---

## 📊 Dataset

The **Diabetes dataset** is a built-in dataset in Scikit-learn. It includes 10 physiological variables (age, BMI, blood pressure, etc.) and a target representing disease progression.

---

## 🧪 Lab Steps

### Step 1: Data Preparation
- Load the diabetes dataset.
- Convert it into a pandas DataFrame.
- Check for missing values and explore feature distribution.

### Step 2: Simple Linear Regression
- Select a single independent feature (e.g., `age` or `bmi`).
- Fit and evaluate a linear model using regression metrics.

### Step 3: Multiple Regression
- Train a model using all features.
- Evaluate performance and visualize prediction results.

### Step 4: Polynomial Regression
- Use `PolynomialFeatures` to generate higher-degree features.
- Compare training vs testing performance to observe overfitting/underfitting behavior.

### Step 5: Ridge and Lasso Regression
- Apply Ridge (`L2`) and Lasso (`L1`) regularization.
- Tune the `alpha` parameter and observe changes in performance and coefficients.

---

## 📈 Key Insights

- **Multiple Regression** significantly outperforms Simple Regression in predictive accuracy.
- **Polynomial Regression** improves training performance but risks overfitting if the degree is too high.
- **Ridge and Lasso** improve generalization and reduce model complexity by penalizing large coefficients.
- **Lasso Regression** provides additional benefit of feature selection by zeroing out less important features.

---

## ✅ Results Summary

| Model                    | MAE    | MSE    | RMSE   | R²     |
|--------------------------|--------|--------|--------|--------|
| Simple Linear Regression | High   | High   | High   | Low (~0.04) |
| Multiple Regression      | Moderate | Moderate | Lower | ~0.51 |
| Polynomial Regression (deg=3) | Low | Low | Lowest | ~0.75 |
| Ridge Regression         | Moderate | Moderate | Lower | ~0.68 |
| Lasso Regression         | Moderate | Moderate | Lower | ~0.66 |

---

## 🧠 Challenges Faced

- Determining the optimal polynomial degree without overfitting.  
- Tuning regularization parameters (`alpha`) to strike a balance between bias and variance.  
- Ensuring meaningful visual interpretation through proper plots.  

---

## 📂 Files in this Repository

- `Lab4.ipynb` – Full Jupyter Notebook with code and visualizations.  
- `README.md` – Overview of the lab, methodology, and results.  

---

## 🔗 References

- Wu, D. (2024). *Data Mining with Python: Theory, application, and case studies*. Chapman & Hall/CRC.  
- GeeksforGeeks. (2024, April 29). *Sklearn Diabetes Dataset: Scikit-learn toy datasets in Python*. https://www.geeksforgeeks.org/machine-learning/sklearn-diabetes-dataset/
