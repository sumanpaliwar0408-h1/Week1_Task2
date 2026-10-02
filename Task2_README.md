# Task 2 --- Sales Data Analysis

## Data Science Internship --- Week 1

**Organization:** WeIntern Pvt Ltd\
**Task:** Task 2 --- Sales Data Analysis\
**Objective:** Analyze a sales dataset to evaluate business performance,
identify sales patterns, and generate customer-focused insights using
accurate KPI definitions and evidence-based interpretation.

## Project Overview

This project analyzes the Sample Superstore dataset using Python and
Pandas. The analysis focuses on core sales KPIs, time-based trends,
category and product performance, regional and customer-segment
differences, and customer purchasing behavior.

Because the source dataset is stored at **order-line level**, a single
Order ID may appear on multiple rows. Therefore, order-based metrics use
**distinct Order ID** rather than row count.

## Dataset Description

The Sample Superstore dataset contains:

-   **9,994 order-line records**
-   **21 original columns**
-   **5,009 unique orders**
-   **793 unique customers**
-   **1,850 unique products**
-   Order dates covering **2014--2017**

The dataset includes order, customer, product, geographic, shipping,
sales, quantity, discount, and profit information.

## Tools and Libraries

-   Python
-   Pandas
-   Jupyter Notebook

## Analytical Preparation

The analysis includes:

-   Dataset structure and data-type inspection
-   Standardization of column names to lowercase `snake_case`
-   Date parsing and validation
-   Creation of year, month, and year-month fields
-   Distinct-order logic for order-based metrics
-   Order-level aggregation where required
-   Category, product, region, segment, and customer-level grouping

## Core KPI Summary

  -----------------------------------------------------------------------
  KPI                                                              Result
  ------------------------------ ----------------------------------------
  Total Revenue                                            \$2,297,200.86

  Total Orders                                                      5,009

  Average Order Value                                            \$458.61

  Total Units Sold                                                 37,873

  Top-Selling Category by                                      Technology
  Revenue                        

  Top Revenue-Generating Product    Canon imageCLASS 2200 Advanced Copier
  -----------------------------------------------------------------------

**KPI definitions:**

-   **Total Revenue:** Sum of the `Sales` field.
-   **Total Orders:** Number of distinct `Order ID` values.
-   **Average Order Value:** Total Revenue divided by Total Orders.
-   **Total Units Sold:** Sum of `Quantity`.
-   **Top-Selling Category:** Category with the highest total revenue.
-   **Top Revenue-Generating Product:** Product with the highest total
    revenue.

## Sales Trend Analysis

Yearly revenue results:

  Year          Revenue   Orders    Units   YoY Revenue Growth
  ------ -------------- -------- -------- --------------------
  2014     \$484,247.50      969    7,581                  ---
  2015     \$470,532.51    1,038    7,979               -2.83%
  2016     \$609,205.60    1,315    9,837              +29.47%
  2017     \$733,215.26    1,687   12,476              +20.36%

The highest-revenue month was **November 2017**, with **\$118,447.83**
in revenue.

The lowest-revenue month was **February 2014**, with **\$4,519.89** in
revenue.

These results describe the observed historical trend; the dataset does
not establish the external causes of the changes.

## Category and Product Performance

-   **Technology** generated the highest category revenue.
-   Technology revenue: **\$836,154.03**
-   Highest-revenue product: **Canon imageCLASS 2200 Advanced Copier**
-   Revenue from that product: **\$61,599.82**
-   Highest-volume product: **Staples**
-   Staples units sold: **215**

Revenue leadership and unit-volume leadership are therefore treated as
separate analytical measures.

## Regional Performance

Revenue by region:

  Region           Revenue
  --------- --------------
  West        \$725,457.82
  East        \$678,781.24
  Central     \$501,239.89
  South       \$391,721.91

The **West** generated the highest revenue among the four regions.

## Customer Segment Analysis

Revenue by customer segment:

  Segment             Revenue
  ------------- -------------
  Consumer          \~\$1.16M
  Corporate       \~\$706.15K
  Home Office     \~\$429.65K

The Consumer segment contributed the largest share of observed revenue.

## Customer Insights

The analysis distinguishes customer frequency from customer monetary
contribution.

Key results include:

-   Total customers: **793**
-   Repeat customers: **781**
-   Repeat customer rate: **98.49%**
-   Repeat customers contributed approximately **99.78%** of observed
    revenue.
-   Highest-revenue customer: **Sean Miller**, approximately
    **\$25,043.05**
-   Most-frequent customer: **Emily Phan**, **17 distinct orders**

The highest-revenue customer and most-frequent customer are different,
showing why customer value and purchase frequency should be evaluated
separately.

## Evidence-Based Observations

1.  The dataset contains 5,009 unique orders generating \$2.30M in
    revenue from 37,873 units, with an average order value of \$458.61.
2.  Revenue declined 2.83% in 2015, then increased 29.47% in 2016 and
    20.36% in 2017.
3.  November 2017 recorded the highest monthly revenue at \$118,447.83.
4.  Technology was the highest-revenue category at \$836,154.03.
5.  Canon imageCLASS 2200 Advanced Copier led product revenue, while
    Staples led unit volume.
6.  The West was the highest-revenue region at \$725,457.82.
7.  781 of 793 customers were repeat customers and generated
    approximately 99.78% of observed revenue.
8.  Sean Miller generated the highest customer revenue, while Emily Phan
    placed the most distinct orders.

## Recommendations

-   Track revenue, distinct orders, units, and average order value
    together rather than interpreting business performance from one KPI
    alone.
-   Evaluate high-revenue and high-volume products separately.
-   Use regional and customer-segment results as inputs for deeper
    profitability and resource-allocation analysis.
-   Retain repeat-customer and customer-value measures in future
    reporting to distinguish purchasing frequency from monetary
    contribution.

## Limitations and Assumptions

-   The source dataset is at order-line level.
-   Distinct `Order ID` is used for all order-based metrics.
-   The provided `Sales` field is treated as revenue.
-   Repeat customers are customers with more than one distinct order in
    the supplied dataset.
-   Observed patterns are descriptive and should not be interpreted as
    causal relationships.
-   Findings apply only to the time period and records represented in
    the supplied Sample Superstore dataset.

## Repository Structure

``` text
Data_Science_Week1_Task2_Sales_Analysis/
├── Data/
│   └── Raw/
│       └── Sample - Superstore.csv
├── Notebooks/
│   └── Task2.ipynb
├── Outputs/
│   └── Charts/
│       ├── monthly-sales-trend.png
│       ├── revenue-by-category.png
│       ├── revenue-by-region.png
│       └── customer-segment-analysis.png
├── Reports/
│   └── Task2_Sales_Data_Analysis_Report.pdf
├── Screenshots/
│   ├── sales-kpi-summary.png
│   ├── monthly-sales-trend.png
│   ├── customer-insights.png
│   └── regional-category-analysis.png
├── README.md
└── requirements.txt
```

## How to Run the Project

1.  Clone or download this repository.
2.  Make sure Python is installed.
3.  Install the required dependency:

``` bash
pip install -r requirements.txt
```

4.  Open `Notebooks/Task2.ipynb` in Jupyter Notebook, JupyterLab, or VS
    Code.
5.  Run the notebook cells from top to bottom.
6.  The notebook reads `Sample - Superstore.csv` from `Data/Raw/` and
    reproduces the KPI, trend, product, regional, segment, and customer
    analysis.

## Main Deliverables

-   `Task2.ipynb` --- complete analytical notebook
-   `Task2_Sales_Data_Analysis_Report.pdf` --- structured Task 2 report
-   KPI summary table
-   Eight evidence-based observations
-   Trend-based interpretation
-   Dedicated customer insight section
-   Analytical charts and screenshots
-   `README.md`
-   `requirements.txt`

## Author

**Suman Paliwar**\
Data Science Internship --- Week 1
