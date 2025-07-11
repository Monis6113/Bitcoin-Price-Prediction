# Bitcoin-Price-Prediction

# Objective:

In this hands-on project, I stepped into the role of a data analyst exploring cryptocurrency market trends to help investors make more informed decisions. The goal was to analyze historical Bitcoin price data, engineer meaningful features, and develop machine learning models that predict whether buying Bitcoin on a given day could be profitable.

**Dataset Overview**

The dataset consists of eight years of daily Bitcoin OHLC data:

**Price Metrics:** Open, High, Low, Close, Adj Close

**Time Variables:** Date (split into year, month, day)

**Derived Metrics:** Open-Close difference, Low-High difference, Quarter-end flags, Target signal

# Approach

**1. Data Exploration**

Loaded and examined data shape, types, and descriptive statistics.

Checked for null values and redundant columns (e.g., removed Adj Close).

Visualized closing price trends over time to identify market cycles and volatility.

**2. Exploratory Data Analysis (EDA)**

Plotted distributions and boxplots for OHLC prices to detect outliers.

Created bar plots of average prices by year to reveal long-term trends.

Analyzed price variations during quarter ends to detect seasonal effects.

**3. Feature Engineering**

Derived new features like open-close and low-high to capture daily price movements.

Added is_quarter_end to test for periodic effects.

Created a binary target variable to signal whether the next day’s close price was higher.

**4. Correlation & Data Prep**

Used a heatmap to check for highly correlated features.

Normalized features with StandardScaler for stable model training.

Split the data into training (70%) and validation (30%) sets.

**5. Model Development & Evaluation**

Trained Logistic Regression, SVM (Polynomial Kernel), and XGBoost classifiers.

Evaluated each model using ROC-AUC scores to assess how well they distinguish profitable trades.

Visualized prediction performance with confusion matrices.

# Key Insights

Feature engineering significantly improved model interpretability, adding practical signals like day-over-day price differences and quarter-end flags.

XGBoost achieved high training accuracy but showed signs of overfitting; Logistic Regression delivered more stable performance on unseen data.

Visual EDA highlighted extreme price volatility in recent years, aligning with known market events like the 2021 Bitcoin surge.

# Tools & Libraries Used

**Python:** Core scripting language

**pandas, numpy:** Data cleaning and manipulation

**matplotlib, seaborn:** Visualization

**scikit-learn:** Data preprocessing, modeling, and evaluation

**XGBoost:** Gradient boosting for high-accuracy predictions

# Outcome 

This project strengthened my ability to clean and analyze time-series financial data, engineer predictive features, and compare models for practical deployment. It also helped me simulate a product analyst mindset by turning raw historical data into actionable trading signals—bridging the gap between data analysis and real-world business strategy.
