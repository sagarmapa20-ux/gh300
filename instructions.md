Demo prompts
Prompt 1: Create the notebook
Create a Jupyter notebook named sales_visualization_demo.ipynb. Generate 2,000 rows of reproducible synthetic retail sales data for 2025 and 2026. Include order date, region, product, channel, units sold, unit price, discount percentage, revenue, cost, profit, and customer satisfaction. Make the data realistic by including seasonality, product price differences, regional demand patterns, and reasonable random variation. Add markdown cells explaining each stage.

Prompt 2: Validate and explore
Validate the generated dataset. Show its shape, data types, missing values, duplicate count, and numeric summary. Confirm that revenue and profit are calculated correctly. Then identify three patterns worth investigating, but do not invent conclusions that are not supported by calculations.

Prompt 3: Create core visualizations
Create these visualizations with clear titles, labels, legends, and an accessible color palette:

Monthly revenue trend.
Profit by region.
Product revenue by region as a heatmap.
Discount percentage versus profit as a scatter plot. Add one selective annotation to each chart and write two concise observations below each chart.
Prompt 4: Improve storytelling
Review all charts for storytelling quality. Remove unnecessary visual clutter, format currency and percentages, make category ordering meaningful, and highlight the most important comparison or anomaly. Keep the underlying data unchanged.

Prompt 5: Add an executive summary
Add a final markdown section titled Executive Summary. Summarize the strongest findings in five bullets, distinguish observations from recommendations, and state clearly that the dataset is synthetic.

Useful follow-up prompts
Add 1,000 new rows while preserving the same schema and business relationships.
Create a reusable function for each visualization and test it with the current dataframe.
Detect outliers in profit using the IQR method and compare results with and without outliers.
Add a correlation heatmap for numeric columns and explain correlation does not imply causation.
Export the synthetic dataset to data/synthetic_sales.csv and the charts to outputs/.
Optimize the notebook so all transformations are vectorized and cells run in order.
Repository instructions
This repository contains Python and Jupyter notebook demonstrations for synthetic business-data analysis and visualization.

Use Python 3.11-compatible code.
Prefer pandas and NumPy for data manipulation, matplotlib and seaborn for visualization.
Set a fixed random seed whenever generating synthetic data.
Make synthetic datasets realistic by defining relationships between measures. Do not create every column independently.
Clearly label all sample data as synthetic.
Keep notebooks runnable from top to bottom without hidden state.
Organize notebooks into markdown sections: Business question, Setup, Data generation or loading, Validation, Exploration, Visualization, Insights, and Next steps.
Validate shape, types, missing values, duplicates, ranges, and derived calculations before analysis.
Use vectorized operations rather than row-by-row loops.
Use accessible color palettes, descriptive titles, axis labels, legends, and appropriate number formatting.
Avoid 3D charts and avoid pie charts with more than five categories.
Add annotations only when they strengthen the chart's main message.
Separate observations from recommendations and support every observation with a displayed calculation or chart.
Do not overwrite source data. Write generated files under data/ and chart outputs under outputs/.
When modifying a notebook, preserve its narrative flow and explain material changes in markdown cells.
