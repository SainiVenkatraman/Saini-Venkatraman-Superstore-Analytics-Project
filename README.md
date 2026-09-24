# Superstore Sales Analytics, Profit Prediction and Customer Segmentation Using Machine Learning

## AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026

---

## 1. Project Overview

Data analytics enables organizations to transform raw business data into meaningful insights that support data-driven decision-making.

This project analyzes the **Superstore retail dataset** to understand sales performance, profitability, customer purchasing behavior, product performance, regional trends, and relationships between important business variables.

The project follows an end-to-end data analytics and machine learning workflow, beginning with data loading and preprocessing and progressing through exploratory data analysis, feature engineering, statistical analysis, predictive modeling, classification, and customer segmentation.

Three machine learning approaches are implemented:

1. **Linear Regression** for Sales prediction.
2. **Decision Tree Classification** for Profitability prediction.
3. **K-Means Clustering** for customer segmentation.

The project demonstrates the practical application of Python-based data analytics and machine learning techniques to a real-world retail dataset.

---

## 2. Problem Statement

The objective of this project is to analyze historical Superstore sales data and identify meaningful patterns related to sales, profit, customers, products, discounts, and regional performance.

The project also aims to use machine learning techniques to:

* Predict Sales using relevant business features.
* Classify orders as Profitable or Non-Profitable.
* Segment customers according to their purchasing behavior.

The resulting analysis and models provide a structured approach for understanding business performance and customer behavior.

---

## 3. Project Objectives

The major objectives of this project are:

* Understand the structure and characteristics of the Superstore dataset.
* Clean and preprocess the raw data.
* Perform exploratory data analysis.
* Analyze sales and profitability patterns.
* Study relationships between numerical variables.
* Perform feature engineering using date and business-related attributes.
* Predict Sales using Linear Regression.
* Classify orders based on profitability using a Decision Tree Classifier.
* Evaluate classification performance using multiple metrics.
* Segment customers using K-Means clustering.
* Determine a suitable number of customer clusters using Silhouette Score.
* Analyze the characteristics of each customer segment.
* Export important machine learning results as CSV files.
* Generate meaningful business insights from the analysis.

---

## 4. Dataset

The project uses the **Superstore retail dataset** containing transactional information about customers, orders, products, sales, discounts, quantities, regions, and profitability.

The project uses the **Superstore Dataset** (`sample_-_superstore.xls`) for sales analytics, profitability prediction, and customer segmentation.

**Dataset Link:**
[Superstore Dataset – Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

The dataset contains information related to orders, customers, products, sales, discounts, shipping, and profit, which enables exploratory data analysis and machine learning-based analysis.

### Major Dataset Attributes

Important attributes used in the analysis include:

* Order ID
* Order Date
* Ship Date
* Ship Mode
* Customer ID
* Customer Name
* Segment
* Country
* City
* State
* Postal Code
* Region
* Product ID
* Category
* Sub-Category
* Product Name
* Sales
* Quantity
* Discount
* Profit

---

## 5. Technologies Used

### Programming Language

* Python 3

### Development Environment

* Jupyter Notebook / JupyterLab

### Python Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy

### Machine Learning Techniques

* Linear Regression
* Decision Tree Classification
* K-Means Clustering

---

## 6. Project Workflow

The project follows the following analytical workflow:

```text
Superstore Dataset
        ↓
Data Loading
        ↓
Data Inspection
        ↓
Data Cleaning & Preprocessing
        ↓
Exploratory Data Analysis
        ↓
Statistical Analysis
        ↓
Feature Engineering
        ↓
Machine Learning
        ├── Linear Regression
        ├── Decision Tree Classification
        └── K-Means Clustering
        ↓
Model Evaluation
        ↓
Customer Segment Analysis
        ↓
Result Export
        ↓
Business Insights
```

---

# 7. Data Loading and Initial Exploration

The dataset is loaded using Pandas and examined to understand its structure.

The initial analysis includes:

* Viewing the first and last records.
* Examining column names.
* Checking dataset dimensions.
* Inspecting data types.
* Generating descriptive statistics.
* Identifying missing values.
* Checking duplicate records.

This stage establishes an understanding of the dataset before further analysis.

---

# 8. Data Preprocessing

Data preprocessing is performed to prepare the dataset for analysis and machine learning.

The preprocessing stage includes:

* Handling missing values.
* Checking duplicate records.
* Converting date columns into appropriate datetime formats.
* Preparing numerical and categorical variables.
* Creating customer-level aggregated data for segmentation.
* Preparing features required by machine learning models.

For machine learning pipelines, appropriate preprocessing techniques are applied to numerical and categorical features.

---

# 9. Exploratory Data Analysis

Exploratory Data Analysis (EDA) is performed to identify patterns, trends, distributions, and relationships within the Superstore dataset.

The analysis examines areas such as:

* Sales performance.
* Profit performance.
* Quantity distribution.
* Discount patterns.
* Category-wise performance.
* Sub-category performance.
* Segment-wise performance.
* Regional performance.
* State-level performance.
* Customer behavior.
* Relationships between Sales, Profit, Quantity, and Discount.

### Visualizations

The project uses:

* Bar charts
* Line charts
* Histograms
* Box plots
* Scatter plots
* Heatmaps

These visualizations help communicate analytical findings clearly.

---

# 10. Feature Engineering

Additional features are created from the original dataset to support deeper analysis and machine learning.

### Date-Based Features

The following features are extracted from `Order Date`:

* Year
* Month
* Month Name
* Quarter

### Shipping Feature

A `Shipping Days` feature is calculated using:

```text
Ship Date - Order Date
```

This represents the number of days required to ship an order.

### Profit Margin

Profit Margin is calculated as:

```text
Profit Margin = (Profit / Sales) × 100
```

### Profitability Classification

Orders are classified into two categories:

```text
Profitable
Non-Profitable
```

An order is considered **Profitable** when its Profit is greater than zero; otherwise it is classified as **Non-Profitable**.

---

# 11. Statistical Analysis

Statistical analysis is used to understand the characteristics and relationships within the dataset.

The project uses descriptive statistics and correlation analysis to examine important numerical variables.

Variables considered include:

* Sales
* Profit
* Quantity
* Discount
* Shipping-related measures

Correlation analysis helps identify the strength and direction of relationships between numerical variables.

---

# 12. Machine Learning and Predictive Analytics

Machine learning is applied to the Superstore dataset using three different approaches.

## 12.1 Regression — Sales Prediction

### Objective

The regression model predicts **Sales** using selected business and order-related features.

### Features Used

Numerical features:

* Quantity
* Discount
* Shipping Days

Categorical features:

* Ship Mode
* Segment
* Region
* Category
* Sub-Category

### Model

**Linear Regression**

### Preprocessing

The regression pipeline uses:

* Median imputation for numerical variables.
* Most-frequent imputation for categorical variables.
* One-hot encoding for categorical variables.

The data is divided into training and testing sets before model training.

### Evaluation Metrics

The regression model is evaluated using:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score

Actual and predicted Sales values are also compared visually.

---

# 13. Classification — Profitability Prediction

## Objective

The classification model predicts whether an order is:

```text
Profitable
```

or

```text
Non-Profitable
```

### Features Used

Numerical features:

* Sales
* Quantity
* Discount
* Shipping Days

Categorical features:

* Ship Mode
* Segment
* Region
* Category
* Sub-Category

### Model

**Decision Tree Classifier**

The Decision Tree is configured with:

* Maximum depth: 6
* Random state: 42
* Balanced class weights

### Preprocessing

The classification pipeline applies:

* Median imputation to numerical variables.
* Most-frequent imputation to categorical variables.
* One-hot encoding to categorical variables.

### Evaluation Metrics

The model is evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix
* Classification Report

A visualization of the trained Decision Tree is also included in the notebook.

---

# 14. Customer Segmentation Using K-Means

Customer segmentation is performed to group customers according to their purchasing behavior.

Customer-level data is created using aggregated purchasing information.

### Clustering Features

The following features are used:

* Total Sales
* Total Profit
* Total Quantity
* Order Count
* Average Order Value

### Data Standardization

The clustering features are standardized using `StandardScaler`.

Standardization ensures that features with different numerical scales can contribute appropriately to the clustering process.

### Determining the Number of Clusters

K-Means clustering is evaluated for values of:

```text
K = 2 to 6
```

Silhouette Score is calculated for each value of K.

The K value producing the highest Silhouette Score is automatically selected for the final clustering model.

### Final Clustering Model

The final customer segmentation is performed using:

**K-Means Clustering**

with:

* Automatically selected number of clusters.
* `random_state = 42`
* `n_init = 10`

---

# 15. Customer Segment Analysis

After clustering, each customer is assigned to a cluster.

The project analyzes each cluster using:

* Number of customers.
* Average Sales.
* Average Profit.
* Average Quantity.
* Average Orders.
* Average Order Value.

A scatter plot is also used to visualize customer segments based on Sales and Profit.

This analysis helps identify differences in customer purchasing behavior across the generated segments.

---

# 16. Model Evaluation Summary

The notebook provides a consolidated machine learning summary containing:

### Regression

* MAE
* RMSE
* R² Score

### Classification

* Accuracy
* Precision
* Recall
* F1 Score

### Clustering

* Selected number of clusters (K)
* Silhouette Score analysis

---

# 17. Output Files

The project exports important machine learning results into CSV files.

| File                         | Description                               |
| ---------------------------- | ----------------------------------------- |
| `regression_results.csv`     | Regression evaluation metrics             |
| `classification_results.csv` | Classification evaluation metrics         |
| `customer_segments.csv`      | Customer-level data with assigned cluster |
| `cluster_profile.csv`        | Summary profile of customer clusters      |

These files make the important analytical results available outside the Jupyter Notebook.

---

# 18. Project Structure

```text
Superstore Analytics/
│
├── sample_-_superstore.xls
│
├── Saini_Venkatraman_Superstore_Analytics.ipynb
│
├── regression_results.csv
├── classification_results.csv
├── customer_segments.csv
├── cluster_profile.csv
│
├── requirements.txt
└── README.md
```

---

# 19. How to Run the Project

## Step 1: Install Python

Install Python 3 on the system.

## Step 2: Clone or Download the Project

Place all project files in the same project directory.

## Step 3: Install Dependencies

Open Command Prompt or Terminal inside the project directory and run:

```bash
pip install -r requirements.txt
```

## Step 4: Start Jupyter

Run:

```bash
jupyter lab
```

or:

```bash
jupyter notebook
```

## Step 5: Open the Notebook

Open:

```text
Saini_Venkatraman_Superstore_Analytics.ipynb
```

## Step 6: Run the Notebook

Execute the notebook cells sequentially from beginning to end.

Ensure that:

```text
sample_-_superstore.xls
```

is available in the same working directory as the notebook.

---

# 20. Skills Demonstrated

This project demonstrates practical skills in:

### Python

* Python programming
* Data structures and operations
* Functions and analytical workflows

### Data Analytics

* Data loading
* Data cleaning
* Data preprocessing
* Exploratory Data Analysis
* Descriptive statistics
* Correlation analysis
* Feature engineering

### Data Visualization

* Matplotlib
* Seaborn
* Statistical and business visualizations

### Machine Learning

* Train-test splitting
* Feature preprocessing
* Linear Regression
* Decision Tree Classification
* K-Means Clustering
* Feature scaling
* Model evaluation
* Silhouette analysis

### Business Analytics

* Sales analysis
* Profitability analysis
* Customer behavior analysis
* Customer segmentation
* Business insight generation

---

# 21. Conclusion

This project demonstrates an end-to-end application of data analytics and machine learning techniques to a retail sales dataset.

The analysis begins with data exploration and preprocessing and progresses through feature engineering, statistical analysis, visualization, predictive modeling, classification, and customer segmentation.

Linear Regression is used for Sales prediction, Decision Tree Classification is used for Profitability prediction, and K-Means clustering is used to identify customer segments based on purchasing behavior.

The project demonstrates how Python-based analytical and machine learning techniques can be applied to transform transactional retail data into structured insights and predictive results.

---

## Author

**Saini Venkatraman**

**Project:** Superstore Sales Analytics, Profit Prediction and Customer Segmentation Using Machine Learning

**Program:** AICTE | IBM SkillsBuild Data Analytics with AI Internship 2026

**Tools:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy, Jupyter Notebook
