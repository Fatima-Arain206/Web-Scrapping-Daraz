# Web-Scrapping-Daraz
# Daraz E-Commerce Intelligence System

A complete end-to-end **Web Scraping, Data Engineering, Statistical Analysis, Machine Learning, and Recommendation System** built using real-world e-commerce product data.

The main purpose of this project is to collect product data from Daraz, clean and validate the collected data, store it in a structured database, perform statistical and exploratory analysis, train machine learning models, and finally provide useful product insights and recommendations through an interactive dashboard.

---

## 🎯 Project Objective

The objective of this project is not just to scrape product information.

We aim to build a complete data pipeline:

```text
Daraz Website
      ↓
Web Scraping
      ↓
Raw Data Collection
      ↓
Data Cleaning
      ↓
Data Validation
      ↓
Database Storage
      ↓
Exploratory Data Analysis
      ↓
Statistical Analysis
      ↓
Feature Engineering
      ↓
Machine Learning
      ↓
Model Evaluation
      ↓
Product Prediction & Recommendation
      ↓
Interactive Dashboard
```

The project will demonstrate how raw web data can be transformed into meaningful business insights and intelligent predictions.

---

# 🚀 Project Features

The system is planned to include the following major components:

* Web scraping
* Automated data collection
* Data cleaning
* Missing-value handling
* Duplicate detection
* Data validation
* Data normalization
* Oracle database integration
* Exploratory Data Analysis (EDA)
* Descriptive statistics
* Inferential statistics
* Correlation analysis
* Feature engineering
* Machine learning
* Model training
* Model evaluation
* Product ranking
* Product recommendation
* Price analysis
* Price prediction
* Interactive visualization
* Dashboard

---

# 🏗️ System Architecture

The project will follow a modular data pipeline.

```text
                         ┌──────────────────┐
                         │  Daraz Website   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │   Web Scraper    │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │    Raw Data      │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Data Cleaning    │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Data Validation  │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Oracle Database  │
                         └────────┬─────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    ▼                           ▼
          ┌──────────────────┐        ┌──────────────────┐
          │ Statistical      │        │ Exploratory      │
          │ Analysis         │        │ Data Analysis    │
          └────────┬─────────┘        └────────┬─────────┘
                   │                           │
                   └─────────────┬─────────────┘
                                 ▼
                       ┌──────────────────┐
                       │ Feature          │
                       │ Engineering      │
                       └────────┬─────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │ Machine Learning │
                       └────────┬─────────┘
                                │
                                ▼
                       ┌──────────────────┐
                       │ Model Evaluation │
                       └────────┬─────────┘
                                │
                     ┌──────────┴──────────┐
                     ▼                     ▼
              ┌──────────────┐      ┌──────────────┐
              │ Prediction   │      │ Recommendation│
              └──────┬───────┘      └──────┬───────┘
                     │                     │
                     └──────────┬──────────┘
                                ▼
                       ┌──────────────────┐
                       │ Interactive      │
                       │ Dashboard        │
                       └──────────────────┘
```

---

# 📌 Project Phases

## Phase 1 — Project Planning

Before writing the scraper, we will define:

* Project objectives
* Data requirements
* Required product fields
* Scraping strategy
* Database structure
* Analysis questions
* Statistical questions
* Machine learning problems
* Evaluation metrics
* Dashboard requirements

The project will be developed incrementally instead of trying to build everything at once.

---

# 🕷️ Phase 2 — Web Scraping

The first technical stage is collecting product data from Daraz.

### Planned Technologies

* Python
* Requests
* BeautifulSoup
* Selenium/Playwright if required for dynamically rendered content

### Initial Product Fields

The scraper may collect fields such as:

```text
Product ID
Product Name
Category
Brand
Price
Original Price
Discount
Rating
Review Count
Sold Count
Seller Name
Seller Rating
Seller Location
Product URL
Scrape Date
```

The exact fields will be finalized after studying the structure of the target pages.

### Important Principle

The initial 10-product dataset will be treated as a **testing dataset**.

For meaningful statistics and machine learning, the final dataset will be expanded to a substantially larger number of observations where possible.

---

# 🧹 Phase 3 — Data Cleaning

Raw scraped data cannot be directly used for analysis.

The cleaning pipeline will handle:

### Missing Values

* Detect missing values
* Analyze their causes
* Decide whether to remove, replace, or retain them

### Duplicate Data

* Detect duplicate products
* Remove or appropriately handle duplicates

### Data Types

Convert values into proper formats.

Example:

```text
"Rs. 3,499"
        ↓
3499
```

```text
"4.7 ★"
        ↓
4.7
```

```text
"1.2K reviews"
        ↓
1200
```

### Other Cleaning Tasks

* Remove unwanted characters
* Normalize text
* Standardize categories
* Normalize brands
* Handle inconsistent seller names
* Detect invalid prices
* Detect invalid ratings
* Handle outliers

---

# 🧪 Phase 4 — Data Validation

After cleaning, the dataset will be validated using predefined rules.

Example:

```text
Price > 0

Rating >= 0 and Rating <= 5

Review Count >= 0

Discount >= 0 and Discount <= 100

Product Name must not be empty

Product URL must be valid
```

Invalid records will be flagged for further investigation.

---

# 🗄️ Phase 5 — Database Design

Clean data will be stored in a structured **Oracle Database**.

Instead of keeping everything in one large table, the database will use related entities.

### Planned Entities

```text
PRODUCT
CATEGORY
BRAND
SELLER
PRICE_HISTORY
PRODUCT_RATING
SCRAPE_HISTORY
```

The final schema will be designed after understanding the actual scraped data.

### Database Goals

* Reduce data redundancy
* Maintain relationships
* Preserve historical data
* Support efficient queries
* Support statistical analysis
* Support machine learning data preparation

---

# 🔍 Phase 6 — Exploratory Data Analysis

EDA will be performed to understand the dataset before applying machine learning.

### Questions We Will Investigate

#### Product Analysis

* What are the most common categories?
* Which brands appear most frequently?
* Which products have the highest ratings?
* Which products have the most reviews?

#### Price Analysis

* What is the average product price?
* What is the median price?
* Which category is most expensive?
* Which category is cheapest?
* How are prices distributed?

#### Rating Analysis

* What is the average rating?
* Which category has the highest average rating?
* Are highly rated products also highly reviewed?

#### Discount Analysis

* Which products have the largest discounts?
* Does a higher discount relate to popularity?
* Are heavily discounted products actually cheaper?

---

# 📊 Phase 7 — Statistical Analysis

Statistics will be an important part of the project.

## Descriptive Statistics

We will calculate:

* Mean
* Median
* Mode
* Minimum
* Maximum
* Range
* Variance
* Standard deviation
* Quartiles
* Percentiles
* IQR

## Distribution Analysis

We will investigate:

* Skewness
* Kurtosis
* Distribution shape
* Outliers

## Relationship Analysis

We will study:

* Correlation
* Covariance
* Price vs Rating
* Price vs Reviews
* Discount vs Reviews
* Rating vs Reviews

---

# 🧠 Inferential Statistics

Where the dataset and research question support it, we will apply inferential statistics.

Possible techniques include:

* Confidence intervals
* Hypothesis testing
* t-test
* ANOVA
* Chi-square test

### Example Research Question

**Null Hypothesis (H₀):**

There is no significant difference in ratings between discounted and non-discounted products.

**Alternative Hypothesis (H₁):**

There is a significant difference in ratings between discounted and non-discounted products.

Statistical tests will be selected according to the actual data and assumptions rather than applying tests unnecessarily.

---

# ⚙️ Phase 8 — Feature Engineering

Before machine learning, raw data will be converted into useful model features.

Possible engineered features:

```text
Discount Percentage
Price Category
Review Density
Popularity Score
Seller Score
Rating Weight
Log Review Count
Price-to-Rating Ratio
```

Categorical variables such as:

```text
Category
Brand
Seller
```

will be encoded appropriately for machine learning.

---

# 🤖 Phase 9 — Machine Learning

Machine learning will be introduced only after the data has been properly cleaned, analyzed, and prepared.

The exact ML problem will depend on the quality and quantity of collected data.

## Possible ML Problem 1 — Price Prediction

### Features

```text
Category
Brand
Rating
Review Count
Discount
Seller Rating
Sold Count
```

### Target

```text
Product Price
```

Possible models:

* Linear Regression
* Random Forest
* Gradient Boosting

---

# 🎯 Possible ML Problem 2 — Product Rating Prediction

Predict product rating using variables such as:

```text
Price
Discount
Review Count
Seller Rating
Category
Brand
```

---

# 🏆 Possible ML Problem 3 — Product Recommendation

The system can recommend products based on:

* User budget
* Category
* Rating
* Reviews
* Discount
* Product features

Example:

```text
Budget = Rs. 10,000
Category = Electronics
Minimum Rating = 4.0
```

The system can rank suitable products and return the best recommendations.

---

# 📈 Phase 10 — Model Evaluation

Models will not be judged only by a single accuracy value.

## Regression Metrics

For price prediction:

```text
MAE
MSE
RMSE
R²
```

## Classification Metrics

If classification is introduced:

```text
Accuracy
Precision
Recall
F1-Score
Confusion Matrix
```

Different models will be compared and the most suitable model will be selected based on appropriate evaluation metrics.

---

# 🔬 Phase 11 — Model Interpretation

We will also try to understand **why** a model makes its predictions.

Possible techniques:

* Feature importance
* Model coefficients
* Prediction vs actual analysis
* Error analysis

Example question:

> Which features contribute most to product price prediction?

---

# 📊 Phase 12 — Visualization

The project will use visualization to communicate findings.

### Planned Visualizations

* Price distribution
* Rating distribution
* Category comparison
* Brand comparison
* Discount analysis
* Box plots
* Correlation heatmap
* Scatter plots
* Feature importance
* Actual vs predicted values
* Price history

### Technologies

* Matplotlib
* Seaborn
* Plotly

---

# 🌐 Phase 13 — Interactive Dashboard

A final interactive dashboard will be developed.

Possible technology:

**Streamlit**

### Dashboard Sections

```text
Overview
Products
Price Analysis
Rating Analysis
Statistical Analysis
ML Predictions
Recommendations
```

### Filters

Users may be able to filter by:

```text
Category
Brand
Price Range
Rating
Discount
Seller
```

---

# 🔄 Phase 14 — Automation

After the core pipeline works, the scraping process can be automated.

```text
Scheduler
    ↓
Scraper
    ↓
Validation
    ↓
Database
    ↓
Analysis
```

This can allow periodic collection of new product and price data.

---

# 📈 Phase 15 — Price History & Trend Analysis

If data is collected repeatedly, we can create historical price records.

Example:

```text
Date        Price
--------------------
Day 1       5000
Day 2       4800
Day 3       5200
Day 4       4500
```

This enables:

* Price trend analysis
* Price change detection
* Discount monitoring
* Historical comparison

---

# 🧰 Technology Stack

## Programming

* Python

## Web Scraping

* Requests
* BeautifulSoup
* Selenium/Playwright if required

## Data Processing

* Pandas
* NumPy

## Statistics

* SciPy
* Statsmodels

## Visualization

* Matplotlib
* Seaborn
* Plotly

## Machine Learning

* Scikit-learn

## Database

* Oracle Database

## Dashboard

* Streamlit

## Development Tools

* VS Code / Jupyter Notebook
* Git
* GitHub

---

# 📁 Planned Project Structure

```text
Daraz-Ecommerce-Intelligence/
│
├── README.md
│
├── data/
│   ├── raw/
│   ├── cleaned/
│   └── processed/
│
├── scraping/
│   ├── scraper.py
│   ├── config.py
│   └── utils.py
│
├── cleaning/
│   ├── clean_data.py
│   └── validation.py
│
├── database/
│   ├── schema.sql
│   ├── tables.sql
│   └── queries.sql
│
├── analysis/
│   ├── eda.ipynb
│   ├── descriptive_statistics.ipynb
│   └── inferential_statistics.ipynb
│
├── machine_learning/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── train.py
│   ├── evaluate.py
│   └── models/
│
├── dashboard/
│   └── app.py
│
├── reports/
│
├── requirements.txt
│
└── .gitignore
```

---

# 👥 Team Responsibilities

The project will be developed collaboratively.

### Data Collection

* Website research
* Scraping
* Raw dataset collection
* Scraping validation

### Data Engineering

* Cleaning
* Validation
* Database design
* Data transformation

### Statistics & Analysis

* EDA
* Descriptive statistics
* Inferential statistics
* Visualization

### Machine Learning

* Feature engineering
* Model training
* Model evaluation
* Recommendation system

### Dashboard

* Interactive visualizations
* Filters
* Predictions
* Recommendations

Team members will understand the complete pipeline so that every member can explain the project during presentation and viva.

---

# 🗺️ Development Strategy

We will **not build everything at once**.

The project will be developed in stages:

```text
Stage 1
Scrape a small sample
        ↓
Stage 2
Verify and clean the data
        ↓
Stage 3
Build the database
        ↓
Stage 4
Collect a larger dataset
        ↓
Stage 5
Perform EDA
        ↓
Stage 6
Perform statistical analysis
        ↓
Stage 7
Engineer ML features
        ↓
Stage 8
Train ML models
        ↓
Stage 9
Evaluate and improve models
        ↓
Stage 10
Build recommendation system
        ↓
Stage 11
Build dashboard
        ↓
Stage 12
Automate the pipeline
```

This staged approach allows us to detect problems early and avoid building machine learning models on poor-quality data.

---

# ⚠️ Ethical & Technical Considerations

The project will respect the website's applicable:

* Terms of service
* `robots.txt`
* Rate limits
* Access restrictions

Requests will be controlled to avoid unnecessary load on the website.

The project is intended for **educational and research purposes**.

---

# 🎓 Expected Learning Outcomes

By completing this project, we aim to understand the complete journey of data:

```text
Web Data
   ↓
Collection
   ↓
Cleaning
   ↓
Storage
   ↓
Exploration
   ↓
Statistics
   ↓
Feature Engineering
   ↓
Machine Learning
   ↓
Evaluation
   ↓
Prediction
   ↓
Recommendation
   ↓
Visualization
```

The project will provide practical experience in:

* Web scraping
* Data engineering
* Database management
* Statistics
* Data visualization
* Machine learning
* Model evaluation
* Recommendation systems
* Data-driven decision making

---

# 🚀 Future Improvements

Possible future extensions include:

* Larger-scale data collection
* Automated scheduled scraping
* Advanced recommendation algorithms
* Sentiment analysis of product reviews
* Natural Language Processing
* Time-series price prediction
* Anomaly detection
* Product similarity search
* Advanced ML models
* Cloud deployment

---

# 📌 Project Status

**Current Stage:** Planning & Data Collection

```text
[ ] Project Planning
[ ] Web Scraping
[ ] Raw Dataset
[ ] Data Cleaning
[ ] Data Validation
[ ] Oracle Database
[ ] EDA
[ ] Statistical Analysis
[ ] Feature Engineering
[ ] Machine Learning
[ ] Model Evaluation
[ ] Recommendation System
[ ] Dashboard
[ ] Automation
[ ] Final Report
```

---

# 👨‍💻 Team

**Project:** Daraz E-Commerce Intelligence System

**Focus:**

> Web Scraping + Data Engineering + Statistics + Machine Learning + Recommendation System

This project is being developed as an academic data science project with the goal of building a complete real-world data pipeline from web data collection to intelligent decision-making.
