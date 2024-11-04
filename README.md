# CAPSTONE-PROJECT-DOCUMENTATION 1

----

## PROJECT TITLE: CAPSTONE SALES DATA

----

[PROJECT OVERVIEW](#project-overview)

[DATA SOURCES](#data-sources)

[TOOLS USED](#tools-used)

[DATA CLEANING AND PREPARATIONS](#data-cleaning-and-preparations)

[EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)

[DATA ANALYSIS](#data-analysis)

[DATA SUMMARIZATION](#data-summarization)

[DATA VISUALIZATION](#data-visualization)

[INFERENCES](#inferences)

[CONCLUSION](#conclusion)

----

### PROJECT OVERVIEW
This project aims at analyzing the sales performance of a retail store. 
Key insights such as top-selling products, performance, and monthly sales trends  regional are to be uncovered at the end of the project. The goal is to produce an interactive Power BI 
dashboard that highlights these findings.

----

### DATA SOURCES
The primary source of data used in the projects are data.sales.cv and this is an open source data that can be freely downloaded from open source online such as kaggle or FRED or any other data respository site.

----

### TOOLS USED
- Microsoft Excel [Download Here](https://www.microsoft.com) 
   1. For Data cleaning
   2. For Data Analysis
   3. For Data visualization

- SQL - Structured Query Language for Quering of Data
  
- Power Bi
  
   1.business analysis
  
   2.visualization
  
   3.creating intereative dashbord.
  
- GitHub for Portfolio Building
      
----

### DATA CLEANING AND PREPARATIONS
In the initial phase of the data cleaning and preparation, the following actions was performed;
   1. Data loading and inspection
   2. Handling missing variables
   3. Data cleaning and formatting
   4. Removing duplicate

----

### EXPLORATORY DATA ANALYSIS
This analysis is meant to answer the followimg questions:
   - The Total Sales Performance
   - Total sales generated in each region
   - The highest selling products
   - Sales performance of each region
   - Revenue by month

----

### DATA ANALYSIS

##### EXCEL FUNCTIONS USED FOR ANALYSIS

```
Total Sales =SUM(H2:H9922)
```
````
Average Sales =AVERAGE(H2:H9922)
````

- AVERAGE SALES PER PRODUCT
````
Average sales for Shirt =AVERAGEIF(C2:C9922,C1986,H2:H9922)
````
````
Average sales for Hat =AVERAGEIF(C2:C9922,C2,H2:H9922)
````
````
Average sales for Gloves =AVERAGEIF(C2:C9922,C5269,H2:H9922)
````
````
Average sales for Jacket = AVERAGEIF(C2:C9922,C3777,H2:H9922)
````
````
Average sales for Shoes =AVERAGEIF(C2:C9922,C6530,H2:H9922)
````
````
Average sales for Socks =AVERAGEIF(C2:C9922,C9899,H2:H9922)
````

- TOTAL REVENUE BY REGION
````
Total Revenue for East =SUMIF(D2:D9922,D2,H2:H9922)
````
````
Total Revenue for North =SUMIF(D2:D9922,D4579,H2:H9922)
````
````
Total Revenue For South =SUMIF(D2:D9922,D6645,H2:H9922)
````
 ````
Total revenue for West =SUMIF(D2:D9922,D9909,H2:H9922)
````
- TOTAL REVENUE BY PRODUCT
````
Total Revenue for Shirt =SUMIF(C2:C9922,C4701,H2:H9922)
````
````
Total Revenue for Hat =SUMIF(C2:C9922,C3,H2:H9922)
````
````
Total Revenue for Gloves =SUMIF(C2:C9922,C5608,H2:H9922)
````
````
Total Revenue for Jacket =SUMIF(C2:C9922,C3094,H2:H9922)
````
````
Total Revenue for Shoes =SUMIF(C2:C9922,C5961,H2:H9922)
````
````
Total Revenue for Socks =SUMIF(C2:C9922,C9907,H2:H9922)
````

##### SQL QUERIES USED FOR ANALYSIS

````
select * from [dbo].[SALES DATA (Capstone Project)]
````
````
select
  product,
  sum(quantity * UnitPrice)  As Total_sales
from[dbo].[SALES DATA (Capstone Project)]
 group by
   product 
````
````   
select
  region,
  count(customer_id) AS Number_sales_transactions
from
  [dbo].[SALES DATA (Capstone Project)]
group by
  region
````
````
select
  product,
  sum(quantity * UnitPrice)  AS Total_Sales
from
  [dbo].[SALES DATA (Capstone Project)]
group by
  product
order by
  total_sales DESC
````
````
select Product,
	sum(quantity * UnitPrice) AS totalrevenue
from[dbo].[SALES DATA (Capstone Project)]
group by product;
````
````
select
MONTH(orderdate) As Month,
SUM(quantity * UnitPrice)  AS Monthly_sales
from [dbo].[SALES DATA (Capstone Project)]
where
YEAR(OrderDate)=2024
group by MONTH(OrderDate)
order by Month;
````
````
 select top 5 customer_id, 
 sum(quantity * UnitPrice)  as Total_Purchase_Amount
 from[dbo].[SALES DATA (Capstone Project)]
 group by Customer_Id
 order by 2 DESC;
 ````
````
 Select region,
 SUM(quantity * UnitPrice)  as Regional_sales,
 (SUM(quantity * UnitPrice) /(select SUM(Total_sales) from[dbo].[SALES DATA (Capstone Project)])*100) as Regional_Sales_Rate
 From [dbo].[SALES DATA (Capstone Project)]
 Group by Region
 order by Regional_Sales_Rate DESC;
 ````
````
select PRODUCT, SUM(quantity * UnitPrice)  AS Sales 
from[dbo].[SALES DATA (Capstone Project)]
where (quantity * UnitPrice)  <=0
group by Product
having MAX(OrderDate)<DATEADD(QUARTER,-1,GETDATE());
````

----

### DATA SUMMARIZATION
#### PIVORT TABLES
Pivort tables was used to summarize the data


- TOTAL SALES BY PRODUCT

  ![image](https://github.com/user-attachments/assets/0580f9a6-23b2-4283-916a-8cb84b393b50)

- TOTAL SALES BY REGION

  ![image](https://github.com/user-attachments/assets/318c4645-c893-457c-ad9e-a0c38420967d)

- TOTAL SALES BY MONTH

  ![image](https://github.com/user-attachments/assets/85dff39f-6b16-43dd-94b0-fc755a2bba7c)

----

  ### DATA VISUALIZATION
  - Power BI was used for data visualization

    ![image](https://github.com/user-attachments/assets/d610160e-5113-4b1b-b990-9d0cd251c093)

  SALES DATA POWER BI DASHBOARD

  ![image](https://github.com/user-attachments/assets/eda2e051-ed21-45ed-80f6-1f57f0e5c7dd)

  #### FILTER BY PRODUCT

  - HAT

![image](https://github.com/user-attachments/assets/b8070dfc-4b35-42da-acd7-836d2521da0a)

  - GLOVES

![image](https://github.com/user-attachments/assets/e001e7ed-e38b-49c9-a765-470adf7577b6)

  - SHIRT

![image](https://github.com/user-attachments/assets/54da76b2-6ccc-4171-9c90-f927d0256e1e)

  - SHOES

![image](https://github.com/user-attachments/assets/401aeb2d-6237-4a9f-b495-d8e199bb52b7)

  - SOCKS

![image](https://github.com/user-attachments/assets/67d53449-2e4f-4d57-9d13-24ff5d40dcfb)

  - JACKET

![image](https://github.com/user-attachments/assets/b8275707-e76c-41af-b2cb-d7e10a0d8f36)


#### FILTER BY REGION

 - EAST

![image](https://github.com/user-attachments/assets/fbdad99d-a02f-486c-b3da-e073cc59079c)

 - NORTH

![image](https://github.com/user-attachments/assets/e48c9a52-6e4c-487f-99dc-bed106e083f3)

 - SOUTH

![image](https://github.com/user-attachments/assets/6962dc9c-a198-4402-b750-e7c6b12039eb)

 - WEST

![image](https://github.com/user-attachments/assets/a03780c1-8ffd-4e25-b993-1b5ec0719227)

----

### INFERENCES

1. OVERALL SALES: The total Sale Two Million, One Hundred and One Thounsand, Ninety, the average sales was gotten to be Two hundred and Twelve. The sum of quantity of products sold is Sixty-eight Thousand, Four Hundred and Sixty-one.

2. MONTHLY SALES TREND: In the year 2023, the month Feburary has the highest sales with the sum of Two Hundred and Fourty-seven Thousand, Five Hundred. The month of April had the lowest sales with sum of Seven Thousand, Four Hundred and Twenty-five. The increament in sales in respect to month was not consistent.
In the year 2024, for the first eight months, Febuary also had the highest sales with the sum of Two hundred and Ninety-eight Thousand, Eight Hundred. The month of July had the lowest sales with the sum of Thirthy-seven Thousand, Two Hundred. The increament in sales over the months is not consistent.
The total sales for year 2023 and first eight months of 2024 is Two Million, One Hundred and One Thounsand, Ninety.

3. REGIONAL BREAKDOWN:
	-EAST: Total sales was Four Hundred and Eighty-five Thousand, Nine Hundred and Twenty-five. The average sales is One Hundred and Ninety-six. The Sum of quantity sold is Twenty Thousand, Three Hundred and Sixty-one.
For the east region sales was made on on March, July and Novembetr on the year 2023. In the year 2024 sales was made only on March and july.

	-NORTH: Total sales was Three Hundred and Eigty-seven thousand. The average sales was One Hundred and Fifty-six. The sum of quantity sold was Twelve Thousand, Four Hundred and Two. Sales was made only on January, May, and september 2023. In the year 2024, sales was made on January and May.

	-SOUTH: Total sales was Nine Hundred and Twenty-seven Thousand, Eight Hundred and Twenty. The average sales was Three Hundred and Four. The sum of quantity sold was Twenty-four thousand Two Hundred and Nienty-eight. Sales was made only on Febuary, June and October 2023. In the year 2024, sales was made on Febuary and June.

	-WEST: Total sales was Three Hundred Thousand, Three Hundred and Fourty-five . The average sales was One Hundred and Twenty-one. The sum of quantity sold was Eleven Thousand, Four Hundred. Sales was made only on April, August and December 2023. In the year 2024, sales was made on April and August.


4. TOP SELLING PRODUCTS: The highest selling product is Hat with Fifteen Thousand and Nine Hundred and Twenty-nine quantity sold,  followed by Shoe which is Forteen Thousand, Four Hundred, and two quantity sold.
The lowest selleing product is jacket with Five Thousand Four Hundred and Fifty-two.
- Hat was only sold at North, East and West.

- Glove was only sold at South and West Region

- Shirt was only sold at Northern and Eastern Region

 - Shoes was only sold at South, East and West Region

 - Socks was only sold at South and West Region

  -Jacket was only sold at North and East Region
   


### CONCLUSION
After the analysis I found out that all of the products are excluded for som regions. Strategic marketing and Advertisment should be adopted to introduced some of these products to the regions where they are barely used.This will help to increase the overall sales.














  


  

  









