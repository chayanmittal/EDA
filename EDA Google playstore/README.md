# Overview
This project involves performing **Exploratory Data Analysis (EDA)** and **Feature Engineering** on a dataset related to the Google Play Store. With over 2.56 million apps available in the Google Play Store, this analysis aims to explore various aspects of these apps, such as the most popular categories, the apps with the largest number of installs, and other key features. By performing data cleaning and feature engineering, we can gain meaningful insights about the apps and understand trends within the data.

🔍 Python code? Check them out here: [EDA Google Playstore](/EDA%20Google%20playstore/EDA%20&%20FE%20GooglePlaystore.ipynb)

## Problem Statement
With millions of apps available, the objective of this project is to:

1. Find the Most Popular Category.
2. Identify the App with the largest number of installs.
3. Determine the App with the largest size.
4. Explore relationships and trends within the dataset using various features such as ratings, installs, price, and category.

## Dataset Description
The dataset consists of 20 columns and 10,841 rows containing information about various apps on the Google Play Store. These columns include features such as:

- **App:** Name of the application.
- **Category:** Category of the app.
- **Rating:** User rating for the app.
- **Reviews:** Number of reviews.
- **Size:** Size of the app.
- **Installs:** Number of installs.
- **Type:** Paid or Free app.
- **Price:** Price of the app (if paid).
- **Content Rating:** Audience type (e.g., "Everyone", "Teen").
- **Last Updated:** Date of last update.

## Steps and Workflow
1. **Data Collection**
    - The dataset is collected from a CSV file named Google_playstore_data.csv.
    - Data columns are initially explored to understand the structure and data types.
2. **Data Cleaning**
    - Handle missing values and remove rows with inconsistent or missing data.
    - Convert columns like Reviews, Installs, and Price to the correct data types.
    - Handle issues such as Size values that contain non-numeric characters like "k" (thousands) or "M" (millions).
    - Drop duplicates to ensure data quality.
3. **Feature Engineering**
    - Create new features for easier analysis such as:
        - Convert Size into a numerical format (handling k and M units).
        - Extract new time-related features from Last Updated (day, month, year).
    - Clean up Price and Installs columns by removing symbols (+, ,, $).
4. **Exploratory Data Analysis (EDA)**
    - Perform univariate analysis on numerical and categorical columns to identify trends.
    - Visualize the distribution of features such as ratings, size, installations, and price.
    - Examine the most popular app categories, top 10 categories, and the relationship between categories and number of installs.
    - Explore the distribution of 5-star rated apps.

![KDE plot](/EDA%20Google%20playstore/insights/kde%20plot%20for%20numerical%20feature.png)
*KDE plot for numerical feature*

5. **Key Insights**
    - The most popular app categories are Family, Games, and Tools.
    - Subway Surfers is the most installed game, with over 35 billion installs in the Google Play Store.
    - Instagram is the most installed social app.
    - Google Drive leads as the most popular productivity app.
    - 271 apps on the Play Store have received a perfect 5-star rating.

![Most popular categories in playstore](/EDA%20Google%20playstore/insights/Most%20Popular%20Categories%20in%20Play%20Store.png)
*Bar graph visualizing the most popular categories in play store*

![5 most installed apps in each popular category](/EDA%20Google%20playstore/insights/5%20most%20installed%20Apps%20in%20Each%20popular%20Categories.png)
*Bar graph visualizing the 5 most installed apps in each popular category*



## Requirements
To run the project and analysis, you need the following libraries installed:
- pandas: For data manipulation and analysis.
- numpy: For numerical operations.
- matplotlib: For data visualization.
- seaborn: For enhanced visualizations.
- warnings: To suppress unnecessary warnings.
- datetime: For working with date and time.

You can install the necessary libraries using the following pip commands:

```python
pip install pandas numpy matplotlib seaborn
```
## Installation and Usage
1. Download the Google_playstore_data.csv dataset and place it in the same directory as the project script.
2. Run the Python script that contains the EDA and feature engineering steps.
3. The script will process the data, clean it, and generate visualizations to uncover key insights about the Google Play Store data.
```python

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
warnings.filterwarnings("ignore")

%matplotlib inline

df = pd.read_csv('Google_playstore_data.csv')
```
## File Outputs
- google_cleaned.csv: The cleaned dataset after handling missing values, duplicates, and type conversions.
- **Visualizations:** Various charts and graphs that explore data distribution and insights into app categories, number of installs, ratings, and more.

## Data Insights & Observations
1. **App Categories:** The top 3 categories with the most apps are Family, Games, and Tools. Conversely, categories such as Beauty, Comics, and Weather have the least number of apps.

2. **Top Installed Apps:** The Games category has the most number of installs, with Subway Surfers leading among the most installed apps.

3. **5-Star Apps:** There are 271 apps with a perfect 5-star rating. The highest-rated app is CT Brain Interpretation from the Family category.

4. **Category Popularity:** Game is the most popular category in terms of total installations (measured in billions).


## Acknowledgments
- The dataset was collected from the Google Play Store.
- Thanks to the contributors of the various Python libraries used in this project.