# Car Sales Analysis Dashboard - Power BI Project

## Project Overview

My Project, a car sales, aims to enhance sales performance tracking and analysis through an efficient Car Sales Dashboard in Power BI.
This Power BI dashboard presents a detailed analysis of car sales data, enabling users to uncover key insights about sales performance across different dealers,dealer region, car company, models, engine,Transmission, car colour, Body Style and also Income of customer.The dashboard supports business stakeholders in identifying trends, improving forecasting, and enhancing overall sales strategy through visual storytelling and data-driven decision-making.
 
---

## 🎯 Purpose

- Track and monitor total car sales over time and dealer
- Analyze performance by brand, model, engine,Transmission, car colour, Body Style
- Visualize regional sales distribution using maps
- Identify top-selling car(Company) and Top dealer
- Enable interactive filtering for deeper insights
- Identify sales by gender,total cars sold a month, by colour, by transmission, by body type
- Identify top customer and no of cars bought
- Assist in planning and sales optimization

---

## 🛠️ Tools & Technologies

- **Power BI Desktop** – for building and publishing the dashboard
- **Microsoft Excel / CSV** – as the primary data source
- **DAX (Data Analysis Expressions)** – for calculated columns, measures, and KPIs
- **Power Query** – for data cleaning and transformation

---

## 📂 Dataset Description

The dataset used in this analysis includes the following fields:

- `Car_id`
- `Date`
- `Customer Name`
- `Gender`
- `Annual Income` 
- `Dealer Name`
- `Company(Car)`
- `Model` (e.g., BMW, Audi, Honda....etc)    
- `Engine`
- `Transmission` (e.g., Auto, Manual)
- `Color`
- `Price`
- `Dealer_no`
- `Body Style` (e.g., SUV, Sedan, Hatchback)
- `Phone`
- `Dealer Region`
- `Income Range` (Customer Income)      


---

## 📊 Dashboard Features

The dashboard includes the following pages and visuals:

- **Sales Overview**
  - Total Sales
  - Total cars sold
  - Average Car price
  - Average Customer Income
  - Total Sales by model
  - Total cars sold by month
  - Total sales by Company(Car)
    

 **Customer Insights**
  - Top Customer
  - Total sales by gender
  - Average of Annual Income by Income Range
 
- **Dealer and Regional Performance**
  - Top Dealer
  - Map Showing regional dealer sales breakdown
  - AveragevCar Price by dealer region
  - Total sales by dealer name
  
- **Car & Feature analysis**
  - Top 1 Car selling company
  - Total sales by company(Car)
  - Total cars sold by model
  - Total cars sold by Color
  - Total cars sold by Body Style
  - Count of company(Car)by transmission



---


**DAX**

## Sales Overview: ##
 

- **Total CarsSold:** 11K
    - **Formula:** `Total Car Sold = COUNT('car_data'[Car_id])`

- **Average CarPrice:** 27.91K
    - **Formula:** `Average Car Price = AVERAGE('car_data'[Price ($)])`

- **Average CustomerIncome:** 825.84K
    - **Formula:** `Average customer Income = AVERAGE(car_data[Annual Income])`


## Customer Insights: ##

  - **Top Customer:** Emma
    - **Formula:** `Top Customer = CALCULATE(
                        SELECTEDVALUE(car_data[Customer Name]),
                        TOPN(1,VALUES('car_data'[Customer Name]),[Total Sales]
                        )
                        )`


## Dealer & Regional Performance: ##

- **Top Dealer:** Rabun Used Car Sales
    - **Formula:** `Top Dealer = CALCULATE(
    SELECTEDVALUE('car_data'[Dealer_Name]),
    TOPN(1, 
        VALUES(car_data[Dealer_Name]), 
       [Total Sales]  
    )
)`

## Car&FeatureAnalysis: ##

- **Top Company(Car):** Chevrolet
    - **Formula:** `Top 1 Selling Company = CALCULATE(
    SELECTEDVALUE('car_data'[Company]),
    TOPN(
        1,
        VALUES(car_data[Company]),
        [Total Sales]
        
    )
  
)`



## 📷 Screenshots

### 1.Sales OverView

<img width="1312" height="736" alt="image" src="https://github.com/user-attachments/assets/aec886e7-95f2-4d03-8dbe-3d7218d5736f" />

### 2.Customer Insights

<img width="1313" height="740" alt="image" src="https://github.com/user-attachments/assets/b0aaacd1-f578-458c-9f37-687dc2d3e32c" />

### 3.Dealer & Regional Performance

<img width="1315" height="737" alt="image" src="https://github.com/user-attachments/assets/8aad72b3-c132-4cd8-9814-10f34264e9f1" />

### 4.Car & Feature Analysis

<img width="1308" height="732" alt="image" src="https://github.com/user-attachments/assets/12ae50fc-25ad-44d5-91b6-22e39408da25" />


---

## 👤 Author

- **Name:** Sahana G M
- **LinkedIn:** [Insert your LinkedIn Profile URL]
- **Email:** Sahanagm682@gmail.com

---
