# 🌾 Agriculture Crop Production Analysis

## 📌 Project Overview

Agriculture is one of the most important sectors of the economy. Crop production depends on many factors such as crop type, season, rainfall, temperature, soil, irrigation and farming methods.

This project focuses on analyzing an **Agriculture Crop Production dataset** using Python and Jupyter Notebook. The main purpose of this project is to understand the data, clean it, manipulate it and find useful information from it.

The dataset contains **1,555 rows and 25 columns**, which provides enough data to perform different types of analysis and visualization.

The complete project follows the process:

**Data → Data Cleaning → Data Manipulation → Data Analysis → Visualization → Findings → Conclusion**

---

# 🎯 Objectives

The main objectives of this project are:

* To understand the agriculture dataset.
* To inspect the rows and columns.
* To identify missing values.
* To identify duplicate records.
* To clean the dataset.
* To perform data manipulation using Pandas.
* To find the highest and lowest crop production.
* To compare different crops.
* To compare production between states.
* To analyze seasonal production.
* To analyze rainfall and temperature.
* To analyze revenue and profit.
* To create different charts.
* To find useful patterns and trends.
* To understand the factors affecting crop production.

---

# 🌱 Why I Chose This Dataset

I chose the Agriculture Crop Production dataset because agriculture is an important part of everyday life and the economy.

Crop production can be affected by different factors such as rainfall, temperature, soil type, irrigation and season. Therefore, I wanted to understand how these factors are related to agricultural production.

The dataset contains **1,555 records and 25 columns**, so it gives enough information for performing different types of data analysis.

By analyzing this dataset, I can find which crops have higher production, which states perform better, which crops generate more revenue and profit, and how production changes over time.

This dataset also helped me understand how Python can be used to solve a real-world data analysis problem.

---

# 📂 Dataset Information

| Property             | Details                     |
| -------------------- | --------------------------- |
| Dataset Name         | Agriculture Crop Production |
| Number of Rows       | 1,555                       |
| Number of Columns    | 25                          |
| File Format          | CSV                         |
| Programming Language | Python                      |
| Platform             | Jupyter Notebook            |
| Main Library         | Pandas                      |
| Numerical Library    | NumPy                       |
| Visualization        | Matplotlib                  |

---

# 🔎 Dataset Inspection

The first step is to understand the structure of the dataset.

```python
df.head()
```

```python
df.tail()
```

```python
df.shape
```

```python
df.columns
```

```python
df.info()
```

```python
df.describe()
```

These functions help to understand the size, columns, data types and basic statistics of the dataset.

---

# 🧹 Data Cleaning

Before analysis, the dataset is checked for common data problems.

The following steps are performed:

* Checking missing values
* Checking duplicate records
* Checking data types
* Checking incorrect values
* Removing duplicates if required
* Converting columns into correct data types
* Sorting the data
* Filtering unnecessary records

Example:

```python
df.isnull().sum()
```

```python
df.duplicated().sum()
```

```python
df.drop_duplicates()
```

---

# 📊 Data Manipulation

Pandas is used to manipulate the agriculture dataset.

Some operations performed are:

* Filtering
* Sorting
* Grouping
* Counting
* Finding totals
* Finding averages
* Finding maximum values
* Finding minimum values

Examples:

```python
df.sort_values("Production_Tonnes", ascending=False)
```

```python
df.groupby("Crop")["Production_Tonnes"].sum()
```

```python
df.groupby("State")["Production_Tonnes"].mean()
```

---

# ❓ Analysis Questions

The following questions are analyzed in this project:

1. What is the total crop production?
2. What is the average crop production?
3. Which crop has the highest production?
4. Which crop has the lowest production?
5. Which state has the highest production?
6. Which state has the lowest production?
7. Which season has the highest production?
8. How does production change over the years?
9. Which crop generates the highest revenue?
10. Which crop generates the highest profit?
11. Which state generates the highest revenue?
12. What is the average rainfall?
13. What is the average temperature?
14. Which soil type gives higher production?
15. Which irrigation type has higher production?
16. Which crops have higher yield?
17. How does rainfall affect production?
18. How does temperature affect production?
19. Which crops are more profitable?
20. How does production change according to season?

---

# 📈 Data Visualization

Matplotlib is used to visualize the agriculture data.

Different charts are created to understand the data easily.

## 📊 1. Bar Chart — Crop Production

Used to compare production between different crops.

```python
crop_production = df.groupby("Crop")["Production_Tonnes"].sum()

plt.figure(figsize=(10,5), facecolor="lightyellow")

plt.bar(crop_production.index,
        crop_production.values,
        color="green")

plt.title("Crop-wise Production")
plt.xlabel("Crop")
plt.ylabel("Production (Tonnes)")

plt.xticks(rotation=45)
plt.grid(axis="y", linestyle="--", alpha=0.5)

plt.tight_layout()
plt.show()
```

---

## 📈 2. Line Chart — Production Over Years

This chart shows how production changes over time.

```python
year_production = df.groupby("Year")["Production_Tonnes"].sum()

plt.figure(figsize=(10,5), facecolor="lightblue")

plt.plot(year_production.index,
         year_production.values,
         color="green",
         marker="o")

plt.title("Year-wise Crop Production")
plt.xlabel("Year")
plt.ylabel("Production (Tonnes)")

plt.grid(True, linestyle="--", alpha=0.5)

plt.show()
```

---

## 🥧 3. Pie Chart — Crop Distribution

```python
crop_count = df["Crop"].value_counts()

plt.figure(figsize=(7,7), facecolor="lavender")

plt.pie(crop_count.values,
        labels=crop_count.index,
        autopct="%1.1f%%",
        startangle=90)

plt.title("Crop Distribution")

plt.show()
```

---

## 📊 4. Histogram — Production Distribution

```python
plt.figure(figsize=(9,5), facecolor="honeydew")

plt.hist(df["Production_Tonnes"],
         bins=15,
         color="orange",
         edgecolor="black")

plt.title("Production Distribution")
plt.xlabel("Production (Tonnes)")
plt.ylabel("Frequency")

plt.show()
```

---

## 🔵 5. Scatter Plot — Rainfall vs Production

```python
plt.figure(figsize=(9,5), facecolor="lightcyan")

plt.scatter(df["Rainfall_mm"],
            df["Production_Tonnes"],
            color="blue",
            alpha=0.6)

plt.title("Rainfall vs Crop Production")
plt.xlabel("Rainfall (mm)")
plt.ylabel("Production (Tonnes)")

plt.grid(True, linestyle="--", alpha=0.5)

plt.show()
```

---

# 💡 Key Findings

The analysis helps to identify:

* The crops with the highest production.
* States with better crop production.
* The most productive seasons.
* Crops generating higher revenue.
* Crops generating higher profit.
* Changes in production over the years.
* The effect of rainfall on crop production.
* The effect of temperature on production.
* Differences between irrigation methods.
* Crops having higher yield.

The exact findings are obtained from the values and graphs generated in the Jupyter Notebook.

---

# 🧠 What I Learned

Through this project, I learned:

* How to work with CSV datasets.
* How to inspect a dataset.
* How to clean data.
* How to handle missing and duplicate values.
* How to filter data.
* How to sort data.
* How to use GroupBy.
* How to calculate totals and averages.
* How to find maximum and minimum values.
* How to create different graphs.
* How to interpret charts.
* How to write observations from data.

---

# 🛠️ Technologies Used

### Python

Used as the main programming language.

### Pandas

Used for data cleaning, manipulation and analysis.

### NumPy

Used for numerical operations.

### Matplotlib

Used for creating visualizations.

### Jupyter Notebook

Used for performing and documenting the complete analysis.

---

# 📁 Project Structure

```text
Agriculture-Crop-Production-Analysis/
│
├── Agriculture_Crop_Production.csv
├── Agriculture_Analysis.ipynb
└── README.md
```

---

# 🔄 Data Analysis Workflow

```text
Dataset
   ↓
Load Dataset
   ↓
Inspect Data
   ↓
Clean Data
   ↓
Manipulate Data
   ↓
Perform Analysis
   ↓
Create Visualizations
   ↓
Findings
   ↓
Conclusion
```

---

# 🏁 Conclusion

The Agriculture Crop Production Analysis project helped me understand how data analytics can be applied to agriculture.

By using Python, Pandas, NumPy and Matplotlib, I was able to clean the dataset, manipulate the data, perform different calculations and create visualizations.

The analysis provides useful information about crop production, states, seasons, rainfall, temperature, revenue and profit.

Overall, this project gave me practical experience in working with a real-world dataset and helped me understand the complete process of data analysis.

The project uses data cleaning, manipulation, exploratory data analysis, and visualization to understand crop production patterns. 

The analysis helps identify differences between crops and regions and provides useful information about agricultural production trends.

This project also demonstrates the practical use of Python libraries such as Pandas, NumPy, and Matplotlib for analyzing real-world datasets.

---

# 👨‍💻 Author

**Abhay Kakade**

Aspiring Data Analyst | Python | Pandas | NumPy | Matplotlib

This project demonstrates practical skills in Python-based data analysis and visualization.

# 🏁 Project Status
Completed ✅

Project Type: Data Analysis

Environment: Jupyter Notebook

# ⭐ If You Find This Project Interesting
Feel free to explore the notebook, datasets and visualizations.

⭐ Star the repository if you find it useful.
