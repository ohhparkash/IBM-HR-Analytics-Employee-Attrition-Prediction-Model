# IBM-HR-Analytics-Employee-Attrition-Prediction-Model
📌 Project Overview
Employee attrition (turnover) represents a significant hidden cost for organizations, involving recruitment expenses, loss of institutional knowledge, and decreased team morale. This project aims to move HR departments from a reactive approach (exit interviews) to a proactive strategy.

Using the IBM HR Analytics dataset, I developed a machine learning solution that functions as an "early-warning system" to identify high-risk employees and uncover the specific organizational factors driving them to leave.

⚖️ The Classification Problem
The core of this project is a Binary Classification task. The objective is to predict a target variable with two possible outcomes:
- Attrition = 'Yes': The employee is likely to resign.
- Attrition = 'No': The employee is likely to stay.

A major technical challenge was the class imbalance within the dataset (84% 'Stay' vs. 16% 'Leave'). A standard model would achieve high accuracy by simply guessing 'Stay' for everyone, failing to identify the actual leavers. This project focuses on optimizing Recall and F1-Score to ensure at-risk employees are correctly identified.

🛠️ Methodology & Technical Workflow
Data Preprocessing: * Cleaned the dataset and removed non-predictive features (e.g., Employee ID).
Encoded categorical variables (Department, Job Role, Overtime) into numerical format for model compatibility.
- Model Selection:
Implemented a Random Forest Classifier. This ensemble method was chosen for its robustness, ability to handle non-linear relationships, and its built-in capability to rank feature importance.

- Handling Imbalance:
Utilized SMOTE (Synthetic Minority Over-sampling Technique) to balance the training data. This allowed the model to learn the distinct patterns of the 'Leave' class, improving the detection rate of potential resignations by nearly 3x.

- Evaluation:
Evaluated performance using a Confusion Matrix and Classification Report, prioritizing the model's ability to "catch" leavers rather than just overall accuracy.

📊 Key Insights & Results
The model revealed that attrition is not random; it is driven by specific, measurable factors. The Top 3 Drivers of Attrition identified were:
- Overtime: Employees working frequent overtime showed the highest risk of departure.
- Monthly Income: Competitive compensation remains a primary factor in retention.
- Total Working Years: Employees earlier in their career paths or with fewer years at the company were more likely to churn.

💻 Tech Stack
- Language: Python
- Libraries: Pandas, NumPy, Scikit-learn, Imbalanced-learn (SMOTE)
- Visualization: Matplotlib, Seaborn
