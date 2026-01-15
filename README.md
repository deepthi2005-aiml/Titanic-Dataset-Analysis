# Titanic-Dataset-Analysis

## Overview
This project analyzes the Titanic dataset to explore factors that influenced passenger survival rates. The notebook includes comprehensive data cleaning, exploratory data analysis (EDA), and visualization to uncover patterns and insights from the historical Titanic passenger data.

## Dataset
The dataset used is `titanic.csv`, which contains information about Titanic passengers including demographics, ticket class, fare, and survival status.

## Project Structure

### 1. Data Import and Setup
- **Libraries Used**: 
  - Data handling: `numpy`, `pandas`
  - Visualization: `matplotlib.pyplot`, `seaborn`
- **Configuration**: Sets plot style to `whitegrid` for professional-looking visualizations

### 2. Initial Data Exploration
- Loads dataset and creates a working copy
- Examines dataset dimensions and structure
- Displays first 5 rows for initial inspection
- Provides dataset information including data types and missing values

### 3. Statistical Analysis
- **Numerical Features**: Descriptive statistics (count, mean, std, min, max, percentiles)
- **Categorical Features**: Count, unique values, top categories, and frequency

### 4. Data Cleaning and Preprocessing
- **Missing Value Analysis**:
  - Calculates percentage of missing values per column
  - Visualizes missing data using a heatmap
- **Feature Engineering**:
  - Extracts deck information from cabin data
  - Groups data by class and sex to calculate median age for imputation
  - Creates a function to impute missing age values based on passenger class and sex
- **Missing Value Treatment**:
  - Imputes missing age values using group medians
  - Fills missing embarkation values with the most common port ('S')
- **Verification**: Confirms cleaning effectiveness with post-cleaning heatmap

### 5. Exploratory Data Analysis and Visualization

#### Survival Analysis:
- **Overall Survival**: Countplot and survival rate calculation
- **Survival by Sex**: Countplot and survival rate by gender
- **Survival by Passenger Class**: Countplot and survival rate by class

#### Demographic Analysis:
- **Age Distribution**: Histograms and boxplots comparing survivors vs. non-survivors
- **Family Relationships**:
  - Creates `FamilySize` feature (siblings/spouses + parents/children + 1)
  - Creates `IsAlone` binary feature
  - Analyzes survival rates for alone vs. family passengers

#### Advanced Visualizations:
- Survival rate by passenger class and sex (point plot)
- Survival rate by passenger class and age (point plot)
- Survival rate by passenger class and fare (point plot)
- Survival rate by age and sex (point plot)
- Survival rate by fare and sex (point plot)

## Key Findings
1. **Overall Survival Rate**: Approximately 38% of passengers survived
2. **Gender Disparity**: Female passengers had significantly higher survival rates
3. **Class Impact**: Higher-class passengers had better survival chances
4. **Age Patterns**: Children had higher survival rates, particularly in lower classes
5. **Family Effect**: Passengers traveling alone had lower survival rates
6. **Fare Correlation**: Higher fares (typically associated with higher classes) correlated with better survival rates

## Technical Details
- **Environment**: Python 3 with Jupyter Notebook
- **Visualization Tools**: Seaborn for statistical graphics, Matplotlib for customization
- **Data Handling**: Pandas for data manipulation, NumPy for numerical operations
- **Missing Data Strategy**: Group-based imputation for age, mode imputation for categorical variables

## How to Use
1. Ensure you have the required libraries installed: `numpy`, `pandas`, `matplotlib`, `seaborn`
2. Place the `titanic.csv` file in the same directory as the notebook
3. Run the cells sequentially to reproduce the analysis
4. Modify visualization parameters or add new analyses as needed

## Dependencies
```
numpy
pandas
matplotlib
seaborn
```

## Notes
- The notebook demonstrates comprehensive EDA techniques suitable for binary classification problems
- Visualization choices are optimized for clarity and insight discovery
- Code includes both basic and advanced analysis methods
- All visualizations are properly labeled and titled for interpretability

This project serves as an excellent template for exploratory data analysis on classification datasets, showcasing best practices in data cleaning, visualization, and insight generation.
