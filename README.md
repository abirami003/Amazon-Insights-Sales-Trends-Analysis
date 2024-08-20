# Amazon-Insights-Sales-Trends-Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaning/preparation)
- [Data Analysis](#data-analysis)
- [Results/Findings](#results/findings)
- [Recommendations](#recommendations)

### Project Overview

This project involves a comprehensive analysis of Amazon sales data, focusing on key metrics such as order status, shipment details, product categories, and customer demographics. The goal is to uncover insights that can drive strategic decisions for optimizing logistics, enhancing customer satisfaction, and increasing overall sales performance.

### Data Sources

Amazon Sales Data: The primary dataset used for this analysis is the "Amazon Sale Report.csv" file, containing detailed information about order,sales and shipment details.

### Tools

- Excel - Database Manageemnt
    - [Download Here](https://microsoft.com)
- Power Query Editor - Data Cleaning and Analysis
- Power BI Desktop - Creating Reports
    - [Download Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

### Data Cleaning/Preparation

In the initial data preparation, I performed the following tasks
1. Data Loading and Inspection
2. Handling missing values
3. Data cleaning and formatting

### Data Analysis

Some interesting code/feature worked with:

To set a Target Goal, I used this DAX function
```dax
QTR1 = CALCULATE(SUM('Amazon Sale Report'[AMOUNT]),DATESBETWEEN('Amazon Sale Report'[DATE],DATE(2022,03,31),DATE(2022,05,14)))
```
```dax
QTR2 = CALCULATE(SUM('Amazon Sale Report'[AMOUNT]),DATESBETWEEN('Amazon Sale Report'[DATE],DATE(2022,05,15),DATE(2022,06,29)))
```
```dax
TARGET VALUE = CALCULATE([QTR1]*1.1)
```
for Cancellation Rate
```dax
ORDER CANCELLATION RATE = SUM('Amazon Sale Report'[CANCELLATION RATE])/ COUNT('Amazon Sale Report'[ORDER ID])
```
for Fulfilment Rate
```dax
ORDER FULFILMENT RATE = SUM('Amazon Sale Report'[FULFILLMENT RATE])/COUNT('Amazon Sale Report'[ORDER ID])
```
```dax
AVG ORDER = SUM('Amazon Sale Report'[AMOUNT])/COUNT('Amazon Sale Report'[ORDER ID])
```

### Results/Findings

The analysis results are summarized as follows:
- Maharashtra is a leading state in turnover
- The T-shirt is a top-selling product
- Customers favour expedited shipping over standard shipping
- The turnover for the second quarter is 19.5% lower than that of the first quarter
- May 03 had the highest volume of orders placed

 ### Recommendations

- Watch is the lowest -selling item. To boost sales ,offer a "Watch Deal" promotion with 15% off
- Shoes and Socks are the lowest-selling items. To boost sales, offer a "Buy 3 Sets of Socks, Get 1 Set Off" promotion and introduce a "Back to School" promotion for shoes from May 10 to May 30 with 20% discount to drive purchases during this key period
- Cancellation rates are highest in Maharashtra, followed by Karnataka, Uttar Pradesh, Telangana, and Tamil Nadu. Addressing specific issues in these states will help reduce cancellations
- Orders dropped from 880 to 410 between June 15 and June 29, and there was a similar decline from May 10 to May 26. Need to investigate the causes of these declines and implement corrective measures
- To boost sales in the lowest-performing areas, Pondicherry and Lakshadweep, deploy localized marketing strategies and targeted promotions, and streamline logistics for faster delivery and improved customer satisfaction
- Also give, 
  - "Wallet Wednesday": Run a weekly promotion offering gift voucher off all wallets on Wednesdays. This creates a regular buying habit and boosts mid-week sales
  - "Scent of the Season": Offer a 10% discount on perfumes and include a free sample of a new fragrance, encouraging customers to try new scents while buying their favorites.
  - Offer a 25% discount on Blazers during special periods such as the Diwali festive season or the end-of-winter sale. This attracts customers looking for high-value purchases at a lower price point, especially during these key shopping times.
  - Shirt & T-Shirt Deal: Offer 30% off when customers buy 4 shirts or 4 T-shirts, encouraging bulk purchases and boosting overall sales.

👕 | 👞 | 🩰 | 🧦 | ⌚ 

💻 | 🖱️

😃

#data  #analysis  #happy
