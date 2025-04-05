# basic-data-analysis-assignment-


# Import necessary libraries
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# 1. Data Loading and Exploration
# Load dataset
data = pd.read_csv('your_data.csv')  # Replace with your actual file path

# Display first few rows of the data
print("First 5 rows of the data:")
print(data.head())

# Check for missing values
print("\nMissing values in each column:")
print(data.isnull().sum())

# Check the data types of the columns
print("\nData types of each column:")
print(data.dtypes)

# Summary statistics
print("\nSummary statistics of the data:")
print(data.describe())

# 2. Basic Data Analysis
# Example: Calculate mean, median, and mode for a specific column (e.g., 'age')
mean_age = data['age'].mean()  # Replace 'age' with your actual column name
median_age = data['age'].median()
mode_age = data['age'].mode()[0]

print(f"\nMean Age: {mean_age}")
print(f"Median Age: {median_age}")
print(f"Mode Age: {mode_age}")

# 3. Visualizations
# Histogram for a specific column (e.g., 'age')
plt.figure(figsize=(8, 6))
sns.histplot(data['age'], kde=True)  # Replace 'age' with your actual column name
plt.title('Age Distribution')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()

# Scatter plot between two variables (e.g., 'age' and 'salary')
plt.figure(figsize=(8, 6))
sns.scatterplot(x='age', y='salary', data=data)  # Replace with your actual columns
plt.title('Age vs Salary')
plt.xlabel('Age')
plt.ylabel('Salary')
plt.show()

# Correlation heatmap
plt.figure(figsize=(10, 8))
sns.
