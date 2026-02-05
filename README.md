📘 Internet Usage Behavior Analysis — EDA & Machine Learning Project
📝 Project Overview

This project analyzes daily internet usage patterns across different age groups using Exploratory Data Analysis (EDA) and Machine Learning.
The goal is to understand digital behavior, predict screen time, and segment users into meaningful groups based on usage patterns.

The dataset contains 2,800 user records with features such as:

Age & Age Group

Social media hours

Work/study hours

Entertainment hours

Primary device

Internet type

Total daily screen time

This project demonstrates end-to-end data analytics and machine learning workflow suitable for a data analyst or ML beginner portfolio.

🎯 Objectives

Perform detailed Exploratory Data Analysis

Identify insights on digital behavior

Build ML models:

Regression → Predict total screen time

Classification → Predict high vs low screen time

Clustering → Segment users into usage personas

Visualize patterns and model results

Communicate clear insights and findings

📂 Project Structure
internet-usage-analysis/
│
├── daily_internet_usage_by_age_group.csv
├── internet_usage_analysis.ipynb
├── README.md
└── images/           (optional — contains visualization exports)

🛠️ Technologies Used

Python

Pandas, NumPy

Matplotlib, Seaborn

Scikit-learn

Jupyter Notebook

🔍 Exploratory Data Analysis (EDA)
Key observations:

Younger users (ages 13–25) have the highest total screen time.

Older users (ages 46+) show conservative digital behavior.

Mobile is the most commonly used primary device.

Strong correlations exist between:

social media hours

work/study hours

entertainment hours
And total screen time.

Visualizations included:

Histogram of total screen time

Screen time by age group

Device usage distribution

Correlation heatmap

Age vs social media scatter plot

🤖 Machine Learning Models
1. Regression — Predicting Total Screen Time

To avoid data leakage, the following columns were removed:

social_media_hours

work_or_study_hours

entertainment_hours
Because these directly sum into the target.

Final Performance:

MAE: ~1.08 hours

R² Score: ~0.67

Interpretation:
Demographic and device features moderately predict screen time when behavioral features are excluded.

2. Classification — High vs Low Screen Time

high_screen_time was created using:

1 → if total_screen_time > median  
0 → otherwise


After removing leakage sources, the classification model achieved:

Accuracy: ~0.51

Low precision/recall

Confusion matrix shows balanced misclassifications

Interpretation:
Demographics alone are not strong predictors of screen time category.
This is realistic for behavioral datasets.

3. Clustering — User Segmentation (KMeans)

Three user groups were identified using:

age

social_media_hours

work_or_study_hours

entertainment_hours

Cluster Personas
Cluster	Avg Age	Characteristics	Label
2	~20.7	Balanced study + entertainment + SM usage	Young Active Users
1	~40.2	Highest work/study hours, moderate entertainment	Mid-Age Professional Users
0	~63.6	Conservative and stable usage patterns	Older Practical Users
📈 Visualizations

The notebook includes:

Distribution plots

Bar charts

Correlation heatmap

Scatter plots

Regression: Actual vs Predicted

Classification: Confusion Matrix

Clustering: 2D & 3D cluster plots

🧠 Key Insights

Teens and young adults dominate digital engagement.

Older individuals have more stable and conservative internet habits.

Regression model performs reasonably well without behavioral leakage.

Classification model shows that demographics alone cannot classify screen time accurately.

Clustering clearly separates users into meaningful behavioral groups.

🧩 Skills Demonstrated

Data Cleaning

Feature Engineering

Leakage Detection & Prevention

Regression & Classification Modeling

KMeans Clustering

Visualization & Insight Communication

Notebook Structuring

End-to-End Analytics Workflow

▶️ How to Run the Project
1. Clone the repository:
git clone https://github.com/<your-username>/internet-usage-analysis.git

2. Install dependencies:
pip install -r requirements.txt

3. Open Jupyter Notebook:
jupyter notebook

4. Run internet_usage_analysis.ipynb
👤 Author

SHAIK TASLEEM
Aspiring Data Analyst | Machine Learning Enthusiast
Email: tasleem1911@gmail.com

🚀 Future Improvements

Build Power BI / Tableau dashboard

Improve classification model using more behavioral features

Try Random Forest & XGBoost models

Implement feature selection & hyperparameter tuning
