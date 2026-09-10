Student Habits & Performance — Machine Learning

A complete Machine Learning project analyzing the relationship between student habits and academic performance.

The project uses exploratory data analysis, data preprocessing, Linear Regression, and Logistic Regression to understand and predict student exam performance.

Project Overview

The objective of this project is to investigate how different student habits and lifestyle factors are associated with academic performance.

Two Machine Learning tasks are performed:

1. Regression: Predict the student's "exam_score".
2. Classification: Predict whether a student will Pass or Fail based on a threshold of 50 marks.

Dataset

Dataset: "Day18_19_student_habits_performance.csv"

The dataset contains information about student habits, lifestyle, and academic performance.

Key variables include:

- Study hours per day
- Sleep hours
- Social media usage
- Netflix usage
- Exercise frequency
- Mental health rating
- Attendance
- Parental education level
- Exam score

The dataset contains approximately 1,000 student records and 16 columns.

Project Workflow

1. Exploratory Data Analysis

- Load and inspect the dataset
- Check dataset shape
- Inspect data types
- Identify missing values
- Check duplicate records
- Generate descriptive statistics
- Visualize the distribution of exam scores
- Analyze numerical correlations
- Generate a correlation heatmap

2. Data Preprocessing

- Separate features and target variables
- Remove the student identifier
- Handle missing numerical values
- Impute missing categorical values
- Apply One-Hot Encoding to categorical features
- Split the dataset into training and testing sets
- Standardize features for Logistic Regression

3. Regression — Exam Score Prediction

A Linear Regression model is trained to predict continuous exam scores.

Evaluation metrics:

- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

4. Classification — Pass/Fail Prediction

A Logistic Regression model is used to classify students as:

- "Pass" — exam score ≥ 50
- "Fail" — exam score < 50

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

Results

The reference model run produced approximately:

Model| Metric| Training| Testing
Linear Regression| R²| 0.9021| 0.8968
Linear Regression| MAE| 4.21| 4.19
Linear Regression| RMSE| 5.34| 5.15
Logistic Regression| Accuracy| 96.25%| 93.50%
Logistic Regression| Precision| 97.04%| 96.49%
Logistic Regression| Recall| 98.71%| 95.93%
Logistic Regression| F1-score| 97.87%| 96.21%

The relatively small difference between training and testing performance suggests that neither model shows strong evidence of overfitting.

Key Insights

1. Study time has the strongest relationship with exam performance

"study_hours_per_day" shows a strong positive relationship with "exam_score", with a correlation of approximately 0.83.

2. Mental health is positively associated with performance

"mental_health_rating" has a positive relationship with exam scores, suggesting that student well-being is relevant to academic outcomes.

3. Entertainment screen time has a negative relationship with performance

Both social media usage and Netflix usage show negative correlations with exam scores.

4. Exercise and sleep have smaller positive relationships

Exercise frequency and sleep hours show positive but weaker relationships with exam performance compared with study time.

5. The classification model performs well

The Logistic Regression classifier achieved approximately 93.5% test accuracy, with precision, recall, and F1-score all above 95% in the reference run.

Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook / Google Colab

Machine Learning Algorithms

Linear Regression

Used for predicting the continuous "exam_score".

Logistic Regression

Used for binary Pass/Fail classification.

Repository Structure

student-habits-performance-ml/
│
├── Day18_19_Student_Performance_ML_Complete.ipynb
├── README.md
├── .gitignore
└── LICENSE

The dataset may be kept outside the repository if it is provided as course/LMS material or if redistribution is not permitted.

How to Run

Google Colab

Upload the notebook and dataset to Google Colab, then run the cells sequentially.

Local Jupyter Notebook

Install the required dependencies:

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

Then launch Jupyter:

jupyter notebook

Open:

Day18_19_Student_Performance_ML_Complete.ipynb

Make sure the CSV dataset is located in the same directory as the notebook.

Disclaimer

This project is intended for educational and Machine Learning practice purposes.

Correlation and model predictions indicate statistical relationships and predictive patterns; they should not be interpreted as proof of causation.