# Session 7: Data Visualisation with Plots

**Quant Society Club**  
Azim Premji University, Bhopal

---

## Overview

In Session 6 we learned how to summarise a dataset with numbers — mean, median, standard deviation, and how to clean missing values.

In this session, we turn those numbers into **pictures**. Data visualisation is how we actually *see* patterns, outliers, and relationships that summary statistics cannot show on their own.

This session is almost entirely about **plots**. We start with **box plots** of the variables, and then move through the complete plot toolkit — histogram, count plot, bar chart, line plot, scatter plot, pie chart, pair plot, and correlation heatmap. For each plot we ask:

1. **What does it show?**
2. **When should we use it?**
3. **How do we build it in Python?**

By the end of the session, you will know which plot to reach for when you have a question about your data.

This is a **2-hour hands-on workshop**. Bring your laptop with Google Colab open.

---

## Learning Objectives

Upon completion of this session, participants should be able to:

- Read and interpret a **box plot** (quartiles, median, whiskers, outliers)
- Plot box plots for every continuous variable in a dataset
- Plot box plots **grouped by a categorical variable** (e.g. marks by grade)
- Choose the right plot for the right question
- Build the following plots using `matplotlib` and `pandas`:
  - Box plot
  - Histogram
  - Count plot (bar chart of frequencies)
  - Bar chart
  - Line plot
  - Scatter plot
  - Pie chart
  - Pair plot
  - Correlation heatmap
- Read a correlation heatmap and interpret the strength and direction of relationships
- Avoid common mistakes (e.g. using a pie chart for too many categories, misleading axes)

---

## Session Outline (2-Hour Structure)

### Part 1 — Recap & Setup (10 min)
- Recap of Session 6 (summary statistics and cleaning)
- Mount Drive, load `academic_data.csv`
- Import plotting libraries: `matplotlib` and `pandas`

### Part 2 — Box Plots (25 min)
- What a box plot is: quartiles, median, IQR, whiskers, outliers
- Box plot of a single continuous variable (`marks`)
- Box plots of all continuous variables at once
- Box plots grouped by a categorical variable (`marks` by `grade`, `study_hours` by `section`)
- Reading outliers in a box plot

### Part 3 — Histograms (15 min)
- What a histogram shows: shape of a single variable
- Choosing the number of bins
- Comparing histograms of two variables side by side

### Part 4 — Count Plots & Bar Charts (15 min)
- Count plot: how often each category appears
- Bar chart: comparing a numeric value across categories
- Grouped bar chart (e.g. average marks by grade and gender)

### Part 5 — Line Plots (10 min)
- When a line plot makes sense (ordered data)
- Plotting a running average of marks over student ID

### Part 6 — Scatter Plots (15 min)
- Scatter plot of two continuous variables
- Adding a trend line
- Using colour (`hue`) to show a third variable

### Part 7 — Pie Chart (5 min)
- When a pie chart works and when it doesn't
- Pie chart of grade distribution

### Part 8 — Pair Plots & Correlation Heatmap (15 min)
- Pair plot: every continuous variable vs every other
- Correlation heatmap: strength of relationships at a glance
- Interpreting positive vs negative correlation

### Part 9 — Choosing the Right Plot (10 min)
- A decision table: question → plot type
- Common mistakes to avoid
- Hands-on practice: plot for 5 given questions

### Part 10 — Wrap-Up & Practice (10 min)
- Summary of all plots covered
- Practice exercises
- Preview of Session 8

---

## Notebook

The session notebook is available in this folder:

`Python_Session_7.ipynb`

To run it, open the file and select **"Open in Colab"** at the top of the notebook page. This will open the notebook directly in Google Colab.

---

## Dataset

We use the same dataset as Sessions 3, 5, and 6:

`academic_data.csv`

**Steps:**
1. Download it from the [Session 3 folder](../session-3/).
2. Save it to your Google Drive at:  
   `MyDrive/Colab Notebooks/Data/academic_data.csv`
3. Confirm you can locate the file during the session.

---

## Plots We Will Cover — Quick Reference

| Plot | Best For | What It Shows |
|---|---|---|
| **Box plot** | Continuous variable, comparison across groups | Quartiles, median, outliers |
| **Histogram** | Single continuous variable | Shape of the distribution |
| **Count plot** | Categorical variable | Frequency of each category |
| **Bar chart** | Comparing a numeric value across categories | Rank / size comparison |
| **Line plot** | Ordered data (time series) | Trends over an order |
| **Scatter plot** | Two continuous variables | Relationship between two variables |
| **Pie chart** | Few categories | Proportions of a whole |
| **Pair plot** | Several continuous variables | Every pairwise relationship |
| **Correlation heatmap** | Several continuous variables | Strength and direction of relationships |

---

## Key Interpretations to Remember

### Box plot
- The **box** covers the middle 50% of the data (Q1 to Q3).
- The **line inside** the box is the median.
- The **whiskers** extend to the smallest and largest non-outlier values.
- **Dots beyond the whiskers** are outliers.

### Histogram
- **Right-skewed:** long tail on the right (mean > median).
- **Left-skewed:** long tail on the left (mean < median).
- **Symmetric:** mean ≈ median.

### Correlation heatmap
- Values range from **−1 to +1**.
- **+1** = perfect positive relationship.
- **0** = no linear relationship.
- **−1** = perfect negative relationship.
- Correlation does **not** imply causation.

---

## Common Mistakes to Avoid

1. **Using a pie chart with too many slices** — after ~5 categories a bar chart is clearer.
2. **Forgetting to label axes** — every plot should have a title, x-axis label, and y-axis label.
3. **Using a line plot for unordered categories** — line plots imply an order.
4. **Truncating the y-axis** to exaggerate differences — always start at 0 for bar charts.
5. **Assuming correlation means causation** — two variables can move together because of a third factor.

---

## Practice Problems

Practice problems will be released after the session. They will focus on:

- Choosing the appropriate plot for a given question
- Building the plot in Python
- Writing a one-line interpretation of what the plot shows

Participants are encouraged to attempt each problem independently before referring to any solution.

---

## Instructor

**Ramesh Beniwal**  
Coordinator, Quant Society Club  
Department of Economics  
Azim Premji University, Bhopal

---

## Notes

This material is intended for members of the Quant Society Club at Azim Premji University, Bhopal. The notebook and dataset may be reused for educational purposes with appropriate attribution.
