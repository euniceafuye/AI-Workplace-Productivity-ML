# AI-Enhanced Workplace Productivity: A Comparative Model Study

This project analyzes the impact of Artificial Intelligence on employee productivity through a comparative Machine Learning approach. The main goal is to predict the **Productivity Score** of employees by benchmarking various regression algorithms to identify the one with the highest predictive power and best generalization.

## 📊 Project Objective
The focus of this project is to evaluate and compare multiple Machine Learning models. By testing different architectures—ranging from simple linear models to complex ensemble methods—I aimed to determine the most effective way to capture the relationship between AI usage, work habits, and output.

## 🛠️ Machine Learning Pipeline
A rigorous workflow was followed to ensure a fair comparison between models:

1. **Data Integration**: Merged feature sets (job roles, experience, AI usage hours) with productivity targets using `Employee_ID`.
2. **Exploratory Data Analysis (EDA)**: 
   * Visualized missing data patterns using the `missingno` library.
   * Analyzed correlations between AI tools and workplace performance.
3. **Preprocessing**: 
   * Handled missing values via mean imputation.
   * Applied log transformations to skewed features (e.g., meeting hours).
   * Implemented One-Hot Encoding for categorical variables.
4. **Feature Selection**: Removed identifiers and high-leakage variables (like `burnout_risk_score`) to ensure models learned generalizable patterns.

## 🏆 Model Benchmarking & Results
I trained and evaluated the following regression algorithms:
* **Linear Regression**: Used as the baseline for interpretability.
* **XGBoost Regressor**: To capture complex non-linear relationships.
* **Random Forest Regressor**: For robust ensemble-based learning.
* **K-Nearest Neighbors (KNN)**: For a similarity-based approach.

### The Winner: Linear Regression
After evaluating performance metrics (MAE, RMSE, and R²), **Linear Regression** emerged as the final choice, providing the best balance between prediction accuracy and model stability for this specific dataset.

* **Final R² Score**: **0.6735** (The model explains ~67% of the variance).
* **MAE**: 6.43
* **RMSE**: 8.06

## 📈 Performance Evaluation
The selected model was validated through:
* **Learning Curves**: Confirming high and converging performance on both training and validation sets (indicating low bias and low variance).
* **Residual Analysis**: Confirming that residuals are centered around zero with no systematic patterns, ensuring the model is not biased.

## 📂 Repository Structure
* `Notebook 1.ipynb`: Full Python code for model comparison and evaluation.
* `ai_productivity_features.csv`: Dataset containing employee attributes.
* `ai_productivity_targets.csv`: Dataset containing target productivity scores.

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/yourusername/ai-workplace-productivity.git](https://github.com/yourusername/ai-workplace-productivity.git)
