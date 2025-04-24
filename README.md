
# Titanic Dataset - Data Cleaning & Preprocessing

This project demonstrates the process of cleaning and preprocessing the Titanic dataset to prepare it for machine learning models. The dataset is preprocessed by handling missing values, encoding categorical features, scaling numerical features, removing outliers, and saving the cleaned data for further analysis or modeling.

## Task Overview

The Titanic dataset contains information about the passengers on the Titanic, such as their age, class, survival status, and other features. This project focuses on preparing the dataset for machine learning tasks by addressing common data cleaning issues like missing values, feature scaling, and encoding categorical variables.

## Dataset

The dataset is loaded from a public URL:
[Dataset URL](https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv)

### Columns in the Dataset:

- **PassengerId**: Unique ID for each passenger.
- **Survived**: Indicates whether the passenger survived (1) or not (0).
- **Pclass**: The passenger's class (1st, 2nd, 3rd).
- **Name**: Passenger's name.
- **Sex**: Passenger's gender.
- **Age**: Passenger's age.
- **SibSp**: Number of siblings/spouses aboard.
- **Parch**: Number of parents/children aboard.
- **Ticket**: Ticket number.
- **Fare**: The amount of money the passenger paid for the ticket.
- **Cabin**: The cabin where the passenger stayed.
- **Embarked**: The port where the passenger boarded (C = Cherbourg; Q = Queenstown; S = Southampton).

## Steps Involved

### 1. **Loading the Dataset**

The Titanic dataset is loaded from a publicly available CSV file into a Pandas DataFrame.

### 2. **Exploring the Data**

Initial exploration involves checking the basic structure of the dataset:

- Overview of data types and non-null counts.
- Descriptive statistics.
- Identifying missing values.

### 3. **Handling Missing Values**

- **Age**: Missing values are filled with the median of the `Age` column.
- **Fare**: Missing values are filled with the median of the `Fare` column.
- **Embarked**: Missing values are filled with the mode (most frequent value) of the `Embarked` column.
- **Cabin**: The `Cabin` column is dropped due to a high percentage of missing values.

### 4. **Encoding Categorical Variables**

- **Sex**: The `Sex` column is mapped to binary values (0 for male, 1 for female).
- **Embarked**: The `Embarked` column is one-hot encoded into two separate columns: `Embarked_Q` and `Embarked_S`.

### 5. **Feature Scaling**

- **Age** and **Fare** columns are scaled using `StandardScaler` to standardize the numerical features, ensuring they are on the same scale.

### 6. **Outlier Detection and Removal**

Outliers in the `Age` and `Fare` columns are identified using the Interquartile Range (IQR) method and removed from the dataset to prevent them from skewing the model.

### 7. **Saving the Cleaned Dataset**

After all preprocessing steps, the cleaned dataset is saved as `cleaned_titanic.csv` for use in further machine learning analysis or modeling.

## Technologies Used

- **Python**: Programming language used for data manipulation and preprocessing.
- **Pandas**: Data manipulation and analysis library.
- **NumPy**: Numerical computing library.
- **Matplotlib** and **Seaborn**: Visualization libraries for plotting data.
- **Scikit-learn**: Library used for feature scaling.

