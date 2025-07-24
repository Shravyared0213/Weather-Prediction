**🌤️ Weather Classification Analysis & Modeling
📌 Project Overview**
This notebook aims to:
Perform exploratory analysis on a weather dataset.
Understand the distribution, outliers, and skewness in variables.
Preprocess the data to handle skewness and remove outliers.
Train and evaluate multiple machine learning models to classify weather types.

**📁 Dataset Summary**
File: Weather.csv
Observations: 1461 rows × 6 columns

**Features:**

date (datetime)

precipitation, temp_max, temp_min, wind (continuous)

weather (categorical target)

**🔧 Libraries Used**
python
Copy
Edit
pandas, numpy, seaborn, matplotlib, scipy, sklearn

**🔍 Data Analysis Highlights**
🟡 Categorical Analysis

Count plot of weather types.

Percent distribution of:

Rain: ~43.87%

Sun: ~43.80%

Drizzle: ~3.63%

Snow: ~1.78%

Fog: ~6.91%

**🔵 Numerical Feature Exploration**
Descriptive stats and histogram plots for:

precipitation, temp_max, temp_min, wind

Skewness analysis using:

Violin plots

Boxplots grouped by weather

**🔴 Correlation Analysis**

Pearson correlation

T-tests to assess statistical significance between numerical variables.

Heatmap showing positive correlation between temp_max and temp_min.

**⚙️ Data Preprocessing**

Dropped date column (not relevant to prediction).

Removed outliers using IQR filtering on numerical features.

Skewness correction applied:

Square root transformation on precipitation and wind.

Label encoding applied on the weather column to convert it into numerical classes.

**🎯 Machine Learning**
🧪 Feature and Target Split

python

Copy
Edit

X = all columns except "weather"  
y = "weather"
train_test_split() used with test size = 10%

**✅ Models Trained & Accuracy Scores**

Model	Accuracy

K-Nearest Neighbors	58.70%

Support Vector Classifier	50.72%

Gradient Boosting Classifier	71.74%

Random Forest Classifier	76.81%
**
**📌 Conclusion****
Random Forest achieved the highest accuracy of 76.81%, followed by Gradient Boosting.

Random Forest outperformed other models likely due to its robustness to skewed distributions and outliers, and its ability to generalize well on unscaled, mixed-type data.

Data transformation, outlier removal, and encoding were key to model performance.

The categorical target (weather) was effectively predicted using ensemble classifiers.

