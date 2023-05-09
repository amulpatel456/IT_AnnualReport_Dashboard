# IT_AnnualReport_Dashboard

# Project Description:

The project involved the creation of a visually impactful dashboard using Power BI to represent an IT company's annual expenditure report. The data sources included multiple tables such as actuals, cost, budget, departments, regions, and forecast, which were connected using relationship management. KPIs and measures were created to personalize the reports, and the dashboard was designed to help the company make better decisions based on their future business.

# Project Report

### Introduction:
This report outlines the details of the data visualization project created using Power BI to represent an IT company's annual expenditure report. The report covers the data sources used, the measures and formulas created, and the visualizations developed.

### Data Sources:
The data sources for this project were various tables from an Excel file, including actuals, costs, budget, departments, regions, and forecasts. The tables were connected using the manage relationship feature in Power BI.

### Measures and Formulas:
Several measures were created to help with data analysis and visualization. These measures include:

Forecast RT: This measure calculates the sum of actuals for a specific date range filtered by the latest date. The formula for this measure is:
forecastRT = CALCULATE(SUM(Actuals[Actual]), FILTER(ALLSELECTED('Calendar'[Date]), ISONORAFTER('Calendar'[Date],MAX(Actuals[Date]),DESC)))

Actual RT: This measure calculates the sum of actuals for a specific date range filtered by the latest date. The formula for this measure is:
Actual RT = CALCULATE(SUM(Actuals[Actual]), FILTER(ALLSELECTED('Calendar'[Date]), ISONORAFTER('Calendar'[Date],MAX(Actuals[Date]),DESC)))

Budget RT: This measure calculates the sum of actuals for a specific date range filtered by the latest date. The formula for this measure is:
Budget RT = CALCULATE(SUM(Actuals[Actual]), FILTER(ALLSELECTED('Calendar'[Date]), ISONORAFTER('Calendar'[Date],MAX(Actuals[Date]),DESC)))

Budget V Forecast: This measure calculates the difference between the sum of the budget and forecast tables. The formula for this measure is:
Budget V Forecast = SUM('Budget'[Budget]) - SUM('Forecast'[Forecast])

Budget V Forecast %: This measure calculates the percentage difference between the sum of the budget and forecast tables. The formula for this measure is:
Budget V Forecast % = VAR __BASELINE_VALUE = SUM('Forecast'[Forecast])
VAR __VALUE_TO_COMPARE = SUM('Budget'[Budget])
RETURN
IF(
NOT ISBLANK(__VALUE_TO_COMPARE),
DIVIDE(__VALUE_TO_COMPARE - __BASELINE_VALUE, __BASELINE_VALUE)
)

### Visualization:
The dashboard includes various visualizations such as bar charts, line charts, tables, and KPIs. The visualizations help to display the data in an easy-to-understand format. The KPIs display the important metrics that drive business decisions.

### Conclusion:
In conclusion, the data visualization project using Power BI was successful in creating a visually impactful dashboard that represents an IT company's annual expenditure report. The measures and formulas used in the project help to analyze and display the data effectively. The dashboard will aid the company in making informed decisions based on future business.

