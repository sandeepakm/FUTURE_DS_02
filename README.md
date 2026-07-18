# FUTURE_DS_02
# 📊 Customer Churn Analysis Dashboard

## Project Overview
This Power BI dashboard analyzes customer churn patterns and helps identify factors that influence customer retention. The dashboard provides insights into customer demographics, contract types, internet services, payment methods, tenure, and monthly charges to support data-driven decision-making.

## Objectives
- Analyze customer churn behavior.
- Identify factors contributing to customer attrition.
- Monitor churn rate and retention rate.
- Compare churn across customer segments.
- Support customer retention strategies.

## Dashboard Features

### KPI Cards
- Total Customers
- Churn Customers
- Retention Customers
- Churn Rate (%)
- Average Monthly Charges
- Average Tenure

### Visualizations
- Churn by Gender
- Churn by Contract Type
- Churn by Internet Service
- Monthly Charges vs Churn
- Customer Tenure vs Churn
- Churn Customers by Senior Citizen
- Payment Method vs Churn

### Interactive Filters
- Gender
- Contract Type
- Internet Service
- Payment Method
- Churn Status

## Dataset
This project uses the **Telco Customer Churn Dataset**.

### Key Columns
- CustomerID
- Gender
- SeniorCitizen
- Tenure
- Contract
- InternetService
- PaymentMethod
- MonthlyCharges
- Churn

## Tools Used
- Power BI Desktop
- Power Query
- DAX
- Telco Customer Churn Dataset

## DAX Measures

```DAX
Total Customers = COUNT(Customer[CustomerID])

Churn Customers =
CALCULATE(
    COUNT(Customer[CustomerID]),
    Customer[Churn] = "Yes"
)

Retention Customers =
CALCULATE(
    COUNT(Customer[CustomerID]),
    Customer[Churn] = "No"
)

Churn Rate =
DIVIDE([Churn Customers], [Total Customers], 0) * 100

Average Monthly Charge =
AVERAGE(Customer[MonthlyCharges])

Average Tenure =
AVERAGE(Customer[tenure])
```

## Key Insights
- Analyze customer churn across different demographics.
- Identify high-risk customer groups.
- Understand the impact of contract type on churn.
- Evaluate how internet services affect customer retention.
- Compare payment methods and their relationship with churn.
- Track monthly charges and tenure patterns among churned customers.

## How to Use
1. Open the Power BI (.pbix) file.
2. Refresh the dataset if required.
3. Use the slicers to filter data.
4. Analyze KPIs and visualizations.
5. Generate insights for customer retention strategies.

## Dashboard Preview
Customer Churn Analysis Dashboard with KPI cards, churn analysis charts, and interactive slicers.

## Author
**Sandeep Ankamreddy**  
B.Tech (Data Science)
