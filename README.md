Budget vs Actual Dashboard (FY2025)

A Power BI dashboard comparing budget and actual spend across four departments and five cost lines for FY2025, with variance analysis by department, cost line and month.

The data is synthetic. It was generated for this project to show a realistic budget-vs-actual structure with deliberate variances to investigate. It does not reflect any real company.

Dashboard Overview
Metric	Value
Total Budget	£5.13M
Total Actual	£5.25M
Total Variance	£121K (overspend)
Total Variance %	2.4%

The dashboard includes:

KPI cards: total budget, total actual, total variance and variance %.
Budget vs actual by department: clustered bars comparing budget and actual for Operations, Sales, Marketing and IT.
Variance by department and cost line: a matrix of variance across Payroll, Marketing, Software_IT, Travel and Overheads, with department totals.
Monthly variance: a line chart showing how the overspend builds through the year.
Slicers: filter by department and month.
Key Findings
Overall overspend of 2.4%. Actual spend is £121K above budget across the year.
IT is the largest overspend at £66K. Most of this is payroll (£30K) and software (£35K). Software spend is over budget from April, and the gap widens through the second half of the year.
Marketing is £31K over budget. Most of it (£28K) is marketing spend. The largest overspends fall in October to December, with November the highest month.
Sales (£14K) and Operations (£10K) are smaller. Sales is mainly travel (£9K). Operations is mainly payroll (£6K) and overheads (£3K).
The overspend builds through the year. Monthly variance rises through the second half, dips in August and peaks in November.
Calculations

Calculated measures (one per cost line, shown for Payroll):

Payroll Budget   = SUM(FY2025[Payroll_Budget])
Payroll Actual   = SUM(FY2025[Payroll_Actual])
Payroll Variance = [Payroll Actual] - [Payroll Budget]
Payroll Var %    = DIVIDE([Payroll Variance], [Payroll Budget])

Totals across all cost lines:

Total Budget   = [Payroll Budget] + [Marketing Budget] + [Software_IT Budget] + [Travel Budget] + [Overheads Budget]
Total Actual   = [Payroll Actual] + [Marketing Actual] + [Software_IT Actual] + [Travel Actual] + [Overheads Actual]
Total Variance = [Total Actual] - [Total Budget]
Total Var %    = DIVIDE([Total Variance], [Total Budget])

Sign convention: a positive variance means actual spend is above budget (overspend). Variance % is calculated from total variance divided by total budget, rather than by adding the individual line percentages, because each line has a different budget base.

Data

Source: synthetic, generated for this project.

Period: January to December 2025 (FY2025), monthly.

Structure: one row per department per month (48 rows). Each cost line has a budget column and an actual column.

Departments: Sales, Operations, Marketing, IT.

Cost lines: Payroll, Marketing, Software_IT, Travel, Overheads.

Currency: GBP.

Files
budget_vs_actual_fy2025.csv: the source data.
budget_vs_actual_dashboard.pbix: the Power BI file with the data model, measures and visuals. Check this matches the file name in your repo.
screenshots/: images of the final dashboard. Remove this line if the folder doesn’t exist yet.
Limitations
The data is synthetic. Variances were planted for analysis, so the conclusions describe the dataset and not any real business.
Only cost lines are included. There is no revenue or balance sheet data.
Budgets are flat across months. A real budget would normally reflect seasonality and phasing.
The data is at department level. It does not show individual transactions, suppliers or cost centres below department.
Skills Demonstrated

Power BI, budget vs actual analysis, variance analysis, DAX measures, data modelling, dashboard design, and FP&A reporting.
