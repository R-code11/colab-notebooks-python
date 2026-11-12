# Session 6: Exploratory Data Analysis — Detailed

**Quant Society Club**  
Azim Premji University, Bhopal

---

## Overview

In Session 5 we loaded our first real dataset and took a quick first look. In this session we go **much deeper**. This is the complete **EDA (Exploratory Data Analysis)** workshop — the core skill of every data analyst.

We move from *"what is this dataset"* to *"what story does the data tell"*. By the end, you'll have a **reusable EDA workflow** that you can apply to any dataset in your academic courses, research projects, or future jobs.

This session is designed to be a **2-hour hands-on workshop**. Bring your laptop with Google Colab open.

---

## Learning Objectives

Upon completion of this session, participants should be able to:

- Recognise the four types of variables: **categorical (nominal, ordinal), continuous (discrete, identifier)**
- Understand why `year` is numeric but best treated as categorical
- Compute the **right summary statistics** for each type of variable
- Calculate mean, median, mode, standard deviation, variance, IQR, coefficient of variation, percentiles, skewness, and kurtosis
- Detect and handle **missing values**, **duplicates**, and **placeholder values**
- Find **outliers** using the IQR rule and check for impossible values
- Visualise **univariate distributions** — histograms, KDE, box plots, count plots, pie charts
- Explore **bivariate relationships** — scatter plots, correlation matrices, groupby, pivot tables, crosstabs, chi-square tests
- Explore **multivariate patterns** using hue plots, pairplots, and binning (`pd.cut`, `pd.qcut`)
- Write a **reusable `quick_eda()` function** to summarise any dataset in one line

---

## Session Outline (2-Hour Structure)

### Part 1 — Setup & Recap (10 min)
- Session 5 recap
- Mount Drive, load `academic_data.csv`
- Import libraries

### Part 2 — Data Quality (15 min)
- Missing values — count, percentage, decision
- Duplicate rows
- Placeholder values (e.g. `-` in `complaint_type`)
- Creating `df_clean` (a safe copy)
- **Important:** `ai_tool`'s 7 missing values filled with `"No Tool"` **only in `df_clean`** — original `df` unchanged. We also check whether those 7 students really used less AI.

### Part 3 — Categorical vs Continuous (15 min)
- Nominal, ordinal, discrete, identifier — the 4 types
- Why `year` (1, 2, 3, 4) is numeric but effectively **categorical**
- Automatic detection using `select_dtypes`

### Part 4 — Continuous Summary (20 min)
- mean, median, mode, std, variance
- IQR, CV (coefficient of variation)
- Percentiles (25th, 50th, 75th, 90th)
- Skewness, kurtosis
- Building a reusable summary function

### Part 5 — Categorical Summary (15 min)
- Frequency table
- Percentage and cumulative percentage
- Mode
- Looping through all categorical columns

### Part 6 — Univariate Plots (15 min)
- Histogram + KDE
- Box plot
- Count plot
- Pie chart

### Part 7 — Outliers (10 min)
- IQR rule
- Impossible values (negative study hours, marks > 100, etc.)

### Part 8 — Bivariate Analysis (20 min)
- Scatter plot + trend line
- Correlation matrix + heatmap
- Groupby
- Pivot table
- Box plots across groups
- Crosstabs and stacked bar charts
- Chi-square test of independence

### Part 9 — Multivariate Analysis (10 min)
- `hue` plots (sns.scatterplot with hue)
- `pairplot`
- Binning with `pd.cut` (equal width) vs `pd.qcut` (equal frequency)
- Feature engineering: creating `uses_ai` (True / False)

### Part 10 — Wrap-Up & Practice (10 min)
- Reusable `quick_eda()` function
- **Insights table** — filled together in class
- **9 practice exercises** (easy, medium, challenging)
- One-page cheat sheet

---

## Notebook

The session notebook is available in this folder:

`Python_Session_6.ipynb`

To run it, open the file and select **"Open in Colab"** at the top of the notebook page. This will open the notebook directly in Google Colab.

---

## Dataset

We use the same dataset as Session 3 and Session 5:

`academic_data.csv`

**Steps:**
1. Download it from the [Session 3 folder](../session-3/).
2. Save it to your Google Drive at:  
   `MyDrive/Colab Notebooks/Data/academic_data.csv`
3. Make sure you can locate the file during the session.

---

## ⚠️ Two Important Notes

### 1. `df_clean` vs original `df`

The notebook creates a new DataFrame called **`df_clean`**. This is a **copy** of the original — safe to modify. In `df_clean`, we fill the 7 missing `ai_tool` values with `"No Tool"`. The **original `df` remains untouched**.

We also verify in Part 2 whether those 7 students really used less AI — which they do, confirming that "No Tool" is a sensible interpretation.

### 2. One cell saves a cleaned CSV (optional)

**Part 10.2** contains a cell that saves a new file called **`academic_data_clean.csv`** into your Drive's Data folder. The original `academic_data.csv` is **not affected**.

If you don't want to create this new file, simply **skip that cell** and run the rest of the notebook normally.

---

## Insights Table — Filled in Class

The notebook has an **insights table** (Section 10.1) that is **deliberately left blank**. This is not an oversight — it is a teaching decision.

After you have run all the code and looked at the actual outputs, you will fill this table **in class, together**. Each row asks you to:
- State a pattern or finding
- Quote the number that supports it
- Suggest why it might be happening

This is the most valuable part of EDA — *interpreting* the numbers, not just computing them.

---

## Practice Problems

The final section contains **9 practice exercises** divided into three levels.

**Easy (3 exercises)**  
Direct applications of the tools learned: `value_counts`, `describe`, `groupby`.

**Medium (3 exercises)**  
Require combining two or more techniques: outliers + filtering, crosstab + interpretation, binned category + groupby.

**Challenging (3 exercises)**  
Open-ended questions that require visualisation, feature engineering, and reasoning about whether a pattern is *real* or an *artifact*.

Participants are encouraged to attempt each problem independently before referring to any solution. These are the exact types of questions that appear in research and analytical interviews.

---

## Cheat Sheet

The notebook ends with a **one-page cheat sheet** listing all the key pandas commands used in this session — sorted by purpose (load, inspect, summarise, visualise, group). Save it as a quick reference for your future work.

---

## Instructor

**Ramesh Beniwal**  
Coordinator, Quant Society Club  
Department of Economics  
Azim Premji University, Bhopal

---

## Notes

This material is intended for members of the Quant Society Club at Azim Premji University, Bhopal. The notebook and dataset may be reused for educational purposes with appropriate attribution.
