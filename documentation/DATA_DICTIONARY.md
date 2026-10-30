# Data dictionary — Microsoft Financial Sample

**Source:** `data/Financial Sample.xlsx`, 700 rows. Each row is a financial sales observation, not a unique customer or invoice transaction.

**Categorical:** Segment, Country, Product, Discount Band, Month Name.

**Numeric:** Units Sold, Manufacturing Price, Sale Price, Gross Sales, Discounts, Sales, COGS, Profit, Month Number, Year.

**Date:** Date (monthly-stamped observations, September 2013 through December 2014).

**Definitions:**
- Sales = Gross Sales − Discounts
- Profit = Sales − COGS (source-defined, not accounting net income)
- Profit Margin % = Profit / Sales
- Discount Rate % = Discounts / Gross Sales
- COGS Ratio % = COGS / Sales

**Discount Band:** `None` is a legitimate band; do not treat it as a null. Source documentation previously noted 53 blank values; confirm how these were handled in the **actual PBIX Power Query** before claiming a final null count or replacement rule.

**Currency:** workbook does not explicitly specify a currency; `$` in the report is a display convention.

**Date limitation:** 2013 covers only Sep–Dec; 2014 covers Jan–Dec. Unadjusted full-year YoY rates are not directly comparable.

**Model:** `FactFinancials` fact table with `DimDate` date dimension; verify the active one-to-many relationship in Power BI Desktop.
