📊 Banking Transaction Anomaly Detection using Data Analysis
📌 Project Overview
Banking fraud often goes undetected due to hidden patterns in large volumes of transaction data. This project focuses on identifying suspicious or anomalous transactions using data analysis and statistical techniques.

Instead of relying on predefined fraud rules, this project uses Exploratory Data Analysis (EDA) and outlier detection methods to highlight unusual transaction behavior.

🎯 Problem Statement
How can unusual transaction patterns be identified using data analysis techniques before fraud is officially confirmed?

🔄 Data Science Lifecycle
1. Question
Identify suspicious transactions based on abnormal patterns.

2. Data
Transaction dataset containing:

Transaction ID

User ID

Transaction Amount

Time

Location

Transaction Type

3. Insight
Detect anomalies and derive meaningful insights about fraud-like behavior.

📂 Project Structure
project/
│
├── data/
│   ├── raw/                # Original dataset
│   ├── processed/          # Cleaned dataset
│
├── notebooks/
│   └── analysis.ipynb      # Main analysis notebook
│
├── src/
│   └── utils.py            # Helper functions
│
├── outputs/
│   ├── plots/              # Generated graphs
│   └── reports/            # Final insights
│
└── README.md
⚙️ Technologies Used
Python

Jupyter Notebook

NumPy

Pandas

Matplotlib

Seaborn

🧪 Data Processing Steps
🔹 Data Loading
Loaded CSV dataset using Pandas

🔹 Data Cleaning
Handled missing values using fill/drop methods

Removed duplicate records

Standardized column names

🔹 Data Transformation
Converted time columns into usable formats

Structured data for analysis

📊 Exploratory Data Analysis (EDA)
🔸 Summary Statistics
Mean, median, standard deviation of transaction amounts

Distribution of transactions across users

🔸 Visualizations
📉 Histogram
Shows distribution of transaction amounts

📦 Boxplot
Identifies outliers (important for anomaly detection)

📈 Line Plot
Shows transaction trends over time

🔵 Scatter Plot
Relationship between transaction variables

🚨 Anomaly Detection Approach
This project uses statistical methods instead of complex machine learning models.

✅ IQR Method (Interquartile Range)
Q1 = 25th percentile

Q3 = 75th percentile

IQR = Q3 - Q1

Rule:

Lower Bound = Q1 - 1.5 * IQR  
Upper Bound = Q3 + 1.5 * IQR  
Transactions outside this range are considered anomalies.

✅ Z-Score Method
Measures how far a value is from the mean

Rule:

|Z-score| > 3 → potential anomaly

📌 Key Insights
Most transactions fall within a normal range, but a small percentage show extreme values

High-value transactions are rare and may indicate risk

Some users exhibit unusual spending spikes

Transactions at odd hours show higher anomaly probability

⚠️ Assumptions
High transaction amounts may indicate suspicious activity

Unusual patterns are treated as potential anomalies

Dataset represents realistic banking behavior

🚧 Limitations
No real-time detection (batch analysis only)

No labeled fraud data (unsupervised detection)

Statistical methods may flag false positives

🚀 Future Improvements
Integrate machine learning models (Isolation Forest, Autoencoder)

Build real-time fraud detection system

Add user behavior profiling

Create interactive dashboard using React
