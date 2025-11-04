# Homework 1 — Data Analysis in Business  
## Customer Analytics (Variant 14)

### Author  
**Anastasia Smirnova 233**  

---

## Project Overview
This repository contains the solution for **Homework 1** of the *Data Analysis in Business* course.  
The task focuses on analyzing a dataset with **bank loan applications** and **existing client information**.

The main goal is to:
1. Explore and clean the dataset;  
2. Prepare a data mart for segmentation;  
3. Build two independent segmentation methods (RFM and K-Means);  
4. Evaluate the number of clusters;  
5. Describe and visualize customer profiles.

All analysis, code, comments, and visualizations are included directly in the Jupyter/Colab notebook.

---
## How to Run the Project

### Option 1 — Google Colab
1. Open [Google Colab](https://colab.research.google.com/).  
2. Upload `HW1_Var14_Analytics.ipynb`.  
3. Run all cells (`Runtime → Run all`).  
4. When prompted, upload the dataset `HW1_var_14.csv`.  
5. The notebook will generate:
   - `final_datamart_var14.csv`  
   - `segmentation_outputs_var14.csv`  

### Option 2 — Local Jupyter
```bash
git clone https://github.com/<your-username>/HW_1_2025-Smirnova_Anastasia.git
cd HW_1_2025-Smirnova_Anastasia
pip install -r requirements.txt
jupyter notebook HW1_Var14_Analytics.ipynb
```

---

## Methodology and Workflow

### Part 1 – Data Exploration and Preparation 
- Examined data completeness and consistency.
- Counted unique, zero, and missing values.
- Checked distributions by numeric and categorical features.
- Cleaned missing or invalid entries and encoded categories.
- Built the final data mart for segmentation.

### Part 2 – Two Segmentation Methods 

#### RFM Segmentation 
- Recency → synthetic (no date)
- Frequency → transaction or loan count
- Monetary → loan amount or credit limit sum
- Five RFM segments built using quantiles

#### K-Means Clustering
- Scaled numerical features
- Tested k = 2–10
- Selected optimal k = 5 using Elbow, Silhouette, Calinski-Harabasz, and Davies-Bouldin metrics

### Part 3 – Cluster Evaluation 
- Compared quality metrics for different k values
- Selected balanced segmentation with k = 5
- Visualized cluster sizes using a pie chart

### Part 4 – Customer Profiling 
- Created descriptive profiles for each segment based on median values
- Summarized typical demographic and behavioral traits
- Visualized cluster profiles using bar plots and PCA scatterplots

---

## Visualizations Included
- Histograms and boxplots of numeric features
- Category distributions (e.g., gender, region)
- RFM scatter plots (Frequency vs Monetary by segment)
- K-Means Elbow curve and metrics table
- PCA visualization of clusters
- Pie chart of cluster proportions
- Median feature profiles per cluster
