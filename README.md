# Blinkit Sales Anaysis Dashboard


## Problem Statement

- The Blinkit Sales Analysis Power BI project aims to provide an insightful and interactive dashboard for analyzing sales performance across various dimensions. ​


- This project will facilitate data-driven decision-making by visualizing key metrics, identifying trends, and uncovering actionable insights within Blinkit's sales data.​

- The project will empower stakeholders with valuable insights into sales performance, enabling informed decision-making and strategic planning.​


### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
- Step 3 : Extract, clean, and transform data from various sources to ensure accuracy and consistency.​

- Step 4 : Generate useful and insightful KPIs according to the business requirement.​

- Step 5 : Build the Power BI dashboard with interactive features and visualizations based on the defined requirements.

- step 6 : Create a matrics to insert a proper slicer for whole dashboard that includes all KPIs, charts and many more

for creating new matrix following DAX expression was written;
      
       Metrics = {
    ("Total Sales", NAMEOF('BlinkIT Grocery Data'[Total Sales]), 0),
    ("Avg Sales", NAMEOF('BlinkIT Grocery Data'[Avg Sales]), 1),
    ("Avg Rating", NAMEOF('BlinkIT Grocery Data'[Avg Rating]), 2),
    ("No of Items", NAMEOF('BlinkIT Grocery Data'[No of Items]), 3)
}
        
Snap of new calculated column ,

![Screenshot (1)](https://github.com/user-attachments/assets/dd2c856b-4126-4069-9ebc-050307838d4b)


        
- Step 7 : New measure was created to find total revenue.

Following DAX expression was written for the same,
        
        Total Sales = SUM('BlinkIT Grocery Data'[Sales])
        
A card visual was used to represent count of customers.

![Screenshot (4)](https://github.com/user-attachments/assets/0bb2aabd-58cb-4767-809f-b2424affcbe9)


        
 - Step 8 : New measure was created to find average sales,
 
 Following DAX expression was written for the same,
 
         Avg Sales = AVERAGE('BlinkIT Grocery Data'[Sales])
 
 A card visual was used to represent this value.
 

 
 ![Screenshot (5)](https://github.com/user-attachments/assets/88f0e04c-425d-43e8-8487-0e1381968fd3)


 
 - Step 9 : New measure was created to find out average rating per item.
 
 Following DAX expression was written to find total distance,
 
         Avg Rating = AVERAGE('BlinkIT Grocery Data'[Rating])
    
 A card visual was used to represent this average rating.
 
 
 ![Screenshot (6)](https://github.com/user-attachments/assets/914d9a12-daf3-4ae5-a2aa-cfd165ead577)
 
 - Step 10 : New measure was created to find out total number of items


         No of Items = COUNTROWS('BlinkIT Grocery Data')
 
 
![Screenshot (7)](https://github.com/user-attachments/assets/bf685955-01b1-4cbd-b04a-87e1ab114939)

# Snapshot of Dashboard (Power BI Service)

![Screenshot (8)](https://github.com/user-attachments/assets/2bb44b34-c6cd-43e4-a70f-6bf70e2ab8bf)

 


# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Sales = $1.20M

   Highest number of Sales = Fruits & Vegetables ($178.12K)

   Lowest number of Sales = Seafoods ($9.08K)

   Highest number of Sales by outlet size = Medium size($507.9K)

   Lowset number of Sales by outlet size = High ($248.99K)


           
### [2] Average Ratings

    a) Meat - 4.0/5
    b) Fruits & Vegetables - 3.91/5
    c) Hpousehold - 3.95/5
    d) Health & Hygiene - 3.93/5
    e) Soft Drinks - 3.89/5
    f) Hard Drinks - 3.84/5
    g) Baking Goods - 3.95/5
    h) Frozen Foods - 3.93/5
    i) Dairy - 3.92/5
    j) Seafood - 3.91/5
    k) Starchy Foods - 3.91/5
    l) Breads - 3.83/5
    m) Breakfast - 3.90/5
    n) Snack Foods - 3.90/5
    o) Canned - 3.95/5
    p) Others - 3.93/5
  
  while calculating average rating, null values have been ignored as they were not relevant for some customers. 
  
  These ratings will change if different visual filters will be applied.  
  

 ### [3] Some other insights
 
 - Total 8523 items sold by different outlets at different location.​

- Items with Low fat content have the highest sales of 776.32K compared to regular fat i.e., 425.36K.​

- Data reveals that sales reached their peak in 2018, highlighting it as the highest-performing year in terms of revenue generation.​
 


 
