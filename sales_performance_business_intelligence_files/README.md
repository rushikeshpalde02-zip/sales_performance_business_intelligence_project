# Sales Performance and Business Intelligence Analysis

## End-to-End Data Analytics Project

A transaction-level sales analytics project focused on data quality, KPI reporting, exploratory data analysis (EDA), sales trends, customer and product performance, regional comparisons, and shipping operations.

**Project scope:** Data Analytics and Exploratory Data Analysis only.  
**Excluded:** Machine learning, predictive modeling, forecasting models, model training, and model evaluation.

## Objectives

- Assess and improve the quality of sales transaction data.
- Calculate core business KPIs, including total sales, orders, customers, products, and average order value.
- Analyze annual, monthly, and quarterly sales performance.
- Compare categories, sub-categories, products, customer segments, regions, and states.
- Explore customer purchasing behavior using descriptive RFM analysis.
- Examine transaction distributions, potential outliers, and shipping duration.
- Convert analysis results into practical business insights and recommendations.

## Analytical Workflow

1. Business understanding
2. Data loading and understanding
3. Data quality assessment
4. Data cleaning
5. Feature engineering
6. KPI analysis
7. Exploratory Data Analysis
8. Sales trend analysis
9. Product analysis
10. Customer analysis
11. Regional analysis
12. Shipping and operational analysis
13. Outlier and distribution analysis
14. Business insights and recommendations

## Tools and Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / IPython

## Dataset

**Required file:** `sales_forcasting.csv`

Place the CSV file in the project root directory, alongside your notebook or Python script.

Expected fields used by the analysis include:

- **Order and shipping:** `Order ID`, `Order Date`, `Ship Date`, `Ship Mode`
- **Sales and products:** `Sales`, `Product ID`, `Product Name`, `Category`, `Sub-Category`
- **Customers:** `Customer ID`, `Customer Name`, `Segment`
- **Geography:** `Region`, `State`, and optionally `Postal Code`

The code expects these column names in the dataset. If your CSV uses different names, update the code accordingly. Do not publish confidential or personally identifiable data.

## Setup and Execution

### 1. Clone or download this repository

If using Git:

```bash
git clone <your-repository-url>
cd sales_performance_business_intelligence
```

Alternatively, download the repository ZIP from GitHub and extract it.

### 2. Create a virtual environment (recommended)

Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

macOS / Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
python -m pip install -r requirements.txt
```

### 4. Add the dataset

Put `sales_forcasting.csv` in the project root directory.

### 5. Run the analysis

Open your notebook in Jupyter and run the cells in order, from data loading through final recommendations. If you use a Python script instead, run it with:

```bash
python analysis.py
```

Replace `analysis.py` with your actual script filename. The supplied analysis uses `display()`, which is available in Jupyter/IPython; for a standalone script, import `display` from `IPython.display` or replace those calls with `print()`.

## Analysis and Outputs

| Area | Analysis performed |
|---|---|
| Data quality | Column types, missing values, duplicate rows, date conversion |
| Business KPIs | Sales, orders, customers, products, average order value, average shipping days |
| Time trends | Annual sales and year-over-year growth, monthly trends, quarterly performance, year-month heatmap |
| Product performance | Category, sub-category, product revenue, revenue share, Pareto analysis |
| Customer analytics | Segment revenue, customer revenue, order frequency, descriptive RFM analysis |
| Geography | Region, state, and region-by-category sales |
| Operations | Shipping mode, shipping duration, shipping time by region |
| Statistical exploration | Sales distribution, boxplot-based outlier inspection, numeric correlation |

The notebook calculates summaries and visualizations from the supplied dataset. Actual findings and business recommendations should be reported only after running the analysis and validating the outputs.

## Business Questions

- Which years, months, and quarters generate the most sales?
- Which categories, sub-categories, and products contribute the most revenue?
- Which customer segments and customers contribute most to sales?
- Which regions and states perform best or need further investigation?
- How do shipping modes and shipping duration vary?
- Are sales transactions heavily skewed, and which records warrant business review?

## Business Recommendations Framework

Use the results to decide whether to:

- Investigate the drivers of high-growth and declining periods.
- Plan inventory, campaigns, and logistics around observed seasonal patterns.
- Review product availability and the performance of low-revenue products.
- Prioritize high-value and potentially at-risk customers using descriptive RFM measures.
- Investigate lower-performing regions using order volume, customer count, average order value, and product mix.
- Monitor shipping duration and investigate regional operational differences.

Recommendations should be tied to observed evidence rather than assumed in advance.

## Project Structure

```text
sales_performance_business_intelligence/
├── sales_forcasting.csv
├── analysis.ipynb
├── requirements.txt
├── README.md
└── images/
    └── .gitkeep
```

Rename `analysis.ipynb` in this example if your notebook has a different filename. Do not commit virtual environments, secrets, or unnecessary temporary files.

## Visuals

Save selected charts or dashboard screenshots in the `images/` directory. Once images have been added, embed them here using their relative paths, for example:

```markdown
![Annual Sales Trend](images/annual_sales_trend.png)
```

## Limitations and Data Notes

- Missing values should be treated according to business context; they should not be removed automatically.
- High-value transactions are potential outliers for investigation, not automatic deletion candidates.
- Correlation describes association and does not establish causation.
- RFM here is descriptive customer analysis; it does not use machine learning.
- The analysis assumes the dataset includes the fields listed above. Validate column names and data types before execution.
- Average order value is calculated as total sales divided by distinct orders when `Order ID` is available. Confirm that this definition matches the business reporting standard.

## Conclusion

This project demonstrates an end-to-end analytical workflow that turns raw sales transactions into business intelligence through data validation, KPI analysis, descriptive statistics, trend analysis, customer and product analysis, regional comparisons, and operational review.

**Tools used:** Python, Pandas, NumPy, Matplotlib, Seaborn  
**Project type:** Data Analytics / Exploratory Data Analysis  
**Machine learning:** Not included
