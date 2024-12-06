# Cognifyz-Internship-Project
Data analysis of Restaurants all over the world.
**Level 1: Data Preparation and Exploration**

1. **Dataset Loading and Exploring:**
   - **`pd.read_csv('/content/dataset.csv')`:** This line uses the pandas library (`pd`) to read the dataset from the specified CSV file path into a pandas DataFrame (`df`). DataFrames are a convenient way to store and manipulate tabular data in Python.
   - **`df.head(20)`:** This displays the first 20 rows of the DataFrame. It's a quick way to get a visual overview of the data's structure, column names, and some sample values.
   - **`df.shape`:** This attribute returns a tuple containing the number of rows and columns in the DataFrame. It's useful for understanding the size of the dataset.

2. **Type Conversion - I:**
   - **`df.dtypes`:** This attribute shows the data type of each column in the DataFrame. Data types are important for ensuring that data is interpreted correctly and that appropriate operations can be performed on it.
   - **Ordinal Encoding (`OrdinalEncoder`)**
      - **Why used?** Ordinal encoding is used for features that have a natural order or ranking among their categories. In this case, features like "Has Table booking" are binary (Yes/No) and have an implied order (Yes is often considered "better" than No). 
      - **How it works:** Ordinal encoding assigns a numerical value to each category based on its order. For example, "No" might be encoded as 0 and "Yes" as 1. This preserves the ordinal relationship between the categories.
   - **One-Hot Encoding (`OneHotEncoder`)**
      - **Why used?** One-hot encoding is used for categorical features where the categories have no inherent order or ranking. Examples in this dataset are "Rating color" and "Currency." Using numerical values directly for these features could mislead machine learning models into assuming an ordinal relationship when there isn't one.
      - **How it works:** One-hot encoding creates a new binary column for each category. If a data point belongs to a particular category, the corresponding column is set to 1; otherwise, it's set to 0. This creates a sparse representation of the categorical data.
   - **Multi-label Encoding (`MultiLabelBinarizer`)**
      - **Why used?** The 'Cuisines' column has multiple cuisines separated by commas. This is a multi-label feature because a single restaurant can have multiple cuisines.
      - **How it works:** Multi-label encoding transforms the list of cuisines into a set of binary features. Each cuisine gets its own binary column, and if a restaurant offers that cuisine, the corresponding column is set to 1.

3. **Handling Missing Values:**
   - **`df.isnull().sum()`:** This calculates the number of missing values (NaN) in each column. It's essential to identify and handle missing data, as it can affect the performance of machine learning models.
   - **`df.dropna()`:**  In this case, rows with missing values in the 'Cuisines' column are dropped. This is a straightforward approach to handle missing data, but other methods like imputation (filling in missing values) could be considered depending on the nature of the missing data.

4. **Class Imbalance:**
   - **`df['Aggregate rating'].value_counts()`:** This calculates the frequency of each unique value in the 'Aggregate rating' column. It helps to understand the distribution of the target variable, especially if there's class imbalance (one class having significantly more instances than others).
   - **SMOTENC:** 
      - **Why used?** Class imbalance can lead to biased models that perform poorly on minority classes. SMOTENC is a technique to address this by oversampling the minority classes.
      - **How it works:** SMOTENC creates synthetic samples for the minority classes based on the existing data points. It's designed to handle both categorical and numerical features. It works by finding the k-nearest neighbors of minority class instances and creating new instances along the lines connecting them.
      - **Why not other methods?** Other methods like Random Oversampling or SMOTE might not be as effective with mixed data types. SMOTENC is designed to handle both numerical and categorical data, making it suitable for this dataset.

5. **Describing Data:**
   - **`df.describe()`:** This provides summary statistics (mean, standard deviation, min, max
