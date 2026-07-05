# AI-Powered-Sales-Data-Analysis-Project
# AI-Powered Sales Data Analysis Using Python, SQL and GenAI

## Project Overview

This project is a complete sales data analytics portfolio project built with Python, SQL, data visualization, and GenAI-style business insight prompts. It takes a raw sales CSV file, cleans the data, performs exploratory data analysis, creates professional charts, stores the cleaned data in a SQLite database, runs SQL analysis queries, and generates business-ready summary files.

The project is designed to be beginner-friendly, easy to explain, and ready for GitHub or LinkedIn portfolio sharing.

## Business Problem

Sales teams often collect large amounts of order data, but the data is not always clean, structured, or ready for decision-making. The goal of this project is to transform raw sales data into useful business insights that can help answer questions such as:

- Which product categories generate the most revenue?
- Which cities and regions perform best?
- Which customers contribute the most sales?
- Which payment modes and sales channels are most used?
- What monthly sales trends can leadership monitor?

## Dataset Description

The project expects a CSV file named:

```text
ai_powered_sales_dataset.csv
```

Place the file inside:

```text
data/raw/
```

Expected columns:

- Order_ID
- Order_Date
- Customer_Name
- Customer_Segment
- City
- State
- Region
- Product_Category
- Product_Name
- Quantity
- Unit_Price
- Discount_Percent
- Sales
- Profit
- Shipping_Cost
- Payment_Mode
- Sales_Channel
- Order_Status
- Customer_Rating

If any required column is missing, the project shows a clear error message in the terminal.

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SQLite
- SQL
- GenAI prompts
- Markdown
- Git and GitHub
- VS Code

## Project Workflow

1. Load raw sales CSV data
2. Validate required columns
3. Check missing values and duplicate rows
4. Clean the dataset
5. Create new date and profit columns
6. Save the cleaned dataset
7. Perform exploratory data analysis
8. Generate visualizations
9. Store cleaned data in SQLite
10. Run SQL analysis queries
11. Generate business summary and GenAI prompts

## Folder Structure

```text
ai-powered-sales-analysis-genai/
|
├── data/
│   ├── raw/
│   │   └── ai_powered_sales_dataset.csv
│   └── processed/
│       └── cleaned_sales_data.csv
|
├── charts/
│   ├── revenue_by_category.png
│   ├── profit_by_category.png
│   ├── monthly_sales_trend.png
│   ├── top_10_customers.png
│   ├── top_10_cities.png
│   ├── region_wise_sales.png
│   ├── payment_mode_distribution.png
│   ├── sales_channel_performance.png
│   ├── customer_rating_distribution.png
│   └── category_region_heatmap.png
|
├── database/
│   └── sales_analysis.db
|
├── outputs/
│   ├── business_summary.txt
│   ├── genai_business_prompt.txt
│   ├── linkedin_post_prompt.txt
│   └── sql_query_results.txt
|
├── src/
│   ├── main.py
│   ├── data_cleaning.py
│   ├── eda_analysis.py
│   ├── visualizations.py
│   ├── sql_analysis.py
│   └── genai_prompts.py
|
├── README.md
├── requirements.txt
├── .gitignore
└── run_instructions.md
```

## Key Business Questions

- What is the total revenue, profit, and net profit?
- How many orders were placed?
- What is the average order value?
- Which product category generated the highest revenue?
- Which city and region performed best?
- Who are the top 10 customers?
- Which month had the highest sales?
- Which payment mode was used most often?
- Which sales channel generated the most revenue?
- What is the distribution of customer ratings?

## Data Cleaning Steps

The cleaning process is handled in `src/data_cleaning.py`.

Steps performed:

- Load the CSV from `data/raw/ai_powered_sales_dataset.csv`
- Validate all required columns
- Check missing values
- Check duplicate rows
- Remove duplicate rows
- Convert numeric fields to numeric data types
- Fill missing `Shipping_Cost` values with the median
- Fill missing `Customer_Rating` values with the mean
- Convert `Order_Date` to datetime
- Create `Year`, `Month`, `Month_Name`, and `Day_Name` columns
- Create `Net_Profit = Profit - Shipping_Cost`
- Save cleaned data to `data/processed/cleaned_sales_data.csv`

## Exploratory Data Analysis

The EDA process is handled in `src/eda_analysis.py`.

It calculates:

- Total revenue
- Total profit
- Total net profit
- Total orders
- Total quantity sold
- Average order value
- Revenue by product category
- Profit by product category
- City-wise revenue
- Top 10 customers
- Monthly sales trend
- Region-wise revenue
- Payment mode count
- Sales channel performance
- Order status count

## SQL Analysis

The SQL workflow is handled in `src/sql_analysis.py`.

The cleaned data is stored in SQLite as:

```text
database/sales_analysis.db
```

Table name:

```text
sales_data
```

SQL query results are saved to:

```text
outputs/sql_query_results.txt
```

Queries included:

- Category-wise total sales
- City-wise total sales
- Region-wise total sales
- Payment mode order count
- Sales channel revenue
- Top 10 customers
- Monthly revenue
- Order status count

## Visualizations

Charts are created with Matplotlib and Seaborn and saved inside the `charts/` folder.

Generated charts:

- Revenue by Product Category
- Profit by Product Category
- Monthly Sales Trend
- Top 10 Customers
- Top 10 Cities by Revenue
- Region-wise Sales Performance
- Payment Mode Distribution
- Sales Channel Performance
- Customer Rating Distribution
- Product Category vs Region Heatmap

## GenAI Integration

This project includes GenAI-style prompt files that can be used with tools like ChatGPT, Gemini, or Claude.

Generated files:

- `outputs/business_summary.txt`
- `outputs/genai_business_prompt.txt`
- `outputs/linkedin_post_prompt.txt`

The GenAI business prompt asks an AI assistant to generate:

- 5 business insights
- 5 recommendations
- Executive summary
- 3 business risks to monitor

The LinkedIn post prompt helps create a professional project post for sharing this portfolio work.

## Key Insights

After running the project, the generated business summary includes:

- Total revenue
- Total profit
- Total net profit
- Total orders
- Total quantity sold
- Average order value
- Best product category
- Best city
- Best region
- Best sales month
- Most used payment mode
- Best sales channel

Open `outputs/business_summary.txt` after running the project to review the final insights from your dataset.

## Business Recommendations

Recommendations can be generated from the file:

```text
outputs/genai_business_prompt.txt
```

Use the prompt in ChatGPT, Gemini, or Claude to produce professional business recommendations based on the project results.

Typical recommendation areas include:

- Improving revenue from high-performing categories
- Strengthening sales in top regions
- Supporting profitable sales channels
- Reducing shipping costs
- Monitoring order status issues
- Improving customer experience based on rating patterns

## How to Run This Project

Open the project folder in VS Code:

```text
ai-powered-sales-analysis-genai
```

Create and activate a virtual environment.

Mac/Linux:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Windows:

```bash
python -m venv .venv
.venv\Scripts\activate
```

Install requirements:

```bash
pip install -r requirements.txt
```

Place the CSV file here:

```text
data/raw/ai_powered_sales_dataset.csv
```

Run the project:

```bash
python src/main.py
```

## Screenshots/Charts

After the project runs successfully, all chart images are available in the `charts/` folder. These charts can be added to GitHub, LinkedIn posts, resumes, or presentations.

Recommended charts to highlight:

- `charts/revenue_by_category.png`
- `charts/monthly_sales_trend.png`
- `charts/top_10_customers.png`
- `charts/category_region_heatmap.png`

## LinkedIn Post Template

Use this template after generating your results:

```text
I completed a data analytics portfolio project: AI-Powered Sales Data Analysis Using Python, SQL and GenAI.

In this project, I cleaned and analyzed sales data using Python, performed EDA with Pandas, created visualizations using Matplotlib and Seaborn, stored the cleaned data in SQLite, ran SQL queries, and generated GenAI prompts for business insights.

Key areas covered:
- Data cleaning
- Exploratory data analysis
- SQL analysis
- Business KPI reporting
- Data visualization
- GenAI-assisted business storytelling

This project helped me practice end-to-end analytics workflow skills and convert raw data into business insights.

#DataAnalytics #Python #SQL #Pandas #DataVisualization #GenAI #PortfolioProject
```

For a customized post based on your actual results, use:

```text
outputs/linkedin_post_prompt.txt
```

## Future Improvements

- Add an interactive dashboard using Streamlit or Power BI
- Add automated data quality checks
- Add unit tests for cleaning and EDA functions
- Add forecasting for future monthly sales
- Add customer segmentation analysis
- Add product-level profitability analysis
- Connect the project to a cloud database

## Author Section

Created by: SK SAHIL 

LinkedIn: https://www.linkedin.com/in/sahil-ahammad-7a158b2b5/

GitHub:https://github.com/SK-SAHIL786
