# Final Power BI QA checklist

- [ ] Refresh source workbook successfully after relocating the project.
- [ ] Verify Sales, Profit, COGS, Discounts, Units Sold totals against the source.
- [ ] Verify Gross Sales − Discounts = Sales; Sales − COGS = Profit.
- [ ] Check how source blank Discount Band values were handled; keep legitimate `None` category distinct.
- [ ] Confirm `DimDate` is marked as date table and relationship is active (one-to-many, single-direction).
- [ ] Review actual PBIX measures; update `dax/` files to match final formulas (draft files currently incomplete).
- [ ] Correct or clearly qualify YoY comparisons because 2013 has only Sep–Dec.
- [ ] Fix truncated Profit YoY KPI text and confirm margin percentage-point change.
- [ ] Verify map countries and tooltips; map coloring may not correctly match all countries.
- [ ] Confirm donut slices represent Sales by Discount Band, and center total is Sales.
- [ ] Test all five slicers and their interactions with visuals.
- [ ] Test sidebar buttons and Reset Filters bookmark; remove or disable nonfunctional navigation.
- [ ] Check all labels and layout at Fit to page and 100% zoom.
- [ ] Confirm screenshot reflects the final saved PBIX and update if needed.
- [ ] Check the README's stated functionality against actual Power BI Desktop behavior.
