# 🦠 COVID-19 Data Analysis with Python

## 📋 Overview

This project analyzes COVID-19 pandemic data using Python and Pandas. It's a practical data analysis exercise that demonstrates how to work with real-world health data to extract meaningful insights about the spread and impact of COVID-19 across different regions.

**Data Period**: Records as of 29-April-2020

## 📊 Dataset

The dataset is sourced from **Kaggle** and contains COVID-19 statistics including:

| Column | Description |
|--------|-------------|
| Region | Country/Region name |
| Confirmed | Number of confirmed COVID-19 cases |
| Deaths | Number of deaths |
| Recovered | Number of recovered cases |

> **Note**: This is a small dataset for learning purposes. The full dataset contains approximately 19,000 rows.

## 🔧 Technologies Used

- **Python 3.x**
- **Pandas** - Data manipulation and analysis
- **Seaborn** - Statistical data visualization
- **Matplotlib** - Plotting library

## 📈 Analysis Questions Covered

| # | Question |
|---|----------|
| 1 | Show the number of Confirmed, Deaths and Recovered cases in each Region |
| 2 | Remove all records where Confirmed Cases is less than 10 |
| 3 | In which Region were maximum Confirmed cases recorded? |
| 4 | In which Region were minimum Deaths cases recorded? |
| 5 | How many Confirmed, Deaths & Recovered cases were reported from India till 29 April 2020? |
| 6-A | Sort data by Confirmed cases in ascending order |
| 6-B | Sort data by Recovered cases in descending order |

## 🚀 Getting Started

### Prerequisites

```bash
pip install pandas seaborn matplotlib
```

### Running the Analysis

1. Download the dataset from Kaggle
2. Update the file path in the notebook:
   ```python
   data = pd.read_csv("path/to/Covid_19_data.csv")
   ```
3. Run the Jupyter Notebook cells sequentially

## 📁 Project Structure

```
├── Covid19 (1).ipynb          # Main analysis notebook
├── Data/
│   └── Covid_19_data.csv      # COVID-19 dataset
└── README.md                  # This file
```

## 🔍 Data Preprocessing Steps

### 1. Checking Missing Values
```python
data.count()           # Count non-null values
data.isnull().sum()    # Count null values per column
```

### 2. Visualizing Missing Data
```python
sns.heatmap(data.isnull())
plt.show()
```

### 3. Filtering Data
```python
# Remove records where Confirmed cases < 10
data = data[~(data.Confirmed < 10)]
```

## 📊 Key Operations Demonstrated

| Operation | Code Example |
|-----------|--------------|
| Group by Region | `data.groupby('Region')['Confirmed', 'Recovered'].sum()` |
| Sort Values | `data.sort_values(by=['Confirmed'], ascending=False)` |
| Filter by Country | `data[data.Region == 'India']` |
| Aggregate Functions | `data.groupby('Region').Confirmed.sum()` |

## 💡 Key Insights

- Identify regions with highest and lowest COVID-19 impact
- Compare confirmed cases vs recovery rates across countries
- Understand the data distribution using visualizations
- Learn data filtering and cleaning techniques

## 🎯 Learning Objectives

After completing this analysis, you will be able to:

- ✅ Load and explore CSV data using Pandas
- ✅ Handle missing values in datasets
- ✅ Use groupby operations for aggregation
- ✅ Sort and filter DataFrames
- ✅ Create heatmaps using Seaborn
- ✅ Extract country-specific insights

## 📚 Useful Pandas Methods

```python
df.count()                    # Count non-null values
df.isnull().sum()             # Count null values
df.groupby('col').sum()       # Group and aggregate
df.sort_values(by='col')      # Sort DataFrame
df[df.col == 'value']         # Filter rows
df[~(df.col < value)]         # Remove rows by condition
```

## 👤 Author

**Mohan Birajdar**

## 📄 License

This project is for educational purposes.

---

⭐ Part of Big Data Analysis learning series
