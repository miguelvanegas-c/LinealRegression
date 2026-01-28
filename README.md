

# 📘 Machine Learning Project: Linear and Polynomial Regression on Stellar Data

## 📌 Project Overview

This project studies the relationship between **stellar mass** and **stellar luminosity** using regression techniques. Two different models are implemented and analyzed:

1. A **linear regression model with one input feature**.
2. A **polynomial regression model** that extends the first model to better capture non-linear behavior.

The goal is to understand how well each model represents the data and why more complex models can improve prediction accuracy when the relationship between variables is not linear.

All models are implemented from scratch using Python, NumPy, and Matplotlib to better understand how regression works internally.

---

## 🗂 Repository Structure

```
.
├── 01_part1_linreg_1feature.ipynb   # Linear regression with one feature
├── 02_part2_polyreg.ipynb          # Polynomial regression model
└── README.md                       # Project documentation
```

---

## 🎯 Objectives

* Explore the relationship between stellar mass and luminosity.
* Visualize the dataset and identify patterns.
* Build a linear regression model from scratch.
* Evaluate the limitations of a linear model.
* Improve the model using polynomial regression.
* Compare both models and analyze their performance.
* Understand the importance of feature engineering and normalization.

---

## 📊 Dataset Description

The dataset contains physical properties of stars:

* **Mass (M)**: The mass of a star.
* **Luminosity (L)**: The brightness of a star.
* **Temperature (T)**: Additional feature used in the second notebook.

The main objective is to predict luminosity based on mass and extended features.

---

# 🔹 Part 1: Linear Regression with One Feature

Notebook: `01_part1_linreg_1feature.ipynb`

This notebook focuses on building and analyzing a simple linear regression model using only one input feature: stellar mass.

---

## 1. Data Visualization

The notebook begins by plotting stellar mass against luminosity using a scatter plot.
This allows visual inspection of the data and reveals that:

* The relationship between mass and luminosity increases continuously.
* The pattern is curved rather than straight.
* A simple straight line may not describe the data accurately.

This step is essential to understand the nature of the problem before modeling.

---

## 2. Model Construction

A linear regression model is created that attempts to predict luminosity using only mass.
The model tries to find the best straight line that fits the data.

The notebook defines:

* Model parameters.
* A prediction function.
* A way to measure how far predictions are from real values.

---

## 3. Training the Model

The model is trained using an iterative optimization process:

* Initial values are assigned to the model parameters.
* The algorithm repeatedly adjusts these parameters.
* Each step aims to reduce prediction error.
* The cost (error) is tracked across iterations.

This process shows how the model gradually improves during training.

---

## 4. Visualization of Training Results

After training:

* The fitted regression line is plotted on top of the original data.
* Predictions are compared with real luminosity values.
* A cost curve is plotted to show how the error decreases over time.

These plots help confirm whether the model is learning correctly.

---

## 5. Model Evaluation

The linear regression model is evaluated by analyzing:

* Prediction accuracy.
* Shape of the fitted line.
* Remaining error.

The results show that although the model captures the general trend, it fails to represent the curved nature of the data accurately. This leads to systematic prediction errors.

---

## 6. Limitations of the Linear Model

The notebook concludes that:

* The relationship between mass and luminosity is not linear.
* A straight line cannot represent the real growth behavior of luminosity.
* The model suffers from underfitting.
* A more flexible model is required.

This motivates the transition to polynomial regression.

---

# 🔹 Part 2: Polynomial Regression

Notebook: `02_part2_polyreg.ipynb`

This notebook extends the previous work by building a polynomial regression model that can represent curved relationships.

---

## 1. Feature Engineering

New features are created from the original mass variable by transforming it into higher-order terms.
This allows the model to learn non-linear patterns in the data.

Additional variables such as temperature are also included to enrich the input data.

---

## 2. Data Normalization

Before training, the data is normalized:

* All features are scaled to similar ranges.
* This improves numerical stability.
* Training becomes faster and more reliable.

Normalization is a key step for models with multiple features.

---

## 3. Model Training

A multivariable regression model is trained using the same optimization strategy as before, but now with more parameters.

During training:

* The model gradually reduces prediction error.
* The cost function decreases consistently.
* Parameter updates are done using vectorized operations for efficiency.

---

## 4. Visualization of Polynomial Fit

After training:

* A curved regression line is plotted over the data.
* The model follows the actual data distribution more closely than the linear model.
* Predictions align better with observed luminosity values.

This demonstrates the advantage of using polynomial regression for non-linear data.

---

## 5. Model Comparison

The two models are compared in terms of performance and behavior:

| Aspect              | Linear Regression | Polynomial Regression |
| ------------------- | ----------------- | --------------------- |
| Shape of prediction | Straight line     | Curved line           |
| Fit to data         | Poor              | Much better           |
| Error               | Higher            | Lower                 |
| Flexibility         | Low               | High                  |
| Underfitting        | Yes               | Reduced               |

The polynomial model clearly outperforms the linear model for this dataset.

---

# 🧠 Key Concepts Learned

This project covers important machine learning concepts:

* Data visualization and exploration
* Linear regression
* Polynomial regression
* Feature engineering
* Normalization
* Model training
* Model evaluation
* Underfitting vs improved fitting
* Model comparison
* Interpretation of results

---

# 🛠 Technologies Used

* Python
* NumPy
* Matplotlib
* Jupyter Notebook

---

# 📈 Results and Conclusions

* Stellar mass and luminosity have a non-linear relationship.
* Linear regression is too simple for this problem.
* Polynomial regression provides a better approximation.
* Visualization plays a crucial role in understanding model behavior.
* Feature engineering significantly improves model performance.

---


