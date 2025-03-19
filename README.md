# Tiatanic_EDA_Practice_Project

# 📌 Overview
This project explores the Titanic dataset using Exploratory Data Analysis (EDA) techniques in Python with Seaborn and Pandas. We analyze survival rates based on passenger demographics, ticket class, fare, family relations, and embarkation points. Various visualizations and statistical methods are used to uncover patterns in the data.

# 🎯 Objective
Understand the distribution of passengers based on class, age, gender, and embarkation points.

Analyze the impact of gender, age, family size, and ticket class on survival rates.

Identify outliers and handle missing values.

Use data visualizations (heatmaps, violin plots, swarm plots, box plots) to present findings.

# 📊 Dataset Details
Source: Seaborn's built-in Titanic dataset

Columns:

survived: Survival status (0 = No, 1 = Yes)

pclass: Passenger class (1 = First, 2 = Second, 3 = Third)

sex: Gender of the passenger

age: Age of the passenger

sibsp: Number of siblings/spouses aboard

parch: Number of parents/children aboard

fare: Ticket fare

embarked: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)

deck: Cabin deck (many missing values, dropped in analysis)

# 📈 EDA Steps
1.Data Exploration

df.info(), df.describe(), df.isnull().sum() to check missing values and data types.

Identified missing values in age, embarked, and deck.

2.Data Cleaning & Imputation

Age: Filled missing values using groupby(['pclass', 'sex'])['age'].median().

Embarked: Filled missing values with mode (C).

Deck: Dropped due to excessive missing data.

Duplicates: Removed duplicate records.

3.Outlier Handling

Identified outliers in fare and age using IQR.

Removed fare outliers separately by Pclass.

4.Feature Engineering

Created age_group column.

Added family_size (sibsp + parch + 1) and alone (whether traveling solo).

5.Survival Rate Analysis

pclass, sex, age, family_size, embarked, and fare impact on survival.

# 📊 Key Insights

✅ Women had a higher survival rate than men in all classes.
✅ Children (0-10 years) had the best survival chances.
✅ Passengers in 1st class had the highest survival rate (~64%).
✅ Solo travelers had lower survival rates than family travelers.
✅ Higher fare passengers had better survival chances.
✅ Passengers who embarked from Cherbourg had higher survival rates.
✅ Missing cabin info correlated with lower survival rates.


# 🛠 How to Run the Project

Requirements

Ensure you have Python installed along with the following libraries:

pip install pandas seaborn matplotlib numpy


#📜 Conclusion

This project provides an in-depth Exploratory Data Analysis (EDA) on the Titanic dataset using Seaborn. Various patterns in survival rates based on age, gender, class, fare, and family structure have been explored. The findings could be used for predictive modeling in future projects.

