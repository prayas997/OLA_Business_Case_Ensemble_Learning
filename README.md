OLA Driver Churn Prediction — Case Study
A Data Science Project to Understand Why Drivers Leave & How to Retain Them

📌 1. Project Overview
Driver churn (drivers leaving the platform) is a major challenge for ride-hailing companies like OLA. Hiring new drivers is expensive, and sudden drop-outs affect customer experience and business operations.
This project aims to predict whether a driver is likely to leave OLA, based on:
* Driver demographics (Age, Gender, Education, City)
* Job details (Joining designation, Grade, Tenure)
* Performance history (Quarterly rating, Business value generated)
* Income patterns (Monthly income, income increase)
By predicting churn early, companies can take preventive actions to retain drivers.

📊 2. Business Goal
The goal is simple:
Identify drivers who are at high risk of leaving, so the company can intervene early.
Examples of interventions:
* Offer support or training
* Adjust incentives
* Improve engagement with drivers
* Resolve operational issues

📂 3. What’s in the Dataset?
Each row represents a driver in a specific month, containing:
* Personal details: Age, Gender, City
* Job details: Joining date, Last working date, Grade
* Performance: Quarterly rating, Total business value
* Income: Monthly income
We created additional useful features such as:
* Quarterly rating increase
* Income increase
* Performance decline
* Tenure (days/months)
* Average rating per driver
* Income stability (variance)

🔧 4. Steps Performed in the Project
✔️ Data Cleaning
* Handled missing values
* Fixed messy date formats
* Corrected negative tenure values where needed
* Encoded categorical columns
✔️ Feature Engineering
Added features that help the model understand:
* Driver performance trend
* Income pattern
* Stability over time
* Driver tenure
* Business contribution
✔️ Handling Class Imbalance
Drivers who leave are very few compared to those who stay. Used:
* SMOTE
* Class weighting to balance the data during training.
✔️ Model Building
Tried multiple models:
* Decision Tree
* Random Forest
* XGBoost (best performing)
✔️ Best Model
XGBoost with tuned parameters and class weights
* Excellent at identifying minority churn cases
* Balanced precision & recall
* AUC around 0.87

⭐ 5. Key Insights from the Model
The features that help most in predicting churn:
1. Quarterly Rating — strongest signal of driver engagement
2. Gender — significant behavioral differences observed
3. Business Value — low business value often precedes churn
4. Performance Decline — sudden rating drops predict exits
5. Income Increase / Stability — unstable earnings lead to churn

📈 6. Model Evaluation
* Accuracy: ~80%
* AUC: 0.87
* Model catches 82% of drivers who churn, which is crucial for retention.

📝 7. Actionable Business Recommendations
1. Focus on low-rating drivers Engage early when rating drops — coaching, support, feedback calls.
2. Detect income instability Drivers with fluctuating or decreasing income tend to leave.
3. Monitor business value decline Drivers whose demand drops may require route optimisation or incentives.
4. City-wise retention strategy Certain cities show higher churn — tailor driver support regionally.

🧠 8. Why This Project Matters
This project shows how data science can help:
* Reduce driver churn
* Improve platform reliability
* Lower hiring and training costs
* Enhance driver satisfaction

🚀 9. Tech Stack Used
* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn
* SMOTE for balancing
