# CAPSTONE-PROJECT-DOCUMENTATION 1

----

## PROJECT TITTLE: CAPSTONE SALES DATA
----
[PROJECT OVERVIEW](#project-overview)

[DATA SOURCES](#data-sources)

[TOOLS USED](#tools-used)

[DATA CLEANING AND PREPARATIONS](#data-cleaning-and-preparations)

[EXPLORATORY DATA ANALYSIS](#exploratory-data-analysis)

[DATA ANALYSIS](#data-analysis)

[DATA SUMMARIZATION](#data-summarization)

[DATA VISUALIZATION](#data-visualization)

[INFERENCE](#inference)

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
   - The average revenue 
   - Total revenue generated in each region
   - The highest selling locations
   - Sales performance of each region
   - Revenue by month

----

### DATA ANALYSIS
#####EXCEL FUNCTIONS USED FOR THE ANALYSIS
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










