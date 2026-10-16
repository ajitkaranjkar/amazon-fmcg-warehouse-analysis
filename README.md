# FMCG Warehouse Analysis — Optimizing Distribution Efficiency

An Excel project where I analyzed operations data from 25,000 Amazon FMCG warehouses to find what was hurting efficiency — stockouts, delivery delays, rising costs — and what to do about it.

## The data

Warehouse-level records: location type, capacity size, zone, refill requests, transport issues, competitors nearby, retail shops served, electric supply, distance from the hub, headcount, establishment year, storage issues, breakdowns, government checks, and product weight.

Messy in the way real data is. Almost half the establishment-year values were missing, headcount had blanks and outliers. Cleaning that up properly was half the project.

## What I did

- Filled 11,881 missing establishment years with the median (2009) — median, not mean, so a few odd years would not skew it
- Capped headcount outliers using the IQR method instead of deleting rows
- Checked for duplicates and inconsistent category labels (none found, which was a nice surprise)
- Answered 20 analysis questions with aggregation tables and charts — capacity mix, refill demand by zone, staffing benchmarks, transport patterns, storage-issue drivers
- Ran correlations: worker count vs storage issues, distance vs transport issues, warehouse age vs breakdowns
- Built a KPI dashboard (total warehouses, refill rate, transport issues, storage-issue %, electric supply %, shops served)
- Wrote up 8 findings with 8 matching recommendations for management

## A few things I found

- 91.8% of warehouses are rural, and most are Large capacity — the network is built for bulk, not proximity
- The North zone alone generated 41,814 refill requests in 3 months (40.9% of all refills) — that is where stockout risk lives
- Headcount has basically zero correlation with storage issues (-0.009). Throwing more people at it is not the fix
- Distance from the hub barely correlates with transport issues (0.014) — the problem is not how far, it is how the routes are run
- Warehouses from the 90s average 4.03 breakdowns per quarter vs 1.34 for ones built in the 2020s. Maintenance budgets should follow age, not size
- The weird one: A+ certified warehouses report the *most* storage issues (19.9 avg vs 15.9 for C). Either the bar needs a look, or better-run warehouses just report more honestly

## Workbook

`Amazon_FMCG_Warehouse_Analysis_AjitKaranjkar.xlsx` — 8 sheets: README, raw data, cleaned data, cleaning log, basic analysis, medium analysis, dashboard, management summary.

## Tools

Microsoft Excel — formulas, aggregation tables, charts, scatter plots with trendlines.
