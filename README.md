# Fruit Production
 Predicting Graple Fruit production
 
- ## Datasets
  - Production Quantity.csv has 4 columns
  ```
  - start_date, end_date: start day and end day of each month between January 2015 to Dec 2020.
  - prod: production quantity of Grople syrup in tonnes at monthly frequency
  - region_id: A unique identifier for the 10 provinces
  ```
  
  - Daily Precipitation.csv: has 4 columns
  ```
  - start_date, end_date: start day and end day at a daily frequency between January 1, 2014 to Mar 13, 2022.
  - precip: Precipitation quantity (in mm) at daily frequency
  - region_id: A unique identifier for the 10 provinces
  ```
  - Daily Soil Moisture.csv: has 4 columns
  ```
  - start_date, end_date: start day and end day at daily frequency between January 1, 2014 to Mar 6, 2022.
  - smos: Soil Moisture at 5cm depth (measured by the ratio Vol/Vol) at daily frequency
  - region_id: A unique identifier for the 10 provinces
  ```
  - Daily Temperature.csv: has 4 columns
  ```
  - start_date, end_date: start day and end day at daily frequency between January 1, 2014 to Mar 13, 2022.
  - temp: Average daily temperature on the surface of the land (in celsius) at daily frequency
  - region_id: A unique identifier for the 10 provinces
  ```
  - Eight Day NDVI.csv: has 4 columns
  ```
  - start_date, end_date: start day and end day at 8-day frequency between Dec 27, 2013 to Mar 13, 2022.
  - ndvi: Normalized Difference Vegetation Index (NDVI is a ratio which ranges between [-1, 1] and captures the vegetation abundance of an area) at 8 day frequency between the given periods**
  - region_id: A unique identifier for the 10 provinces
  ```
  - predicted_production_qty.csv: has 4 columns
  ````
  - start_date, end_date: start day and end day of each month between Jan 2021 to Dec 2021.
  - prod: This column needs to be filled by the candidate with their predictions of Grople syrup.
  - region_id: A unique identifier for the 10 provinces
  ```
- ## Summary
 - All the datasets were combined to get an annual value for each production cycle with the start date serving as the end date of the annual cycle
 - The mean values were then combined and matched with each region id
 - The correlation was calculated and all the variable were found to be almost independent of each other with only the NDVI having the highest correlation of 0.67 with respect to the target column (total production)
 - The region id was one hot encoded and all the columns were scaled using a min max scaler
 - Using pipeline different models : gradient booster regressor, random forest and decision tree regressor, and SVR, were tested and evaluated to make the final prediction
