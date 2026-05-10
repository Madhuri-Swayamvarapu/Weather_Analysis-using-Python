
**🌦️ Weather Data Analysis using Pandas**

**📌 Project Overview**

This project focuses on analyzing a real-world weather dataset using Python and the Pandas library. The dataset contains hourly weather observations including temperature, humidity, wind speed, visibility, pressure, and different weather conditions.

The main objective of the project is to perform Exploratory Data Analysis (EDA) to understand weather patterns, clean and organize the dataset, and extract meaningful insights using various Pandas operations.

Through this project, different data analysis techniques such as filtering, grouping, aggregation, statistical analysis, and handling missing values are implemented in a simple and efficient manner.

📂 **Dataset Description**

The dataset used in this project is a time-series weather dataset containing hourly recorded weather information.

The dataset includes the following attributes:
Temperature
Dew Point Temperature
Relative Humidity
Wind Speed
Visibility
Pressure
Weather Conditions

Each row in the dataset represents weather information recorded for a specific hour.

The dataset helps in analyzing:

Weather condition trends
Temperature variations
Wind speed distribution
Humidity levels
Visibility changes during different weather conditions

**🛠️ Technologies Used**
Python 🐍

Python is used as the programming language for performing data analysis and manipulation.

Pandas 📊

Pandas is the primary library used for:

Data cleaning
Data filtering
Statistical analysis
Grouping and aggregation
Handling missing values
Jupyter Notebook

**Jupyter Notebook is used as the development environment to write and execute Python code interactively.**

🔍 Work Done in the Project
📊 Data Loading and Exploration

The first step in the project was loading the weather dataset into a Pandas DataFrame using:

import pandas as pd
data = pd.read_csv("Weather Data.csv")

After loading the dataset, basic exploration was performed to understand the structure of the data.

Operations Performed:
Viewing first rows of dataset
data.head()

This helps in checking:

Column names
Data formatting
Sample records
Checking dataset dimensions
data.shape

This operation gives:

Total number of rows
Total number of columns
Displaying column names
data.columns

Used to identify all available features in the dataset.

Checking data types
data.dtypes

Helps in understanding:

Integer columns
Float columns
Object/string columns
Dataset summary using .info()
data.info()

**Provides:**

Non-null values
Memory usage
Datatype summary
📈 Data Analysis Techniques Used
🔹 Finding Unique Values

**The project identifies unique weather conditions using:**

data['Weather Condition'].unique()

This helps in understanding all weather types present in the dataset such as:

Clear
Cloudy
Snow
Rain
Fog
🔹 Counting Unique Values
data.nunique()

Used to calculate the number of unique entries in each column.

🔹 Value Counting
data['Weather Condition'].value_counts()

This operation counts how many times each weather condition occurs.

It helps in identifying:

Most common weather condition
Least occurring condition
📉 Handling Missing Values

The dataset was checked for missing values using:

data.isnull().sum()

This identifies columns containing null or missing data.

To verify non-null values:

data.notnull().sum()

Handling missing values is important because:

It improves analysis accuracy
Prevents errors during computation
📊 Statistical Analysis Performed
🔹 Mean Calculation

Average values were calculated using:

data.mean()

**This helps in finding:**

Average temperature
Average humidity
Average wind speed
🔹 Standard Deviation
data.std()

Used to measure variation in weather data.

A high standard deviation indicates:

Large fluctuations in weather conditions
🔹 Variance Calculation
data.var()

Variance measures data spread and variability.

📊 Data Filtering Operations

Several filtering operations were performed to extract specific weather information.

🔹 Filtering Wind Speed
data[data['Wind Speed_km/h'] == 4]

This retrieves records where wind speed equals 4 km/h.

🔹 Filtering Snow Conditions
data[data['Weather Condition'].str.contains('Snow')]

Used to identify all weather records containing snow-related conditions.

🔹 Multiple Condition Filtering

Conditions can also be combined using logical operators like:

AND (&)
OR (|)

This helps in detailed weather analysis.

📊 Grouping and Aggregation

Grouping is one of the most important parts of the project.

🔹 Grouping by Weather Condition
data.groupby('Weather Condition').mean()

This calculates average values for:

Temperature
Humidity
Wind speed
Visibility

for each weather condition separately.

Example:
Average temperature during Snow
Average humidity during Clear weather

Grouping helps in comparative analysis between different weather conditions.

📊 Column Renaming

Columns were renamed for better readability using:

data.rename(columns={'Weather':'Weather Condition'})

**Renaming improves:**

Code readability
Understanding of dataset columns
📌 Key Insights Obtained
✔️ Clear weather conditions occurred most frequently.
✔️ Snow conditions showed lower temperatures and visibility.
✔️ Wind speed varied significantly across weather types.
✔️ Grouping operations helped identify average weather behavior.
✔️ Statistical analysis provided understanding of data distribution.
✔️ Pandas simplified complex data analysis operations efficiently.
📁 Project Structure
├── Weather Analysis.ipynb
├── Weather Data.csv
├── README.md
📄 Weather Analysis.ipynb

Contains all Python code, analysis, and outputs.

📄 Weather Data.csv

Dataset used for analysis.

📄 README.md

Project documentation and explanation.

**🎯 Conclusion**

This project demonstrates how Python and Pandas can be effectively used for real-world weather data analysis. Various data analysis techniques such as filtering, grouping, aggregation, statistical computation, and handling missing values were successfully implemented.

The project helps in understanding:

Exploratory Data Analysis (EDA)
Data cleaning techniques
Statistical operations in Pandas
Weather trend analysis

Overall, the project provides practical experience in data analysis using Pandas and builds a strong foundation for future data analytics and machine learning projects.
