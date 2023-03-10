![image](https://drive.google.com/uc?id=1KBhOlprSFdBN12iuVTLqHszs3NhCa3AH)

# **Data Science Food Sales Predictions**


## ***Analyzing Food Items Properties / Outlet Data to Predict Food Sales***

---

*  ### Ingrid Arbieto Nelson

> ### *With a wide variety of Food products and shopping outlets in the marketplace, there is so much data available to analyze what Food Items sell! The purpose of this analysis is to delve into various Food Item properties and types of Outlets to see if we can predict Food Item Sales. The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in increasing sales.*

### **Data:**

---


* ### [Original data source](https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/)
* ### For this dataset, there were 8,523 rows and 12 columns.

### **Data Dictionary:**

---

![image](https://drive.google.com/uc?id=1kdsKuuQa6PA5zx6PcI_J7amlONsbFaXj)

## **Data Cleaning**

---





* #### After dropping irrevalent columns, these Food Item Properties / Outlet Properties remain:
  *   ***Item Weight*** - I chose to keep item weight, as heavier items may cost more. It may not be, but I'm not a SME on food sales.
  *   ***Item Fat Content*** - It may be interesting to compare diet food to yummy fat-full food.
  *   ***Item Visibility*** - If an item is highly visable, it seems more likely that the customer would buy it.
  *   ***Item Type*** - Which food item types sell more!
  *   ***Item_MRP*** - Sales price would definitely be relavant to sales.
  *   ***Outlet Size*** - How big an outlet is seems to relate to how much outlet could sell.
  *   ***Outlet Location*** - Location! Location! Location! - big part of sales
  *   ***Item_Outlet_Sales*** - Primary Sales datapoint!
* #### After the data was cleaned, and the following processes were performed:

## **Exploratory Data Analysis:**

---

* During the exploratory data analysis, a boxplot and histogram was visualized for each numeric datatype column. 
* Also, a barplot was visualized for each categorical column. 
* This gave a good baseline for all of the numeric and categorical columns for univariate EDA.
* A heatmap showed the correlation of food item & outlet properties to Item Outlet Sales for multivariate EDA.
<br />

### **EDA for Food Item Outlet Sales**
![image](https://drive.google.com/uc?id=1MlXut2zLYZiHaBRk7LnYE2igMu5TTJAV)
*  Histogram skews to the right.
*  There are a number of outliers for food item sales, likely due to large variety of foods, number of items.
<br />

### **EDA for Food Item Type**
![image](https://drive.google.com/uc?id=1bgIiFXqJddXGE1C7gvji5V6OELGNtYeS)
* Fruits & vegetables, Snacks, and Household items, such as toilet paper, are the top 3 items sold!
* Seafood is the least food item sold.
<br />

### **EDA Heatmap Correlation of Food Item Sales**
![image](https://drive.google.com/uc?id=1R7su-REmp4QDbYmL5Wk5TcORlPW6aCMb)
* The only item with correlation is between Item Retail Price and Food Item Sales. These are moderately correlated.
* Other variables show no correlation.
<br />

## **Explanatory Data Analysis**

---
* ### Explanatory Data Analysis answered these questions regarding how Food Item Properties predict Food Item Sales:
  
## **1. What are the Top Items sold?**  
![image](https://drive.google.com/uc?id=1bgIiFXqJddXGE1C7gvji5V6OELGNtYeS)


---

* #### The top food items sold are
   * #### **```Fruits and Vegetables```**
   * #### **```Snack Foods```**
   * #### **```Household```**
   * #### **```Frozen Foods```**
   * #### **```Dairy```**

## **2 Is there a correlation between Food Item Sales and Item Price?**
![image](https://drive.google.com/uc?id=1e_QsCzCn9dejsibV9Squ9Xa6xZLUKmqo)

#### **2. Is there a correlation between Food Item Sales and Item Price?**

---

* #### The top average Food sales categories are 
   * #### **```1 Starchy Foods```**
   * #### **```2 Seafood```**
   * #### **```3 Fruits and Vegetables```**
   * #### **```4 Snack Foods```**
   * #### **```5 Household```**
   * #### **```6 Dairy```**
* #### The highest price items are
   * #### **```1 Household```**
   * #### **```2 Dairy```**
   * #### **```3 Starchy Foods```**
   * #### **```4 Snack Foods```**
   * #### **```5 Fruits and Vegetables```**
   * #### **```6 Seafood```**
* #### The bottom average Food sales categories are 
   * #### **```1 Health and Hygience```**
   * #### **```2 Soft Drinks```**
   * #### **```3 Baking Goods```**
   * #### **```4 Others```**

* #### The lowest price items are
   * #### **```1 Others```**
   * #### **```2 Soft Drinks```**
   * #### **```3 Health and Hygience```**
   * #### **```4 Baking Goods```**


* #### In conclusion, there is a positive correlation between Food Item Sales and Item Price.

## **3 Is there a correlation between Food Item Sales and Item Price by Outlet Size?**
![image](https://drive.google.com/uc?id=1j2lTadlfWn8IVQljpRy_N8-wKOKo0fDR)
* #### This lmplot shows the line of best fit. 
* #### The most sales of food items occurred at Medium-size Outlets. 
* #### Medium supermarket outlets are the most common size.
* #### Food sales are the highest, based on the most common Supermarket size.
* #### There is a the moderate positive correlation between Food Item Retail Price and Food Item Sales, by Outlet Size.
* #### In conclusion, the greater food sales reflect the most common size of Supermarket : Medium-sized Outlets.
<br />

## **Machine Learning**
---
*  ### Machine Learning was performed on this models to find the best model that predicts Food Item Sales based on Food Item & Outlet properties:

   * Linear Regression Model
   * Decision Tree Regressor Model
   * Tuned Decision Tree Regressor Model
   * Bagged Tree Regressor Model
   * Tuned Bagged Tree Regressor Model
   * Random Forest Regressor Model
   * Tuned Random Forest Regressor Model

## **Summary of Models Evaluated:**

---
![image](https://drive.google.com/uc?id=1gUjnEvxZeCOKuRNK01PGOUrvgvO389v2)
#### The best model to predict Item Outlet Sales is the **Optimized Random Forest Model**. 
* #### The optimized Random Forest Model can account for 53.41% of the variation of the Item Outlet Sales based on the features Item Weight, Item Fat Content, Item Visibility, Item Type, Item MRP (or Sales Price), Outlet Size, and Outlet_Location Type.
* #### The optimized Random Forest Model has moderate bias, but overall the best R^2 performance on the testing data.
* #### The optimized Random Forest Model also has the lowest Root Mean Square error (RMSE), 1,133.80. The RSME metric penalizes larger errors more. The RMSE is a better metric to evaluate than the Mean Absolute Error (MAE), as unexpected large errors can be very bad compared to consistent expected errors. 
* #### The median Item Outlet Sales is 1,794.33. On average, the Item Outlet Sales is off by 1,133.80 or 63.18%. 
* #### The Optimized Random Forest model predicts within 1,133.80 of the Item Outlet Sales, which is a low-to-medium correlation. Given the wide variety of items and sales, this seems more of a middle of the road optimized model.

### **Recommendation**

---

#### My recommendation is the optimized Random Forest Model as a lowto-medium correlation good predictor of Food Item Sales.
