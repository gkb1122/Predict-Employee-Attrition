🔍 Employee Attrition Prediction with Explainable Machine Learning
This project explores employee attrition using machine learning models and interpretable AI techniques. The goal is not just to predict who might leave a company, but to understand why. The analysis is powered by the IBM HR Analytics Employee Attrition dataset, and visualized using tools like SHAP and Seaborn.

📂 Dataset Overview
Source: IBM HR Analytics Employee Attrition & Performance

Records: ~1,470 employees

Features: Includes demographics, job roles, compensation, work environment, performance ratings, and more

Target: Attrition (Yes/No)

⚙️ Preprocessing Steps
Missing Values: Dataset is clean with no nulls.

Encoding: Categorical features were label-encoded using LabelEncoder.

Scaling: Numerical features were standardized using StandardScaler.

EDA: Used histograms, box plots, count plots, and correlation heatmaps to uncover trends.

🧠 Models Implemented
1. Logistic Regression
Simple, interpretable baseline model.

Good for binary classification tasks like attrition prediction.

2. Random Forest Classifier
Handles non-linear relationships.

Provides built-in feature importance.

Performs better on imbalanced datasets compared to logistic regression.

Evaluation Metrics:
Accuracy

Precision, Recall, F1-score

Confusion Matrix

📊 Explainability with SHAP
To interpret the model's predictions, SHAP (SHapley Additive exPlanations) was used:

SHAP summary plot reveals top features driving attrition.

Feature importance ranked by average SHAP impact across samples.

Top drivers identified:

MonthlyIncome

Age

TotalWorkingYears

OverTime

JobRole

🧩 Challenges & Solutions
SHAP value mismatch: Ensured test data was converted back to a DataFrame with column names after scaling.

Shape alignment: Added shape verification and defensive programming to handle feature count mismatches gracefully.

Model explainability: Used TreeExplainer with SHAP for better compatibility with Random Forest.

📌 Key Takeaways
Employees with lower income, more overtime, and fewer years of experience are more likely to leave.

Explainable ML can help HR teams make informed, proactive retention strategies.

SHAP provides transparency into model decision-making.

🛠️ Technologies Used
Python 3.x

Pandas, NumPy, Seaborn, Matplotlib

Scikit-learn

SHAP

Google Colab

🚀 How to Run
Upload the dataset in Colab.

Run the notebook cell-by-cell.

SHAP visualizations will show after model training.


📃 License
This project is licensed under the MIT License. See LICENSE for more information.

