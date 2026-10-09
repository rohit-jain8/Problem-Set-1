# Problem Set 1: The Cost of Living Brief

**ECON 3916 – Data Fluency**

## Project Overview

This project looks at how changes in the cost of living can affect individual households differently from what the national Consumer Price Index (CPI) suggests. I created a hypothetical single-parent household living in the Boston area and built a household price index using six spending categories: rent, groceries, used cars, gasoline, utilities, and healthcare.

The goal was to compare this household's estimated inflation between 2019 and 2024 with official CPI data and understand how spending patterns can influence the inflation a household experiences.

## What I Did

- **Phase 1 – Household Price Index:** Created a household spending basket and calculated both an unweighted average price change and a weighted Laspeyres price index.
- **Phase 2 – FRED Data Comparison:** Retrieved four official CPI series from the Federal Reserve Economic Data (FRED) database, rebased them to 2019 = 100, and compared them with my household index.
- **Phase 3 – Data Analysis:** Checked the CPI series for missing observations, compared their historical coverage, and examined the differences between seasonally adjusted and unadjusted data.
- **Phase 4 – Sensitivity Analysis:** Used AI-generated Python code to test how changing individual spending weights affected the household price index. I then verified the calculations and summarized the findings.

## Key Findings

My household price index increased by **28.49% between 2019 and 2024**, compared to a **22.70% increase in overall CPI**. This difference of 5.79 percentage points suggests that the national CPI may understate the price increases experienced by this particular household.

The weighted household index also showed a higher price increase than the unweighted average of 26.71%, demonstrating why spending weights matter when measuring inflation.

My sensitivity analysis found that Healthcare had the greatest impact when its spending weight was adjusted between 0% and 50%, changing the index by 4.72 points. Rent was the second-most sensitive category, with a 4.04-point change.

Overall, the results show why inflation should be considered alongside a household's actual spending patterns rather than relying entirely on national averages.

## Data Sources and Tools

**Data Source:** Federal Reserve Economic Data (FRED)

The four CPI series used were:

- `CPIAUCSL` – Overall Consumer Price Index
- `CUSR0000SEHA` – Rent of Primary Residence
- `CUSR0000SAF11` – Food at Home
- `CUSR0000SETA02` – Used Cars and Trucks

**Tools:** Python, Google Colab, pandas, NumPy, and Matplotlib.

## Limitations

The household basket uses estimated prices and spending weights, so the findings are intended to illustrate how inflation can vary across households rather than represent the experience of every worker. The analysis also compares estimated household prices with annual average CPI data, which are not perfectly identical measures.

## AI Use and Verification

I used ChatGPT to help generate the sensitivity analysis in Phase 4 and reviewed the code before using its results. I verified that the original spending weights added up to 1.0, that the household index matched my earlier calculation of 128.49, and that the adjusted weights continued to total 1.0 when individual category weights were changed.

## Project File

The complete analysis, Python code, charts, and written explanations are available in:

`Econ_3916_PS1.ipynb`

The notebook can be opened and run in Google Colab.
