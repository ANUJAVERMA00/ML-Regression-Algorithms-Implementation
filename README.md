#  AAPL Stock Price Prediction: A Multi-Stage Regression Study
**A Comprehensive Implementation of Iterative and Analytical Optimization Models**

## Project Team
| Name | Roll Number | Role & Contribution |
| :--- | :--- | :--- |
| **Anuja Verma** | CSJMA23001390276 | Lead Developer: Code implementation, Data Visualization, and Algorithm Optimization. |
| **Deepanshu Sharma** | CSJMA23001390312 | Lead Strategist: Mathematical Logic, Statistical Derivations, and Theoretical Framework. |

---

##  Project Overview
This project involves a deep-dive into the mathematical and practical implementation of Linear Regression to predict **Apple Inc. (AAPL)** stock prices. We developed a progression of models starting from scratch-implemented Gradient Descent to advanced Regularized Multivariate systems.

---

##  1. EDA and Visualization
**Objective:** To audit data health and understand the underlying relationships between global tech giants.

* **Logic:** We utilized **Pearson Correlation** to measure the linear strength between AAPL, MSFT, and TSLA. We chose this because stock prices in the tech sector often move in "clusters" due to shared market sentiment.
* **Math Formula:** $$r = \frac{\sum (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum (x_i - \bar{x})^2 \sum (y_i - \bar{y})^2}}$$
* **Reasoning:** We performed **Outlier Detection** using the IQR method ($Q3 - Q1$) to ensure that black-swan market events didn't skew our model's "perception" of a standard trading day.



---

##  2. Model Implementation
We progressed through three distinct architectural stages to find the optimal fit:

### **A. Simple Linear Regression (Gradient Descent)**
* **Logic:** Implemented an iterative approach to find the line of best fit.
* **Math:** Minimized the **Mean Squared Error (MSE)** cost function:
    $$J(m, c) = \frac{1}{2n} \sum_{i=1}^{n} (y_{pred} - y_{actual})^2$$
* **Update Rule:** Used a learning rate ($\alpha = 0.1$) to update weights:
    $$m = m - \alpha \frac{\partial J}{\partial m}$$

### **B. Polynomial Regression (Non-Linearity)**
* **Logic:** We realized that stock prices don't always move in straight lines. By adding a **Squared Term ($x^2$)**, we allowed the model to capture "price acceleration."
* **Reasoning:** This allows the model to fit a parabolic curve, which is more representative of volatile market shifts.

### **C. Regularization (Ridge & Lasso)**
* **Logic:** To prevent **Overfitting** (where the model memorizes noise instead of patterns).
* **Ridge (L2):** Adds $\lambda \sum \theta^2$ to the cost function to shrink coefficients.
* **Lasso (L1):** Adds $\lambda \sum |\theta|$, which performs **Feature Selection** by zeroing out less relevant predictors like Volume.



---

##  3. Evaluation and Comparison
We benchmarked every model using three core metrics to ensure a 360-degree view of accuracy:
1.  **MSE (Mean Squared Error):** Measures average squared variance.
2.  **RMSE (Root Mean Squared Error):** Provides the error in actual Dollar units.
3.  **R² Score:** Tells us what percentage of the price movement we successfully explained.

###  Final Model Leaderboard
| Stage | Model Description | RMSE (Error $) | R² Score |
| :--- | :--- | :--- | :--- |
| **Part B** | Simple Linear (Univariate) | 3.8948 | 0.9716 |
| **Part D** | Polynomial Regression ($x^2$) | 3.3292 | 0.9792 |
| **Part F** | **Multiple Linear (Final Model)** | **3.3002** | **0.9796** |

---

## 🏁 4. Interpretation and Conclusion
* **The Power of Context:** Moving from a simple model (Part B) to a multivariate model (Part F) reduced our prediction error by **15.2%**. This proves that AAPL's price is heavily influenced by the performance of its peers (MSFT & TSLA).
* **Mathematical Validity:** In our **Model Diagnostics (Part F)**, we plotted **Residuals vs. Predicted Values**. The resulting random "cloud" of points confirmed **Homoscedasticity**, meaning our model is reliable across all price ranges.
* **Final Verdict:** Our final model achieved a **97.96% accuracy rate**, with an average deviation of only **$3.30**. This demonstrates that while the stock market is volatile, high-frequency intraday movements follow a strong linear trend that can be captured through rigorous regression analysis.



---
**Course:** B.Tech (6th Semester)  
**Project:** Machine Learning - Stock Market Forecasting
