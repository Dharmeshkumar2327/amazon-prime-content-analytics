# 🎬 Amazon Prime Movies & TV Shows — Power BI Analytics

> **Interactive Power BI dashboard analyzing Amazon Prime Movies and TV Shows using Power BI, SQL, and Python.**

---

## 📊 Dashboard Preview

![Amazon Prime Power BI Dashboard](dashboard/dashboard_overview.png)

---

## 📌 Project Overview

This project presents an interactive **Power BI dashboard for analyzing Amazon Prime Movies and TV Shows**.

The objective is to transform a raw content dataset into a clear and interactive **Business Intelligence solution** that helps users explore the catalog by:

* Content Type
* Country
* Rating
* Genre
* Release Year
* Directors
* Content Metadata

The project demonstrates an end-to-end **Data Analytics workflow**:

**Raw Data → Data Preparation → Data Analysis → Data Modeling → DAX → Power BI Dashboard → Business Insights**

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Analyze the Amazon Prime content catalog.
* Compare **Movies vs TV Shows**.
* Identify countries contributing to the content catalog.
* Analyze content ratings.
* Explore genre and category distribution.
* Study content trends by release year.
* Analyze directors and other content attributes.
* Build an interactive and user-friendly Power BI dashboard.
* Convert raw data into meaningful analytical insights.

---

## ❓ Business Questions

This project is designed to answer the following business questions:

1. How many titles are available in the dataset?
2. What is the distribution between Movies and TV Shows?
3. Which countries contribute the most content?
4. Which genres and categories are most common?
5. Which ratings appear most frequently?
6. How is content distributed across release years?
7. How many directors are represented?
8. What are the major characteristics of the Amazon Prime catalog?
9. How does content distribution vary by type, country, rating, and genre?
10. What patterns can be identified from the available content metadata?

---

# 📈 Dashboard Features

## 🔢 KPI Cards

The dashboard provides high-level KPIs such as:

* **Total Titles**
* **Total Ratings**
* **Genre Categories**
* **Total Directors**
* **Start Date**
* **End Date**

These KPIs provide a quick overview of the dataset.

---

## 🎬 Movies vs TV Shows

A visual comparison between:

* Movies
* TV Shows

helps understand the overall composition of the content catalog.

---

## 🌍 Country Analysis

A geographic visualization is used to analyze the distribution of Amazon Prime titles across different countries.

This allows users to explore the geographical contribution of content.

---

## ⭐ Rating Analysis

The dashboard provides a breakdown of titles by content rating.

This helps identify the most frequently represented ratings within the dataset.

---

## 🎭 Genre Analysis

Genre/category analysis helps identify frequently occurring content categories and provides an overview of the catalog's content mix.

---

## 📅 Release Year Analysis

An interactive release-year visualization helps explore how titles are distributed across different years and compare Movies and TV Shows over time.

---

# 🛠️ Tools & Technologies

| Tool             | Purpose                                 |
| ---------------- | --------------------------------------- |
| **Power BI**     | Dashboard development and visualization |
| **Power Query**  | Data transformation and preparation     |
| **DAX**          | Measures and analytical calculations    |
| **SQL**          | Data querying and analysis              |
| **Python**       | Data cleaning and exploratory analysis  |
| **Pandas**       | Data manipulation                       |
| **NumPy**        | Numerical analysis                      |
| **Matplotlib**   | Exploratory visualization               |
| **Git & GitHub** | Version control and project portfolio   |

---

# 📂 Dataset

The dataset contains information about Amazon Prime Movies and TV Shows.

### Dataset Fields

| Column         | Description                                  |
| -------------- | -------------------------------------------- |
| `show_id`      | Unique identifier for the title              |
| `type`         | Movie or TV Show                             |
| `title`        | Name of the title                            |
| `director`     | Director associated with the title           |
| `cast`         | Cast members                                 |
| `country`      | Country/countries associated with the title  |
| `date_added`   | Date the title was added                     |
| `release_year` | Original release year                        |
| `rating`       | Content rating                               |
| `duration`     | Movie duration or TV-show season information |
| `listed_in`    | Genre/category information                   |
| `description`  | Description of the title                     |

### Data Considerations

Some fields contain missing values.

Fields such as:

* `country`
* `cast`
* `director`
* `listed_in`

may contain multiple values or incomplete information and may require additional transformation for detailed analysis.

---

# 🔄 Data Analytics Workflow

```text
                 RAW DATASET
                     │
                     ▼
              Data Quality Check
                     │
                     ▼
             Data Transformation
                     │
          ┌──────────┴──────────┐
          ▼                     ▼
       Python                  SQL
          │                     │
          └──────────┬──────────┘
                     ▼
              Power BI Model
                     │
                     ▼
                 DAX / KPIs
                     │
                     ▼
           Interactive Dashboard
                     │
                     ▼
              Business Insights
```

---

# 🧹 Data Preparation

The project involves several data preparation activities, including:

* Checking missing values
* Checking duplicate records
* Converting date fields
* Validating release-year values
* Standardizing categorical fields
* Preparing fields for visualization
* Extracting useful analytical attributes
* Preparing data for Power BI modeling

---

# 🧠 Analytical Areas

## 1. Content Type Analysis

Compare Movies and TV Shows to understand the overall structure of the catalog.

## 2. Geographic Analysis

Analyze content distribution across countries.

## 3. Genre Analysis

Identify the most frequently represented genres and categories.

## 4. Rating Analysis

Analyze the distribution of titles across available ratings.

## 5. Release Trend Analysis

Explore the distribution of content by release year.

## 6. Content Metadata Analysis

Explore:

* Directors
* Cast
* Duration
* Country
* Rating
* Genre
* Description

---

# 💡 Key Insights

The following findings are calculated from the project dataset containing **9,668 titles across 12 fields**.

### 🎬 Content Type

* **7,814 Movies** account for **80.82%** of the catalog.
* **1,854 TV Shows** account for **19.18%** of the catalog.
* Movies therefore represent the majority of titles in the dataset.

### 🌍 Geographic Distribution

Based on country occurrences in the dataset:

| Rank | Country        | Titles |
| ---: | -------------- | -----: |
|    1 | United States  |    334 |
|    2 | India          |    246 |
|    3 | United Kingdom |     67 |
|    4 | Canada         |     35 |
|    5 | France         |     20 |

> Country values can contain multiple countries for a single title, so these counts represent country occurrences rather than mutually exclusive titles.

### 🎭 Top Genres

After splitting the multi-value genre/category field:

| Rank | Genre / Category | Titles |
| ---: | ---------------- | -----: |
|    1 | Drama            |  3,687 |
|    2 | Comedy           |  2,099 |
|    3 | Action           |  1,657 |
|    4 | Suspense         |  1,501 |
|    5 | Kids             |  1,085 |
|    6 | Documentary      |    993 |
|    7 | Special Interest |    980 |
|    8 | Horror           |    875 |
|    9 | Romance          |    674 |
|   10 | Animation        |    547 |

> Because a title can belong to multiple categories, genre counts are not mutually exclusive.

### ⭐ Content Ratings

The most frequently occurring ratings are:

| Rank | Rating | Titles |
| ---: | ------ | -----: |
|    1 | 13+    |  2,117 |
|    2 | 16+    |  1,547 |
|    3 | ALL    |  1,268 |
|    4 | 18+    |  1,243 |
|    5 | R      |  1,010 |

The dataset contains **24 distinct rating values**.

### 📅 Release Year

* The dataset covers titles released between **1920 and 2021**.
* The **median release year is 2016**.
* The **average release year is approximately 2008**.
* The **75th percentile is 2019**, meaning at least 25% of titles were released in 2019 or later.

### 🎥 Directors

* The dataset contains **5,773 distinct director values**.
* **2,083 titles** do not have a director value.

This should be considered when performing director-level analysis.

### ⏱️ Movie Duration

For titles classified as Movies:

* **Average duration:** approximately **91.3 minutes**
* **Median duration:** **91 minutes**
* **25th percentile:** **75 minutes**
* **75th percentile:** **106 minutes**

### 🧹 Data Quality

Several fields contain missing values:

| Field        | Missing Records |
| ------------ | --------------: |
| `date_added` |           9,513 |
| `country`    |           8,996 |
| `director`   |           2,083 |
| `cast`       |           1,233 |
| `rating`     |             337 |

These missing values should be considered when creating filters, KPIs, and analytical measures.

### 📌 Overall Finding

The dataset is strongly weighted toward **Movies (80.82%)**. **Drama, Comedy, Action, and Suspense** are among the most frequently occurring categories. The **United States and India** have the highest country occurrence counts, while the catalog has a **median release year of 2016**.

---

# 🐍 Python Analysis

Python can be used for data cleaning and exploratory data analysis.

### Main Python Tasks

* Data loading
* Data profiling
* Missing-value analysis
* Duplicate checking
* Data transformation
* Exploratory analysis
* Statistical summaries
* Visualization

### Python Libraries

```text
Pandas
NumPy
Matplotlib
```

Python analysis files are available in:

```text
python/
```

---

# 🗄️ SQL Analysis

SQL is used to perform analytical queries and answer business questions.

### SQL Concepts Demonstrated

* `SELECT`
* `WHERE`
* `GROUP BY`
* `ORDER BY`
* `CASE`
* Aggregate Functions
* `JOIN`
* CTEs
* Window Functions
* Data Quality Queries

### Example Query

```sql
SELECT
    type,
    COUNT(*) AS total_titles
FROM amazon_prime_titles
GROUP BY type
ORDER BY total_titles DESC;
```

SQL analysis files are available in:

```text
sql/
```

---

# 📊 Power BI

The Power BI report demonstrates:

* Power Query
* Data Modeling
* DAX
* KPI Cards
* Slicers
* Filters
* Maps
* Charts
* Interactive Visualizations
* Dashboard Design

The Power BI file is available in:

```text
powerbi/
```

---

# 🧠 Skills Demonstrated

## Power BI

* Power Query
* Data Modeling
* DAX
* KPI Development
* Slicers
* Filters
* Maps
* Interactive Visualizations
* Dashboard Design

## SQL

* Data Aggregation
* Filtering
* Grouping
* CASE Statements
* Joins
* CTEs
* Window Functions
* Analytical Queries

## Python

* Pandas
* NumPy
* Data Cleaning
* Missing Value Analysis
* Exploratory Data Analysis
* Data Transformation
* Data Visualization

## Data Analytics

* Business Question Development
* Data Preparation
* Exploratory Analysis
* KPI Development
* Trend Analysis
* Data Visualization
* Business Intelligence

---

# 📁 Repository Structure

```text
amazon-prime-content-analytics/
│
├── README.md
│
├── data/
│   └── amazon_prime_titles.csv
│
├── powerbi/
│   └── Amazon_Prime_Content_Analytics.pbix
│
├── dashboard/
│   ├── dashboard_overview.png
│   └── dashboard_details.png
│
├── python/
│   └── amazon_prime_analysis.py
│
├── sql/
│   └── amazon_prime_analysis.sql
│
└── documentation/
    └── data_dictionary.md
```

---

# 🚀 Future Enhancements

Potential improvements for future versions include:

* Advanced DAX measures
* Dedicated Content Explorer page
* Genre normalization
* Country normalization
* Detailed movie-duration analysis
* Time-series analysis
* Sentiment analysis using descriptions
* Content recommendation prototype
* Machine-learning based content classification
* Comparison with other streaming platforms
* Automated data refresh

---

# 💼 Portfolio Value

This project demonstrates an end-to-end approach to solving a data analytics problem:

```text
Raw Data
   ↓
Data Cleaning
   ↓
Data Analysis
   ↓
SQL
   ↓
Python
   ↓
Data Modeling
   ↓
Power BI
   ↓
Visualization
   ↓
Business Insights
```

The project demonstrates practical skills relevant to roles such as:

* **Data Analyst**
* **Business Intelligence Analyst**
* **Power BI Developer**
* **Reporting Analyst**
* **Junior Data Scientist**

---

# 👨‍💻 About Me

## Dharmesh Kumar

**Data Analyst | SQL | Python | Power BI**

I am interested in transforming raw data into meaningful insights through **Data Analytics, Business Intelligence, SQL, Python, and Power BI**.

### Technical Skills

**Programming:**
Python, SQL, C, C++, Java

**Data Analytics:**
Pandas, NumPy, Power BI, Tableau, Excel, Matplotlib

**Databases:**
MySQL, PostgreSQL, Oracle, MongoDB

**Other:**
Data Cleaning, Data Modeling, DAX, EDA, Git & GitHub

---

# 📫 Connect With Me

* 🔗 **GitHub:** [Dharmeshkumar2327](https://github.com/Dharmeshkumar2327)
* 🔗 **LinkedIn:** [Dharmesh Kumar](https://www.linkedin.com/in/dharmesh-kumar-293a89)

---

# ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.

Thank you for visiting and exploring this project! 🚀
