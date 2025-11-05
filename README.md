# MIS-311_Data: Cost of Living
## Part 1: Data Analysis and Insight 

Python is one of the most popular languages ​​for analysts. In this project, I will apply basic Python to analyze data on cost of living in different regions, and create visualizations for the data. 
This project includes the following parts:
1. Overviewing the dataset
2. Checking and processing data types
3. Cleaning the dataset
4. Clarifying the insights
5. Conclusion
---
### 1. Overviewing the dataset
This dataset provides information on the cost of living and average monthly income across different countries, categorized by year and region. It allows for comparison of living standards by examining whether income levels are sufficient to cover typical living expenses. The data can be used to analyze economic conditions, evaluate affordability, and compare the purchasing power of individuals in various parts of the world.

This is the discription of 5 variables and the type the them:
1. Country (object): The name of the country where the data was collected.
2. Year (int): The year when the data was collected.
3. Average_Monthly_Income (float64): The average monthly income of individuals in USD.
4. Cost_of_Living (int): The average monthly cost of living in USD, including essentials like housing, food, and utilities.
5. Region (object): The geographical region to which the country belongs 
---
### 2. Checking and processing data types
* Using `.shape` to check the number of rows and columns, the data has **201 rows and 5 columns**
<img width="327" height="93" alt="image" src="https://github.com/user-attachments/assets/c385178e-9962-4cb1-a8c3-539e39d68498" />

* Using `.dtypes` to check the data type 

<img width="276" height="272" alt="image" src="https://github.com/user-attachments/assets/19b5a016-79d3-477f-8b2b-101e62ac7423" />

* It is not fit with the data discription, handling the data type of "Cost_of_Living" column into int type. And then collect the final results

<img width="1001" height="368" alt="image" src="https://github.com/user-attachments/assets/5b129bc1-b293-480e-b1f3-7a780f41d17d" />

---

### 3. Cleaning the dataset
* By using `.isna()` to find missing values.
   `.iloc[25:40]` means requesting to display the results from row 25 to row 40. **True** indicates a missing value  and **False** indicates no missing value.

  <img width="479" height="449" alt="image" src="https://github.com/user-attachments/assets/f228e564-ef74-45cb-97be-28ba93ee2ec3" />
  
* Use the `.sum()` syntax to count how many missing values ​​there are in each column.
  
<img width="253" height="241" alt="image" src="https://github.com/user-attachments/assets/3920621c-acd9-402b-b56a-de08459f93ee" />

* Use the `.dropna()` method to removes rows with missing data.

<img width="510" height="398" alt="image" src="https://github.com/user-attachments/assets/4c680e15-1e66-4fcc-a693-de32c34078d8" />

* Save these results into a new Excel data file, ensure the consistency in the discovered data.
  
  <img width="314" height="45" alt="image" src="https://github.com/user-attachments/assets/eb6db6a0-6aa8-4840-a26d-38662f434c10" />

* Using the ` df.duplicated()` and `.value_counts()` syntax to find the total number of duplicate rows. 

<img width="267" height="476" alt="image" src="https://github.com/user-attachments/assets/df71e00d-00d6-470c-8467-bdff3dae4cac" />

 **True** is a duplicate value, and **False** is no duplicate rows.

 * Using the .drop_duplicates syntax to remove duplicate value, and then update for the new data to analyze

   <img width="711" height="617" alt="image" src="https://github.com/user-attachments/assets/7932c3d6-1f80-4cf4-8d6f-a8fdb4c0e0b4" />

---
### 4. Clarifying the insights
#### *4.1. The 1st insight: The highest average monthly incomes.*
First, group the data by the Region column, then calculate the average monthly income (Average_Monthly_Income) of each region using the `.sum()` function. Finally, use `.reset_index()` to return the Region column to its normal form and display the result using `display()`. Furthermore, visualize data with bar charts

<img width="919" height="342" alt="image" src="https://github.com/user-attachments/assets/b43e57bb-b321-42ae-bab1-6a97f6b77f71" />

<img width="887" height="522" alt="image" src="https://github.com/user-attachments/assets/6253b266-a0ed-41d7-a4fa-7d28bd31dc12" />

*Figure 1: The highest average monthly incomes by region*

**Comment**: Based on the results of average monthly income by region, it can be seen that Europe and Asia have the highest total income, showing the concentration of many developed and economically strong countries in these two regions. While North America also has a relatively high total income, Africa and South America have lower total incomes, showing the difference in income levels and economic conditions compared to other regions. Average incomes between regions in the world have significant differences depending on the level of economic development and employment opportunities of each region.

#### *4.2. The 2nd insight: The percentage of cost of living by region*
Calculate the total cost of living by regions and convert it into the percentage and visualize data with pie charts.
<img width="220" height="208" alt="image" src="https://github.com/user-attachments/assets/3b902986-8704-41e3-b876-e1ef95fbeb22" />


<img width="564" height="494" alt="image" src="https://github.com/user-attachments/assets/d9be11a0-9c22-4fc3-b506-39dc3c6c2973" />

*Figure 2: The percentage of cost of living by region*

**Comment:** It is clear from the chart above that the total cost of living is concentrated mainly in the two leading regions, North America (25.0%) and Asia (23.7%), which account for nearly half of the total cost. Europe (22.1%) accounts for the next most significant proportion. In contrast, the remaining three continents - Oceania, Africa and South America - all recorded a contribution of less than 12%. This highlights the dominant role of North America and Asia in shaping the total cost of living surveyed.

---

### 5. Conclusion
Overall, the findings show that North America and Asia play the biggest role in shaping the total cost of living, while Europe also holds a large share. At the same time, Europe and Asia have the highest total income levels, reflecting their strong and developed economies. In contrast, regions like Africa, South America, and Oceania show both lower living costs and lower income levels. This suggests that areas with stronger economies tend to have higher living expenses but also offer better income opportunities.
















  









