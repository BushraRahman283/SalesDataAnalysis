# SalesDataAnalysis

This Google Colab notebook performs an in-depth analysis of sales data collected over several months. The goal is to extract valuable insights to understand sales performance, identify trends, and inform business strategies.

## Data Sources

The analysis is based on sales data files stored in a Google Drive folder. The script concatenates these individual monthly files into a single comprehensive dataset.

## Analysis Performed

The notebook addresses several key questions about the sales data:

- **Best Month for Sales**: Determines which month had the highest sales revenue and the corresponding amount earned.
- **City with Highest Sales**: Identifies the city with the highest total sales revenue.
- **Optimal Advertisement Time**: Analyzes sales patterns throughout the day to recommend the best time to display advertisements for maximizing customer purchases.
- **Products Most Often Sold Together**: Identifies pairs of products that are frequently purchased in the same order.
- **Product Performance by Revenue**: Determines which individual products generate the highest total sales revenue.
- **Average Price per Product**: Calculates the average price for each product listed in the sales data.

## Methodology

The analysis involves the following steps:

- Mounting Google Drive to access the sales data files.
- Reading and concatenating multiple monthly sales data files into a single pandas DataFrame.
- Data cleaning, including handling missing values and converting data types.
- Feature engineering, such as extracting the month, hour, and city from existing columns.
- Aggregating data by month, city, product, and hour to calculate total sales and counts.
- Utilizing `itertools.combinations` and `collections.Counter` to find frequently co-purchased product pairs.
- Visualizing the results using `matplotlib` to provide clear insights into sales trends and performance.

## Tableau Visualization

To enhance the presentation of the insights obtained through Python, the cleaned dataset was exported in JSON format and imported into Tableau. An interactive dashboard was developed to visually explore the data and support deeper analysis. The dashboard highlights key findings from the sales dataset, including:

- Monthly sales performance
- City-wise revenue distribution
- Top-performing products by revenue
- Hourly sales trends

This visualization provides an accessible and interactive way to interpret the dataset and can support both business and analytical decision-making.

The Tableau dashboard can be accessed at the following link:  
**[Sales Data Analysis – Tableau Public](https://public.tableau.com/app/profile/bushra.rahman3743/viz/SalesDataAnalysis_17524368384940/Dashboard1?publish=yes)**

## Key Libraries Used

- `pandas`: For data manipulation and analysis.
- `os`: For interacting with the operating system, specifically to list files in a directory.
- `matplotlib.pyplot`: For creating visualizations (bar plots and line plots).
- `itertools`: For creating combinations of products sold together.
- `collections.Counter`: For counting occurrences of product combinations.
- `google.colab`: For authentication and accessing Google Drive and other Colab features.
- `gspread` and `google.auth`: (Used in other examples, not directly in the sales analysis, but relevant for Google services interaction).

## How to Use

1. Open the notebook in Google Colab.
2. Ensure your Google Drive is mounted and the sales data files (e.g., `Sales_April_2019.csv`, etc.) are located in the specified directory path (`/content/drive/MyDrive/Sales_data/Sales_Data/`).
3. Run all the cells sequentially.
4. The output and visualizations will be displayed within the notebook, showing the results of the sales analysis.

## Further Analysis Ideas

Based on the insights gained, potential future analyses could include:

- Analyzing sales trends over longer periods (e.g., yearly).
- Investigating the impact of specific events or promotions (if data is available).
- Predicting future sales based on historical data.
- Performing more detailed customer segmentation (if customer IDs were available).
