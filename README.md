# Analysis of U.S. Petroleum Production vs. Product Supplied (2020-Present)

## Project Overview

This project analyzes and compares weekly U.S. Crude Oil Production with Total U.S. Petroleum Product Supplied (a proxy for consumption/demand). Using data from the U.S. Energy Information Administration (EIA) since January 2020, the analysis explores the relationship between domestic supply and market demand, the impact of significant events like the COVID-19 pandemic on both series, and the structural balance of the U.S. oil market.

The goal is to demonstrate skills in multi-dataset data acquisition, cleaning, combination, comparative visualization, time series exploration, and interpreting findings in an industry context using Python, pandas, matplotlib, seaborn, and statsmodels.

## Data Sources

This analysis utilizes two key datasets from the EIA:

1.  **U.S. Weekly Product Supplied of Total Petroleum Products**
    * Source: EIA - Weekly Petroleum Status Report
    * File Used: `PET_CONS_WPSUP_K_W.xls`
2.  **Weekly U.S. Field Production of Crude Oil**
    * Source: EIA - Weekly Petroleum Status Report
    * File Used: `WCRFPUS2w.xls`

Both datasets cover weekly periods from January 1, 2020, onwards.

## Objectives

* Acquire and clean weekly U.S. Crude Oil Production data and combine it with cleaned Total Petroleum Product Supplied data.
* Visualize and compare the two time series on the same plot.
* Analyze the difference between Product Supplied and Production over time.
* Examine the impact of the COVID-19 pandemic on both production and product supplied, and their relationship.
* Explore the seasonality present in each series and their difference.
* Interpret the findings to understand the structural balance between domestic crude production and U.S. petroleum demand since 2020.
* (Optional: Mention time series decomposition on one/both series, residual analysis).

## Methodology

The analysis followed these key steps:

1.  **Data Acquisition:** Obtained weekly data for Total Product Supplied (`PET_CONS_WPSUP_K_W.xls`) and Weekly Crude Oil Production (`WCRFPUS2w.xls`) by downloading Excel files from the EIA website.
2.  **Data Loading and Cleaning:** Loaded data from the relevant sheets of both Excel files into separate pandas DataFrames. Performed cleaning steps including removing metadata rows, renaming columns (to 'Week' and descriptive names for values), converting data types (datetime for 'Week', numeric for values), and filtering both datasets to the period since 2020-01-01.
3.  **Data Combination:** Merged the cleaned Production and Product Supplied DataFrames into a single DataFrame based on the common 'Week' column to enable direct comparison.
4.  **Comparative Visualization:** Created line plots to visualize:
    * Weekly U.S. Crude Oil Production and Total Petroleum Product Supplied on the same chart to compare their levels, trends, and fluctuations.
    * The weekly difference between Total Product Supplied and Crude Oil Production to quantify the balance met by other supply sources (imports, stocks).
5.  **(Optional: Time Series Exploration):** Performed time series decomposition on the Total Product Supplied series to isolate its trend, seasonality, and residuals. Analyzed the residuals (e.g., using ACF plot, Ljung-Box test) to understand unmodeled patterns.
6.  **(Optional: Detailed Seasonality View):** Generated a Seasonal Subseries Plot for Total Product Supplied to examine the year-over-year behavior for each specific week of the year.
7.  **Interpretation:** Synthesized the findings from visualizations and data summaries to interpret the market dynamics, the impact of major events, and the relationship between production and demand within the U.S. oil market context since 2020.

## Key Findings

* **Structural Imbalance:** U.S. Total Petroleum Product Supplied consistently exceeds domestic Crude Oil Production, highlighting reliance on imports and inventory changes to meet demand.
* **Differential COVID-19 Impact:** The Spring 2020 pandemic shock caused a much sharper, immediate decline in Product Supplied (demand proxy) than in Crude Oil Production, drastically but temporarily narrowing the supply-demand gap.
* **Persistent Seasonality:** Strong annual seasonality (summer peaks, winter lows) remains a dominant feature in Product Supplied, influencing the weekly balance with less-seasonal crude production.
* **Recovery Dynamics:** Both production and supplied series showed recovery trends since mid-2020, with the supply-demand gap returning to a pattern closer to pre-2020 levels, though the exact trajectory varied.
* **(Optional: Residuals):** Analysis of residuals from decomposition indicated that irregular, non-random patterns remained after accounting for simple trend and seasonality, suggesting the complex nature of events like the 2020 shock requires more nuanced modeling.

## Tools and Technologies

* Python
* pandas (data manipulation, loading, combining)
* matplotlib (plotting)
* seaborn (enhanced visualizations)
* statsmodels (time series decomposition, residual analysis)
* Google Colab (development environment)
* Git and GitHub (version control and project hosting)

## How to Reproduce

1.  Clone this GitHub repository: `git clone [Link to your NEW GitHub repo]`
2.  Navigate to the project directory.
3.  Open the Colab notebook (`notebooks/your-notebook-name.ipynb`) in Google Colab.
4.  Ensure both data files (`PET_CONS_WPSUP_K_W.xls` and `WCRFPUS2w.xls`) are placed in the `data/` directory relative to the notebook's location.
5.  Run the cells sequentially to execute the data loading, cleaning, combination, analysis, and visualization steps.

## Future Work

Potential areas for further analysis include:

* Analyzing other components of the supply-demand balance (e.g., imports, exports, inventory levels) and incorporating them into the comparison.
* Calculating and analyzing the percentage difference between Product Supplied and Production.
* Performing time series decomposition on the difference series.
* Applying more advanced time series modeling techniques (e.g., ARIMA) to the data or the difference series.
* Investigating the impact of other specific historical events or policies.
* Analyzing regional (PADD) or state-level production and consumption data if available.

## Contact

[Emmanouil Amygdalas/mamigdalas]
