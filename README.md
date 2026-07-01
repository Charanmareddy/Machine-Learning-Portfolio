# 🤖 Machine Learning Portfolio

Welcome to my centralized Machine Learning repository. This project serves as an end-to-end implementation log of various machine learning algorithms, data engineering pipelines, and statistical modeling workflows.

---

## 🛠️ Tech Stack & Core Libraries
* **Language:** Python 3.x
* **Data Manipulation & Analytics:** Pandas, NumPy
* **Machine Learning Frameworks:** Scikit-Learn
* **Data Visualization:** Matplotlib

---

## 📂 Repository Architecture & Core Algorithms

I am developing and pushing my implementations modularly. Below is the current tracking index of the portfolio:

| Module / Algorithm | Dataset Used | Objective / Target | Status |
| :--- | :--- | :--- | :--- |
| [📂 Linear Regression](./Linear_Regression) | Salary & Student Performance | Predict numerical targets using Ordinary Least Squares | ✅ Completed |
| [📂 Polynomial Regression](./Polynomial_Regression) | Ice Cream Revenue | Preprocess features to capture non-linear relationships | ✅ Completed |
| 📂 Logistic Regression | *Pending* | *Classification tasks* | ⏳ Upcoming |
| 📂 Decision Trees & Random Forest | *Pending* | *Supervised learning tasks* | ⏳ Upcoming |
| 📂 Clustering (K-Means) | *Pending* | *Unsupervised segmentation* | ⏳ Upcoming |

*Note: Click on the active module links to navigate directly to the specific code directories.*

---

## 📈 Detailed Project Log: Linear Regression Module

The active Linear Regression directory contains two distinct practical notebooks evaluating feature correlation matrices and target mapping formulas.

### 1. Salary Prediction Model (`salary.ipynb`)
* **Objective:** Predict an employee's salary based on years of industry experience.
* **Key Features:** `YearsExperience` (Independent), `Salary` (Dependent/Target).
* **Statistical Insights:** * Features are strongly linearly correlated ($r \approx 0.978$).
  * **Intercept ($\beta_0$):** `25,321.58` (Base salary for a fresher with 0 years of experience).
  * **Slope ($\beta_1$):** `9,423.81` (Expected salary increase for every additional year of experience).
* **Model Accuracy ($R^2$ Score):** **`0.9645` (96.45%)** on training data.

### 2. Student Performance Index Model (`Student_Performance.ipynb`)
* **Objective:** Forecast a student's academic performance index based on various study metrics.
* **Key Features:** `Hours Studied`, `Previous Scores`, `Sleep Hours`, `Sample Question Papers Practiced` (Target: `Performance Index`).
* **Statistical Insights:** * Incredibly high multi-variable relationship. `Previous Scores` holds the strongest direct correlation matrix weight ($r \approx 0.915$).
* **Model Validation Metrics:**
  * **Training $R^2$ Score:** `0.9884` (98.84%)
  * **Testing $R^2$ Score:** **`0.9887` (98.87%)**
  * **Root Mean Squared Error (RMSE):** `2.045` marks variance on test splits.
  * **Mean Absolute Error (MAE):** `1.629` marks on test predictions.

### 3. Polynomial Regression: Ice Cream Revenue (`ice_cream.ipynb`)
* **Objective:** Predict cafe/stand revenue based on the ambient outside temperature.
* **Key Features:** `Temperature` (Independent Feature), `Revenue` (Dependent/Target).
* **Engineering Standard:** Utilized Scikit-Learn's `PolynomialFeatures` preprocessing framework. This converts a simple linear array $[x]$ into higher-degree combinations $[1, x, x^2, \dots, x^n]$ to map curvilinear data patterns that standard Ordinary Least Squares (OLS) cannot capture effectively.
* **Pipeline Goal:** Prevents underfitting by allowing a linear model to natively fit non-linear curves without losing the interpretability of standard regression coefficients.

---

## 🚀 Local Deployment Setup

To clone this repository and run any of the active modules locally, execute the following commands in your terminal:

```bash
# Clone the portfolio
git clone [https://github.com/your-username/your-repo-name.git](https://github.com/your-username/your-repo-name.git)

# Change into the project root directory
cd your-repo-name

# Install the required scientific stack dependencies
pip install pandas scikit-learn matplotlib