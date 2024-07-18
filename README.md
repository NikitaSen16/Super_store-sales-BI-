# Sales-Dashboard


## Problem Statement

The dashboard is created to analyze and visualize the sales performance of a superstore. It aims to provide actionable insights and identify key trends in sales and profit across various dimensions such as geography, customer segments, and product categories, facilitating data-driven decision-making for stakeholders.


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 :The column returns consists of #N/A, replace them with 0.
- Step 4 : In the report view, under the view tab, theme was selected.
- Step 5 : Since the data contains various ship modes,categories and states thus in order to represent these, new visuals were added from  visualizations pane in report view. 
- Step 6 : Slicer was added for four fields named "Cental", "East", "South" & "West".
- Step 7 : Four card visuals were added to the canvas, representing total sales, total profit, total quantity sold and average delivery time. 
- Step 8 : Two stacked area charts were added, one representing monthly sales by year on year and other representing monthly profit by YOY. 
- Step 9 : Donut visuals were also added showing sales by each segment and every payment method.  
- Step 10 : Calculated column was created in which, to find outthe average delivery time.

for creating new column following DAX expression was written;
       
    AvgDelivery = DATEDIFF('SuperStore_Sales_Dataset'[Order Date],'SuperStore_Sales_Dataset'[Ship Date],DAY)
        
Snap of new calculated column ,

![picneed1](https://github.com/user-attachments/assets/e983c279-0133-4481-8a7b-d8c76c9fc35c)

        
- Step 11 : New measure was created to find the sales forecast.

Following DAX expression was written for the same,
        
        salesforecast = SUMMARIZE('SuperStore_Sales_Dataset','SuperStore_Sales_Dataset'[Order Date],"Total sales", SUM(SuperStore_Sales_Dataset[Sales]))
        

![Screenshot 2024-07-18 193952](https://github.com/user-attachments/assets/7287618b-c949-4fd6-8adf-61af9bd8fdd4)

        
 - 

 
 - Step 12 : The report was then made.
 

# Report Snapshot  (Power BI DESKTOP)


![Screenshot 2024-07-18 194156](https://github.com/user-attachments/assets/3cef2ed4-b629-4978-a246-47957b5b2a64)

 
 # Report Snapshot  sales forecast (Power BI DESKTOP)

 
![Screenshot 2024-07-18 194506](https://github.com/user-attachments/assets/66776fb5-400e-4a40-9082-8a584de4e279)

# Insights


Following inferences can be drawn from the dashboard;

### [1] Total Sales = 1.6M

### [2] Total Profit = 175.3K

### [3] Total Quantity sold = 22.3K

### [4] Average delivery time = 4 days




