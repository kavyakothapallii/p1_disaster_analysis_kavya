Project Overview 
This project analyzes disaster data across Indian regions to identify patterns in disaster frequency, affected population and economic loss.

Dashboard Problem Statements : 
1. Identify top 5 regions by total affected population.
2. Compare disaster severity distribution by disaster type.
3. Trend of disasters over time (monthly).
4. Economic loss vs affected population scatter plot.
5. Region-wise disaster frequency heatmap.

Tools and Technologies :
1. Python
2. Pandas 
3. Matplotlib
4. SQL 
5. Jupyter Notebook

Project Flow : 
1) Data cleaning and preprocessing :
   I worked with 3 datasets :
   1.regions.csv
   2.impact_assessment.csv
   3.disaster_events.csv

   Cleaning steps :
   1. Removed duplicate records from all datasets.
   2. Filled missing population and area values using median (to reduce skew impact).
   3. Replaced missing region names with "Unknown".
   4. Replaced missing affected people and economic loss values with 0 (business rule).
   5. Converted event dates to proper datetime format.
   6. Removed rows with invalid dates.
   7. Checked for negative values in numeric columns.
2) Python - MySql Connection and Deriving Insights :
   1.Connected using SQL Alchemy and mysql-connector-python
   2. Created tables and loaded cleaned datasets into database
   3. Used pandas method read_sql to write queries to derive the above insights.
      
3) Visualising the Data :
   1. Top 5 regions by population
      A bar chart was used to compare total affected population across regions.
      Bar charts are suitable for comparing values across categories because they clearly show magnitude differences.
   2. Disaster Distribution By Type
      A bar chart was used here.
      Bar charts are suitable for comparison and we had to compare disaster types here.
   3. Monthly Disaster Trend Over Time
      A line chart was used to analyze disaster frequency across months and years.
      Line charts are appropriate for time-series data because they show trends, patterns, and fluctuations over time.
   4. Economic loss vs affected population scatter plot.
      A scatter plot was used to examine the relationship between affected population and economic loss.
   5. Region-wise disaster frequency
      A heatmap was created using a pivot table of region and disaster type.
      Heatmaps are useful for visualizing intensity and patterns across two categorical dimensions.
4) Graphs :
   1. <img width="896" height="645" alt="Screenshot 2026-02-19 162508" src="https://github.com/user-attachments/assets/c3f1ca2f-a953-42cb-973d-08c9b64e6e36" />
   2. <img width="904" height="636" alt="Screenshot 2026-02-19 162710" src="https://github.com/user-attachments/assets/f748dd53-852e-44be-b7bb-412dd6d96329" />
   3. <img width="871" height="286" alt="Screenshot 2026-02-19 151004" src="https://github.com/user-attachments/assets/071557f9-e3fb-4a0d-a896-a7bdd6df9f26" />
   4. <img width="889" height="598" alt="Screenshot 2026-02-19 091917" src="https://github.com/user-attachments/assets/d4b8279f-dead-408b-adf2-edd97f6a9c42" />
   5. <img width="763" height="646" alt="Screenshot 2026-02-19 152243" src="https://github.com/user-attachments/assets/9255757f-4e65-4b0b-80aa-26cf6e061899" />




   
6) Insights I Discovered

1. Top 5 Regions By Population
   1. Tamil Nadu - 165,787,969
   2. Bihar - 165,514,943
   3. West Bengal - 153,265,505
   4. Odisha - 152,625,346
   5. Uttar Pradesh - 152,476,438

2. Disaster Distribution By Type 
   1. Unknown - 169 Disasters Happened and they weren't reported properly.
   2. Droughts - 167 
   3. Landslide - 161 
   4. Cyclone - 158 
   5. Flood - 152 
   6. Earthquake - 150 
   There is not a lot of distortion here.

3. Monthly Disaster Trend Over Time 
   1. Highest Month - June 2021 - 37 disasters 
   2. Lowest Months - February 2021 and April 2024 - 9 disasters 
   3. Year 2021 - March - 30 and June - 37 
   4. Year 2022 - Highest - December - 30 , Lowest - January - 15 
   5. Year 2023 - Consistent - Mostly 20-30 disasters a month 
   6. Year 2024 - rising till March but sharp drop in April.

4. Economic loss vs affected population scatter plot.
   No strong linear relationship is observed between affected population and economic loss.
   The dataset contains a large number of records where affected population or economic loss equals 0.
   This is due to the business rule: missing affected people and losses were replaced with 0.

5. Region-wise disaster frequency heatmap.
   The distribution of various disaster types across regions is depicted in the heatmap. According to the analysis, the frequency of disasters varies greatly by region, suggesting patterns of vulnerability specific to each area.
   The high frequency of landslides and cyclones in Tamil Nadu indicates a high risk of weather-related and coastal disasters. The region's climate variability is reflected in Gujarat's higher frequency of drought and flood events. Assam is exposed to multiple hazards, as evidenced by the comparatively higher frequency of earthquakes and cyclones.
   Kerala and Uttar Pradesh exhibit less extreme peaks and a more balanced distribution of disaster types. The frequency of droughts is relatively higher in Odisha.
   One noteworthy finding is the high number of disasters classified as "Unknown" in some areas, especially West Bengal. Missing disaster types were changed to "Unknown" in accordance with the business rule that was put into place. Consequently, greater values
