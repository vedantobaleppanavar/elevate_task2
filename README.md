# Titanic Dataset - Data Cleaning and Exploratory Data Analysis (EDA)

## Overview

This project demonstrates the steps involved in **Data Cleaning**, **Preprocessing**, and **Exploratory Data Analysis (EDA)** using the Titanic dataset. The goal is to prepare the dataset for machine learning by handling missing values, encoding categorical variables, scaling numerical features, and visualizing insights.

## Objectives

1. **Task 1: Data Cleaning & Preprocessing**

   - Handle missing values in the dataset.
   - Encode categorical variables into numerical formats.
   - Normalize or standardize numerical features.
   - Visualize and remove outliers for cleaner data.
   - Save the cleaned dataset for further analysis.

2. **Task 2: Exploratory Data Analysis (EDA)**
   - Generate summary statistics of the dataset.
   - Use visualizations to understand data distributions and relationships.
   - Identify patterns, trends, and anomalies in the data.
   - Make feature-level inferences to guide further modeling.

---

## Dataset

The Titanic dataset contains information about passengers on the RMS Titanic, including their survival status, age, ticket class, and more. It is a widely used dataset for introductory machine learning and data analysis tasks.

### Dataset Features

- **PassengerId**: Unique identifier for each passenger.
- **Survived**: Survival status (0 = No, 1 = Yes).
- **Pclass**: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd).
- **Name**: Passenger's name.
- **Sex**: Passenger's gender.
- **Age**: Passenger's age.
- **SibSp**: Number of siblings/spouses aboard.
- **Parch**: Number of parents/children aboard.
- **Ticket**: Ticket number.
- **Fare**: Passenger fare.
- **Cabin**: Cabin number.
- **Embarked**: Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).

---

## Project Workflow

### Task 1: Data Cleaning & Preprocessing

1. **Handle Missing Values**

   - Fill missing values in `Age` with the median.
   - Fill missing values in `Embarked` with the mode.
   - Drop the `Cabin` column due to excessive missing values.

2. **Encode Categorical Variables**

   - Convert `Sex` and `Embarked` into numerical format using one-hot encoding.

3. **Scale Numerical Features**

   - Standardize `Age` and `Fare` using `StandardScaler`.

4. **Outlier Detection & Removal**

   - Visualize outliers using boxplots.
   - Remove outliers in `Fare` using the Interquartile Range (IQR) method.

5. **Save the Cleaned Dataset**
   - Save the cleaned dataset as `titanic_data.csv`.

### Task 2: Exploratory Data Analysis (EDA)

1. **Summary Statistics**

   - Generate descriptive statistics for numerical and categorical features.

2. **Visualizations**

   - Create histograms and boxplots for numeric features (`Age`, `Fare`).
   - Use pairplots to explore relationships between features.
   - Visualize the correlation matrix with a heatmap.

3. **Patterns and Trends**
   - Analyze survival rates by gender and passenger class.
   - Explore the relationship between `Fare`, `Pclass`, and `Survived`.

---

## Tools and Libraries

- **Python**: Programming language used for data analysis.
- **Pandas**: Data manipulation and analysis.
- **NumPy**: Numerical computing.
- **Matplotlib**: Data visualization.
- **Seaborn**: Statistical data visualization.
- **Plotly**: Interactive visualizations.
- **scikit-learn**: Data preprocessing (e.g., standardization).

---

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/vedantobaleppanavar/elevate_task1.git
   cd elevate_task1
   ```

2. Install required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Run the scripts:

   - **Data Cleaning**: `titanic_data_cleaning.py`
   - **EDA**: `titanic_eda.py`

4. (Optional) Open the Jupyter Notebook version for an interactive walkthrough.

---

## Key Insights

### From Data Cleaning:

- Missing values in `Age` and `Embarked` were successfully handled.
- Outliers in `Fare` were removed using the IQR method.
- The dataset was standardized, making it ready for machine learning.

### From EDA:

- **Gender**: Women had a significantly higher survival rate than men.
- **Class**: Passengers in first class had a much higher survival rate than those in lower classes.
- **Fare**: Higher ticket fares were correlated with better survival chances.

---

## Future Work

- Build machine learning models (e.g., Logistic Regression, Random Forest) to predict survival.
- Engineer new features such as `FamilySize` (combining `SibSp` and `Parch`) for better predictions.
- Tune models for better performance and evaluate using cross-validation.

---

## Folder Structure

```plaintext
elevate_task1/
├── titanic_data_cleaning.py   # Script for data cleaning and preprocessing
├── titanic_eda.py             # Script for exploratory data analysis
├── titanic_data.csv           # Cleaned dataset
└── README.md                  # Project documentation
```

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
