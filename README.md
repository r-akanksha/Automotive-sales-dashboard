# Car Sales Dashboard - Power BI Project

## About Company
Our company, a car dealership, aims to enhance sales performance tracking and analysis through an efficient Car Sales Dashboard in Power BI.

## Objective
Design and develop a dynamic, interactive Car Sales Dashboard to visualize critical KPIs, enabling data-driven decision-making and understanding sales performance trends over time.

## Problem Statement 1: KPI’s Requirement
### Sales Overview:
- Year-to-Date (YTD) Total Sales
- Month-to-Date (MTD) Total Sales
- Year-over-Year (YOY) Growth in Total Sales
- Difference between YTD Sales and Previous Year-to-Date (PTYD) Sales

### Average Price Analysis:
- YTD Average Price
- MTD Average Price
- YOY Growth in Average Price
- Difference between YTD Average Price and PTYD Average Price

### Cars Sold Metrics:
- YTD Cars Sold
- MTD Cars Sold
- YOY Growth in Cars Sold
- Difference between YTD Cars Sold and PTYD Cars Sold


## Data Available
### Car Data:
- Car ID
- Date
- Customer Name
- Gender
- Annual Income
- Dealer Name
- Company
- Model
- Engine
- Transmission
- Color
- Price ($)
- Dealer No
- Body Style
- Phone
- Dealer Region

### Calendar Table (Created):
- Date
- Month
- Week
- Year

**Problem Statement 1: KPI’s**

**Sales Overview:**
- **YTD Total Sales:** $371.2M
    - **Formula:** `SUM('Car Data'[Total Sales])`
- **MTD Total Sales:** $54.28M
    - **Formula:** `CALCULATE(SUM('Car Data'[Total Sales]), DATESMTD('Calendar Table'[Date]))`
- **YOY Growth in Total Sales:** 23.6%
    - **Formula:** `[Sales Difference]/[PTYD Total Sales]`
- **Difference between YTD Sales and PTYD Sales:** $70.8M
    - **Formula:** `[YTD Car Sales]-[PTYD Car Sales]`

**Average Price Analysis:**
- **YTD Average Price:** $28.0k
    - **Formula:** `TOTALYTD([Avg Price],'Calendar Table'[Date])`
- **MTD Average Price:** $28.26k
    - **Formula:** `TOTALMTD([Avg Price],'Calendar Table'[Date])`
- **YOY Growth in Average Price:** -0.79%
    - **Formula:** `[Avg Price Diff]/[PTYD Avg Price]`
- **Difference between YTD Average Price and PTYD Average Price:** $0.22k loss
    - **Formula:** `[YTD Avg Price]-[PTYD Avg Price]`

**Cars Sold Metrics:**
- **YTD Cars Sold:** 13.3K
    - **Formula:** `SUM('Car Data'[YTD Car Solds])`
- **MTD Cars Sold:** 1.92k
    - **Formula:** `CALCULATE(SUM('Car Data'[MTD Cars Sold]), DATESMTD('Calendar Table'[Date]))`
- **YOY Growth in

 Cars Sold:** 19.73%
    - **Formula:** `car_data[Cars Sold Diff]/[YTD Car Solds]`
- **Difference between YTD Cars Sold and PTYD Cars Sold:** 3K
    - **Formula:** `[YTD Car Solds]-[PTYD Car Solds]`
 
