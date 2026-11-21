# OTT Viewer Engagement Analysis

## 1. Project Overview

The **OTT Viewer Engagement Analysis** project focuses on analyzing viewer behaviour and engagement patterns on an Over-The-Top (OTT) streaming platform.

The project uses Python and data analysis libraries to clean, process, explore, and visualize viewer data. It examines how factors such as subscription plans, device types, content genres, age, weekly watch hours, and titles watched relate to viewer engagement.

The main objective is to understand viewer engagement patterns and identify the factors that may influence the overall `Engagement_Score`.

---

## 2. Project Objectives

The major objectives of this project are:

- To load and understand the OTT viewer dataset.
- To clean the dataset by handling missing values, duplicate records, and invalid data.
- To perform Exploratory Data Analysis (EDA).
- To analyze the distribution of `Engagement_Score`.
- To study the relationship between weekly watch hours, titles watched, and engagement score.
- To examine the influence of age and average session duration on engagement.
- To compare engagement across subscription plans, device types, cities, and content genres.
- To create meaningful visualizations for presenting analytical findings.
- To generate a cleaned dataset for further analysis.

---

## 3. Project Structure

The following is the folder structure of the project, based on the VS Code Explorer:

```text
HCL Project/
│
├── data/
│   │
│   ├── processed/
│   │   └── ott_data_clean.csv
│   │
│   └── raw/
│       └── ott_data.csv
│
├── Images/
│   ├── 01_overall_satisfaction.png
│   ├── 02_balance_transactions.png
│   ├── 03_correlation.png
│   └── 04_group_comparison.png
│
├── notebooks/
│   └── draft 1.ipynb
│
├── script/
│   ├── presentation.pptx
│   └── srs document
│
├── README.md
│
└── requirement.txt
```

### Folder and File Description

| Folder/File | Description |
|---|---|
| `data/` | Contains the project datasets. |
| `data/raw/` | Stores the original, unprocessed OTT dataset. |
| `data/processed/` | Stores the cleaned and processed dataset. |
| `Images/` | Contains the graphs and visualizations generated during EDA. |
| `notebooks/` | Contains the Jupyter Notebook used for data cleaning, analysis, and visualization. |
| `script/` | Contains project documentation and presentation files. |
| `presentation.pptx` | Project presentation containing important findings. |
| `srs document` | Software Requirements Specification document. |
| `README.md` | Provides an overview and instructions for the project. |
| `requirement.txt` | Contains the Python libraries required to run the project. |

---

## 4. Dataset Description

The project uses an OTT Viewer Engagement dataset containing information about viewers, their subscriptions, viewing habits, and engagement scores.

### Dataset Attributes

| Column Name | Description |
|---|---|
| `Viewer_ID` | Unique identification number of each viewer. |
| `Subscription_Plan` | Subscription plan selected by the viewer. |
| `Device_Type` | Device used to access the OTT platform. |
| `City` | City associated with the viewer. |
| `Content_Genre` | Genre of content watched by the viewer. |
| `Age` | Age of the viewer. |
| `Weekly_Watch_Hours` | Total hours spent watching content per week. |
| `Titles_Watched` | Number of titles watched by the viewer. |
| `Avg_Session_Minutes` | Average duration of a viewing session in minutes. |
| `Last_Active_Date` | Date when the viewer was last active. |
| `Engagement_Score` | Numerical score representing viewer engagement. |

---

## 5. Technologies and Libraries Used

The following technologies and Python libraries are used:

- **Python:** Main programming language.
- **Pandas:** Data loading, cleaning, manipulation, and analysis.
- **NumPy:** Numerical calculations and data processing.
- **Matplotlib:** Data visualization.
- **Seaborn:** Statistical graphs and visualizations.
- **Jupyter Notebook:** Interactive environment for executing Python code.
- **Visual Studio Code:** Development environment for managing the project.

---

## 6. Data Cleaning and Preprocessing

Data cleaning is performed to improve the quality and reliability of the dataset.

The following operations are included:

1. Loading the original CSV dataset.
2. Checking the dataset structure and data types.
3. Removing duplicate records.
4. Converting numerical columns into appropriate numeric data types.
5. Handling missing values.
6. Identifying and handling invalid age values.
7. Converting date columns into datetime format.
8. Standardizing categorical values.
9. Creating additional analytical columns.
10. Saving the cleaned dataset in the processed folder.

### Feature Engineering

Three additional columns are created:

**1. Engagement Category**

The `Engagement_Score` is divided into three categories:

- Low: 0–40
- Medium: Above 40–70
- High: Above 70–100

**2. Age Group**

Viewers are grouped into age categories to make age-based comparisons easier.

**3. Watch Hours Per Title**

This feature represents the average weekly watch hours per title watched.

Formula:

`Watch_Hours_Per_Title = Weekly_Watch_Hours / Titles_Watched`

---

## 7. Exploratory Data Analysis (EDA)

Exploratory Data Analysis is performed to understand the dataset and discover patterns, relationships, and trends.

The following analyses are included:

### 7.1 Overall Engagement Score Analysis

- Calculate mean, median, minimum, and maximum engagement scores.
- Examine the spread and distribution of engagement scores.
- Identify extreme values.
- Analyze the number of viewers in each engagement category.

### 7.2 Viewing Behaviour Analysis

Analyze the relationship between:

- Weekly watch hours and engagement score.
- Number of titles watched and engagement score.
- Age and engagement score.
- Average session minutes and engagement score.

### 7.3 Correlation Analysis

A correlation heatmap is used to understand relationships between numerical variables.

It helps identify which numerical features have stronger positive or negative associations with engagement.

### 7.4 Group-Wise Engagement Analysis

Compare average engagement scores across:

- Subscription plans.
- Device types.
- Cities.
- Content genres.

---

## 8. Data Visualizations

The project includes four main visualization files.

| Image File | Visualization | Purpose |
|---|---|---|
| `01_overall_satisfaction.png` | Engagement Score Distribution | Shows the distribution of engagement scores and engagement categories. |
| `02_balance_transactions.png` | Viewing Behaviour Analysis | Shows the relationship between weekly watch hours, titles watched, and engagement score. |
| `03_correlation.png` | Correlation Heatmap | Displays correlations between numerical variables. |
| `04_group_comparison.png` | Group Comparison | Compares average engagement scores across subscription plans, devices, cities, and genres. |

All visualization images are stored in the `Images/` folder.

---

## 9. Project Workflow

The project follows this general workflow:

```text
        Raw OTT Dataset
               |
               v
       Data Loading
               |
               v
     Data Understanding
               |
               v
       Data Cleaning
               |
               v
    Data Preprocessing
               |
               v
      Feature Engineering
               |
               v
 Exploratory Data Analysis
               |
               v
    Data Visualization
               |
               v
     Findings & Insights
               |
               v
       Final Presentation
```

---

## 10. How to Run the Project

Follow these steps to run the project on your local system.

### Step 1: Clone or Download the Project

Download the project folder and open it in Visual Studio Code.

### Step 2: Install Python

Make sure Python is installed on your system.

### Step 3: Open the Project Folder

Open the `HCL Project` folder in VS Code.

### Step 4: Install Required Libraries

Open the VS Code terminal and run:

```bash
pip install -r requirement.txt
```

### Step 5: Open the Jupyter Notebook

Open the following file:

```text
notebooks/draft 1.ipynb
```

### Step 6: Select the Python Kernel

Select an available Python environment in VS Code.

### Step 7: Execute the Notebook

Run the notebook cells sequentially, starting from dataset loading and continuing through data cleaning, analysis, and visualization.

---

## 11. Expected Outcomes

After completing the project, the analysis is expected to provide:

- An understanding of the overall viewer engagement distribution.
- Insights into viewer watching behaviour.
- An understanding of relationships between numerical variables.
- Comparisons of engagement across different subscription plans and devices.
- Insights into engagement patterns across cities and content genres.
- A cleaned dataset suitable for further analysis.
- Visualizations and findings that can be included in the final presentation.

The actual conclusions should be based on the results generated from the dataset.

---

## 12. Conclusion

The OTT Viewer Engagement Analysis project demonstrates how Python-based data analysis can be used to understand viewer behaviour on a streaming platform.

By performing data cleaning, preprocessing, feature engineering, exploratory data analysis, and visualization, the project provides a structured approach to studying viewer engagement.

The analysis helps identify patterns and relationships among different viewer characteristics and watching behaviours. These insights can support a better understanding of audience engagement and help inform data-driven decisions for OTT platforms.

---

## 13. Author

**Project:** OTT Viewer Engagement Analysis  
**Organization/Project Context:** HCL Project  
**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Jupyter Notebook, VS Code

---

*This README provides the documentation and usage guide for the OTT Viewer Engagement Analysis project.*