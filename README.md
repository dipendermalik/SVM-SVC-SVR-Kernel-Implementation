# Support Vector Machines (SVC & SVR) – End-to-End Implementation

## Project Overview
This repository demonstrates a comprehensive implementation of Support Vector Machines (SVM) covering both:

- Classification (SVC)
- Regression (SVR)

The project includes:
- Mathematical intuition of SVM
- Linear vs Non-linear separability
- Kernel trick (RBF, Polynomial, Sigmoid)
- Hyperparameter tuning using Grid Search
- Performance comparison across models
- Visualization (2D & 3D)

---

## Key Concepts Covered

### Support Vector Classifier (SVC)
- Maximum margin hyperplane
- Support vectors and margin optimization
- Hard margin vs soft margin

SVM aims to maximize the margin between classes while minimizing classification errors.

---

### Support Vector Regression (SVR)
- Epsilon-insensitive loss function
- Trade-off between margin width and prediction error

SVR fits a function within a margin (epsilon) while penalizing deviations beyond it.

---

### Kernel Trick
Used to transform non-linear data into higher dimensions where it becomes linearly separable.

Kernels implemented:
- Linear
- Polynomial
- RBF (Radial Basis Function)
- Sigmoid

---

## Project Workflow

### 1. Data Generation
- Created synthetic datasets:
  - Linearly separable
  - Non-linearly separable (circular patterns)

### 2. Data Preprocessing
- Train-test split
- Feature scaling (important for SVM)

### 3. Model Training

#### Classification Models (SVC)
- Linear Kernel
- RBF Kernel
- Polynomial Kernel
- Sigmoid Kernel

#### Regression Models (SVR)
- Linear SVR
- RBF SVR
- Tuned SVR using GridSearchCV

---

## Hyperparameter Tuning

Performed using GridSearchCV with:
- Cross-validation
- Multiple scoring metrics:
  - MSE
  - R2

Key parameters tuned:
- C: Regularization strength
- gamma: Kernel coefficient
- epsilon: Margin for SVR

---

## Model Evaluation Metrics

### Classification
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC
- Gini
- KS Statistic

### Regression
- MSE
- RMSE
- MAE
- R2 Score
- Adjusted R2

---

## Key Findings

### 1. Linear vs Non-linear Models
Linear SVM performed similarly or slightly better than RBF in many cases.  
This indicates that the underlying data is largely linear.

---

### 2. RBF Kernel Behavior
Best parameters found:
- C = 200
- gamma = 0.001
- epsilon = 0.1

Interpretation:
- Low gamma results in a smoother decision boundary
- High C forces the model to fit data more closely

This combination makes RBF behave similarly to a linear model.

---

### 3. Polynomial Kernel Performance
Polynomial kernel showed slightly better performance in some cases, indicating mild non-linearity in the data.

---

### 4. Bias-Variance Tradeoff

| Model    | Behavior                    |
|----------|----------------------------|
| Linear   | Higher bias, low variance  |
| RBF      | Lower bias, higher variance|
| Polynomial | Balanced                 |

---

## Sample Results

| Model                  | Test RMSE | Test R2 |
|------------------------|----------|--------|
| SVR (Grid - RBF)       | ~5.10    | ~0.448 |
| Linear SVR             | ~5.09    | ~0.450 |
| Polynomial SVR         | ~5.01    | ~0.467 |

---

## Visualizations Included
- Pairplots
- 2D decision boundaries
- 3D plots using Plotly
- Regression prediction plots
- ROC curves

---

## Key Learnings
- SVM is highly sensitive to feature scaling
- Kernel selection depends on data structure
- RBF does not always outperform linear models
- Hyperparameter tuning should follow:
  - Broad search
  - Narrow refinement

---
