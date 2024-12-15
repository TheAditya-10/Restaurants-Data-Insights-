# Restaurant Rating Prediction and Analysis

## Project Overview

This project aims to predict restaurant ratings and comprehensively analyze a restaurant dataset. 

**Key Objectives:**

1. **Data Cleaning and Preprocessing:** Handle missing values, perform type conversions, and encode categorical features (ordinal, one-hot, multi-label).
2. **Class Imbalance:** Address class imbalance in the 'Aggregate rating' using SMOTENC.
3. **Data Exploration and Visualization:** Analyze numerical and categorical features, including distributions, correlations, top cuisines, and restaurant counts by city and country.
4. **Geospatial Analysis:** Visualize restaurant locations on a map using latitude and longitude.
5. **Table Booking and Online Delivery Analysis:** Explore the impact of table booking and online delivery on ratings.
6. **Price Range Analysis:** Investigate the relationship between price range and ratings.
7. **Feature Engineering:** Create new features (Restaurant Name Length, Address Length) for potential model improvement.
8. **Predictive Modeling:** Build and evaluate models (Linear Regression, Decision Tree, Random Forest) to predict ratings.
9. **Customer Preference Analysis:** Identify popular cuisines, highly-rated cuisines, and customer preferences based on votes and ratings.

**Tools and Technologies:**

- Python
- Pandas
- Scikit-learn
- Matplotlib
- Seaborn
- Folium
- Imbalanced-learn

## Code Explanation

### **Level 1: Data Preparation and Exploration**

- **Dataset Loading and Exploring:** Loads the dataset, displays initial rows, and checks data types.
- **Type Conversion:** Converts categorical columns to numerical representations using ordinal encoding, one-hot encoding, and multi-label encoding.
- **Missing Value Handling:** Identifies and handles missing values, primarily by dropping rows.
- **Class Imbalance:** Addresses class imbalance in the target variable using SMOTENC to oversample minority classes.
- **Data Description:** Provides descriptive statistics for numerical features and creates visualizations (histograms, box plots).
- **Categorical Value Analysis:** Analyzes top cuisines and cities with the highest restaurant count using visualizations.
- **Geospatial Analysis:** Creates an interactive map to visualize restaurant locations using Folium.

### **Level 2: Feature Analysis and Engineering**

- **Table Booking and Online Delivery:** Explores the relationship between table booking, online delivery, and ratings.
- **Price Range Analysis:** Analyzes the distribution of price ranges and their impact on ratings.
- **Feature Engineering:** Creates new features, such as restaurant name length and address length, to potentially improve model performance.

### **Level 3: Predictive Modeling and Customer Preference Analysis**

- **Predictive Modeling:** Builds and evaluates predictive models (Linear Regression, Decision Tree, Random Forest) using selected features.
- **Customer Preference Analysis:** Identifies popular cuisines, highly-rated cuisines, and customer preferences based on votes and average ratings.

## Dataset

The project uses a restaurant dataset containing information about various restaurants, including location, cuisine, price range, ratings, and more.

## Results

- The project provides insights into restaurant ratings, popular cuisines, customer preferences, and pricing trends.
- Predictive models are developed to estimate restaurant ratings with reasonable accuracy.
- The analysis helps understand factors influencing restaurant ratings and customer choices.

## Internship with Conifyz Technologies

This project was undertaken during an internship with Conifyz Technologies, providing valuable experience in data science and machine learning techniques applied to real-world data.
