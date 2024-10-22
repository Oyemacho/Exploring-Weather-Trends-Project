# Exploring Weather Trends - Project Local City - Ibadan

## Project Overview
This project explores weather trends in Ibadan, Nigeria, and compares them with global temperature trends over a century (1900-1999). The analysis was performed using SQL for data extraction and Google Sheets for data cleaning, preparation, and visualization.

## Tools Used
### A. SQL (Structured Query Language)
- **Purpose:** Extracting temperature data from databases.
- **Process:**
  - Wrote queries in the SQL Workspace provided by Udacity.
  - Extracted yearly average temperature data for Ibadan (1985-2013).
  - Extracted global average temperature data (1750-2015).
  - Saved the query results as CSV files.
  - **Example Queries:**
    - **Ibadan:**
      ```sql
      SELECT year, avg_temp
      FROM city_data
      WHERE country LIKE 'Nigeria' AND city like 'Ibadan'
      ORDER BY year;
      ```
    - **Global:**
      ```sql
      SELECT *
      FROM global_data;
      ```

### B. Google Sheets
- **Purpose:** Data cleaning, preparation, and analysis.
- **Process:**
  - Imported CSV data into Google Sheets.
  - Cleaned the data by removing null values and irrelevant years (before 1900 and after 1999).
  - Calculated a 10-year moving average for both local (Ibadan) and global temperatures.

## Calculating the Moving Average
- **Objective:** To analyze temperature trends over the century from 1900 to 1999.
- **Method:**
  - Created columns for "Moving Avg Temp Ibadan" and "Moving Avg Temp Global".
  - Used the `AVERAGE()` function to calculate the 10-year moving average.
  - Plotted a line chart to visualize the trends and comparisons.

## Key Considerations for Visualization
- **Data Span:** Focused on a 100-year period (1900-1999) due to the available data ranges.
- **Axis Intervals:** Set vertical axis intervals to 1°C to highlight temperature changes.
- **Chart Type:** Used line charts for detailed time-series analysis.

## Visualization
### Local (Ibadan) Temperature Trend
- Highlighted changes between 25°C and 28°C.

### Global Temperature Trend
- Highlighted changes between 7°C and 10°C.

## Observations
1. **Temperature Comparison:** 
   - Average temperature in Ibadan (26.47°C) was significantly higher than the global average (8.64°C) from 1900 to 1999.
2. **Consistent Margin:**
   - The temperature margin between Ibadan and global averages remained relatively consistent (~17.48°C in 1900 to ~17.67°C in 1999).
3. **Temperature Increase:**
   - Both local and global temperatures rose by approximately 1°C over the century.
4. **Trend Analysis:**
   - Noted a slight temperature decrease in 1916 followed by a steady rise.
   - The global temperature trend indicates a significant warming pattern, emphasizing the need for sustainable practices to combat global warming.

## Conclusion
This project highlights the temperature trends in Ibadan and globally, providing insights into the changing climate over the last century. The findings underscore the importance of addressing global warming through sustainable practices.
