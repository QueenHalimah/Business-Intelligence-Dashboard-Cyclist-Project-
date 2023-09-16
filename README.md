# Business Intelligence Dashboard Cyclist Project

Welcome to Cyclistic! 
Congrats on your new job with the business intelligence team at Cyclistic, a fictional bike-share company in New York City. In order to provide your team with both BI business value and organizational data maturity, you will use your knowledge of the BI stages: capture, analyze, and monitor. By the time you are done, you will have an end-of-course project that demonstrates your knowledge and skills to potential employers.

Your meeting notes
You recently attended a meeting with key stakeholders to gather details about this BI project. The following details are your notes from the meeting. Use the information they contain to complete the Stakeholder Requirements Document, Project Requirements Document, and Planning Document.

Project background -

Primary dataset: 
NYC Citi Bike Trips- https://console.cloud.google.com/marketplace/details/city-of-new-york/nyc-citi-bike?project=my-project-employees-table

Secondary dataset: 
Census Bureau US Boundaries- https://console.cloud.google.com/marketplace/product/united-states-census-bureau/us-geographic-boundaries?project=my-project-employees-table

Cyclistic has partnered with the city of New York to provide shared bikes. Currently, there are bike stations located throughout Manhattan and neighboring boroughs. Customers are able to rent bikes for easy travel between stations at these locations.

Cyclistic’s Customer Growth Team is creating a business plan for next year. The team wants to understand how their customers are using their bikes; their top priority is identifying customer demand at different station locations.

Cyclistic has captured data points for every trip taken by their customers, including:

Trip start time and location (station number, and its latitude/longitude)

Trip end time and location (station number, and its latitude/longitude)

The rented bike’s identification number

The type of customer (either a one-time customer, or a subscriber)

The dataset includes millions of rides, so the team wants a dashboard that summarizes key insights. Business plans that are driven by customer insights are more successful than plans driven by just internal staff observations. The executive summary must include key data points that are summarized and aggregated in order for the leadership team to get a clear vision of how customers are using Cyclistic.

Stakeholders: 

Sara Romero, VP, Marketing

Ernest Cox, VP,  Product Development

Jamal Harris, Director, Customer Data

Nina Locklear, Director, Procurement

Team members: 

Adhira Patel, API Strategist

Megan Pirato, Data Warehousing Specialist

Rick Andersson, Manager, Data Governance 

Tessa Blackwell, Data Analyst

Brianne Sand, Director, IT

Shareefah Hakimi, Project Manager

*Primary contacts are Adhira, Megan, Rick, and Tessa. 

Per Sara: Dashboard needs to be accessible, with large print and text-to-speech alternatives.

Project approvals and dependencies:

The datasets will include customer (user) data, which Jamal will need to approve. Also the project might need approval by the teams that own specific product data, including bike trip duration and bike identification numbers. So I need to make sure that stakeholders have data access to all datasets.

Project goal: Grow Cyclistic’s Customer Base

Details from Ms. Romero:

Understand what customers want, what makes a successful product, and how new stations might alleviate demand in different geographical areas.

Understand how the current line of bikes are used.

How can we apply customer usage insights to inform new station growth?

The customer growth wants to understand how different users (subscribers and non-subscribers) use our bikes. We’ll want to investigate a large group of users to get a fair representation of users across locations and with low- to high-activity levels.

Keep in mind users might use Cyclistic less when the weather is inclement. This should be visible in the dashboard.

   The deliverables and metrics:

A table or map visualization exploring starting and ending station locations, aggregated by location. I can use any location identifier, such as station, zip code, neighborhood, and/or borough. This should show the number of trips at starting locations.

Tip: You can show either a table or a map. For more about creating maps in Tableau, check out the
  Build a simple map guide on Tableau Help 
. For a table, you could include just starting locations or a combination of starting and ending locations. 

A visualization showing which destination (ending) locations are popular based on the total trip minutes.

Tip: Focus on peak months.

A visualization that focuses on trends from the summer of 2015.

A visualization showing the percent growth in the number of trips year over year.

Gather insights about congestion at stations.

Tip: For each day, use a table calculation to calculate the net of start and ending trips per station. This gives an approximation of whether there are more bikes coming in or out of a station.

Gather insights about the number of trips across all starting and ending locations.

Gather insights about peak usage by time of day, season, and the impact of weather.

*Dashboard must be created in 6 weeks!

Measure success:

Analyze data that spans at least one year to see how seasonality affects usage. Exploring data that spans multiple months will capture peaks and valleys in usage. Evaluate each trip on the number of rides per starting location and per day/month/year to understand trends. For example, do customers use Cyclistic less when it rains? Or does bikeshare demand stay consistent? Does this vary by location and user types (subscribers vs. nonsubscribers)? Use these outcomes to find out more about what impacts customer demand.

Other considerations:

The dataset includes latitude and longitude of stations but does not identify more geographic aggregation details, such as zip code, neighborhood name, or borough. The team will provide a separate database with this data. 

The weather data provided does not include what time precipitation occurred; it’s possible that on some days, it precipitated during off-peak hours. However, for the purpose of this dashboard, I should assume any amount of precipitation that occurred on the day of the trip could have an impact.

Starting bike trips at a location will be impossible if there are no bikes available at a station, so we might need to consider other factors for demand.

Finally, the data must not include any personal info (name, email, phone, address). Personal info is not necessary for this project. Anonymize users to avoid bias. 

People with dashboard-viewing privileges: 

Adhira, Brianne, Ernest, Jamal, Megan, Nina, Rick, Shareefah, Sara, Tessa

Roll-out:

Week 1: Dataset assigned. Initial design for fields and BikeIDs validated to fit the requirements.

Weeks 2–3: SQL and ETL development

Weeks 3–4: Finalize SQL. Dashboard design. 1st draft review with peers.

Weeks 5–6: Dashboard development and testing

Questions:

How were bikes used by our customers?

How can we apply insights from the data generated by trip data?

Next steps
As you use these notes to complete the key BI documents, take time to consider:

How to organize the various points and steps

How to group similar topics

Whether the information is relevant to the project

Whether the metrics are effective or not

Let's start by reviewing what we have in our Stakeholder Requirements Document, Project Requirements Document, and Planning Document.

Stakeholder Requirements Document:

[Activity_ Stakeholder Requirements Document - Cyclistic.pdf](https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/files/12641186/Activity_.Stakeholder.Requirements.Document.-.Cyclistic.pdf)

Project Requirements Document:

[Activity_ Project Requirements Document - Cyclistic.pdf](https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/files/12641200/Activity_.Project.Requirements.Document.-.Cyclistic.pdf)

Planning Document:

[Activity_ Strategy Document - Cyclistic.pdf](https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/files/12641203/Activity_.Strategy.Document.-.Cyclistic.pdf)

CREATING OUR TARGET TABLE

The next step in our project will be to use our knowledge of SQL and potentially Google Dataflow to combine and move the key datasets you identified for the Cyclistic project into a target table. This represents the extraction phase of an ETL pipeline, when data is pulled from different sources and moved to its destination. I will then use the table created in this activity to develop the final dashboard for stakeholders.

The key metrics the stakeholders and I have identified, their business questions, and what data you’ll need to develop the final dashboard is crucial. Previously, we explored the different public datasets that stakeholders provided and uploaded the zip code table a colleague shared with me. For the final dashboard, I will need to create two target tables: a table to capture the entire year and a table that focuses on summer trends. Here is an example of a query to capture a table with data from the entire year:

  ```SELECT
  TRI.usertype,
  ZIPSTART.zip_code AS zip_code_start,
  ZIPSTARTNAME.borough borough_start,
  ZIPSTARTNAME.neighborhood AS neighborhood_start,
  ZIPEND.zip_code AS zip_code_end,
  ZIPENDNAME.borough borough_end,
  ZIPENDNAME.neighborhood AS neighborhood_end, -- Since this is a fictional dashboard, you can add 5 years to make it look recent
  DATE_ADD(DATE(TRI.starttime), INTERVAL 5 YEAR) AS start_day,
  DATE_ADD(DATE(TRI.stoptime), INTERVAL 5 YEAR) AS stop_day,
  WEA.temp AS day_mean_temperature, -- Mean temp
  WEA.wdsp AS day_mean_wind_speed, -- Mean wind speed
  WEA.prcp day_total_precipitation, -- Total precipitation
  -- Group trips into 10 minute intervals to reduces the number of rows
  ROUND(CAST(TRI.tripduration / 60 AS INT64), -1) AS trip_minutes,
  COUNT(TRI.bikeid) AS trip_count
FROM
  `bigquery-public-data.new_york_citibike.citibike_trips` AS TRI
INNER JOIN
  `bigquery-public-data.geo_us_boundaries.zip_codes` ZIPSTART
  ON ST_WITHIN(
    ST_GEOGPOINT(TRI.start_station_longitude, TRI.start_station_latitude),
    ZIPSTART.zip_code_geom)
INNER JOIN
  `bigquery-public-data.geo_us_boundaries.zip_codes` ZIPEND
  ON ST_WITHIN(
    ST_GEOGPOINT(TRI.end_station_longitude, TRI.end_station_latitude),
    ZIPEND.zip_code_geom)
INNER JOIN
  `bigquery-public-data.noaa_gsod.gsod20*` AS WEA
  ON PARSE_DATE("%Y%m%d", CONCAT(WEA.year, WEA.mo, WEA.da)) = DATE(TRI.starttime)
INNER JOIN
  -- Note! Add your zip code table name, enclosed in backticks: `example_table`
  `(insert your table name) zipcodes` AS ZIPSTARTNAME
  ON ZIPSTART.zip_code = CAST(ZIPSTARTNAME.zip AS STRING)
INNER JOIN
  -- Note! Add your zipcode table name, enclosed in backticks: `example_table`
  `(insert your table name) zipcodes` AS ZIPENDNAME
  ON ZIPEND.zip_code = CAST(ZIPENDNAME.zip AS STRING)
WHERE-- This takes the weather data from one weather station
  WEA.wban = '94728' -- NEW YORK CENTRAL PARK
  -- Use data from 2014 and 2015
  AND EXTRACT(YEAR FROM DATE(TRI.starttime)) BETWEEN 2014 AND 2015
GROUP BY
  1,
  2,
  3,
  4,
  5,
  6,
  7,
  8,
  9,
  10,
  11,
  12,
  13
```
Note that this query includes a DATE_ADD function to add five years to the data. The public data we are using to create this dashboard is from 2014 and 2015, so this is a way to make my dashboard appear more recent. Once we execute the code, it will take a few moments to process. After the query has finished running, we will be able to download the tables as CSV files by using the Save Results dropdown and selecting the appropriate file type. Example at screenshot below:

![Project Target Table](https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/assets/80160857/b37abc5f-955f-4576-ab63-e5efc054bc5e)

The result of this query is a merged target table that JOINs the public datasets and the zip code table that was uploaded. 

Additionally, we will need to execute a query that captured data from just the summer season:

``` SELECT
 TRI.usertype,
 TRI.start_station_longitude,
 TRI.start_station_latitude,
 TRI.end_station_longitude,
 TRI.end_station_latitude,
 ZIPSTART.zip_code AS zip_code_start,
 ZIPSTARTNAME.borough borough_start,
 ZIPSTARTNAME.neighborhood AS neighborhood_start,
 ZIPEND.zip_code AS zip_code_end,
  ZIPENDNAME.borough borough_end,
  ZIPENDNAME.neighborhood AS neighborhood_end,
 -- Since we're using trips from 2014 and 2015, we will add 5 years to make it look recent
  DATE_ADD(DATE(TRI.starttime), INTERVAL 5 YEAR) AS start_day,
 DATE_ADD(DATE(TRI.stoptime), INTERVAL 5 YEAR) AS stop_day,
  WEA.temp AS day_mean_temperature, -- Mean temp
 WEA.wdsp AS day_mean_wind_speed, -- Mean wind speed
  WEA.prcp day_total_precipitation, -- Total precipitation
  -- We will group trips into 10 minute intervals, which also reduces the number of 
rowsROUND(CAST(TRI.tripduration / 60 AS INT64), -1) AS trip_minutes,
 TRI.bikeid
FROM  
 `bigquery-public-data.new_york_citibike.citibike_trips` AS TRI
INNER JOIN
`bigquery-public-data.geo_us_boundaries.zip_codes` ZIPSTART
ON ST_WITHIN(
ST_GEOGPOINT(TRI.start_station_longitude, TRI.start_station_latitude),
 ZIPSTART.zip_code_geom)
INNER JOIN
`bigquery-public-data.geo_us_boundaries.zip_codes` ZIPEND
ON ST_WITHIN(
 ST_GEOGPOINT(TRI.end_station_longitude, TRI.end_station_latitude),
ZIPEND.zip_code_geom)
INNER JOIN
 -- https://pantheon.corp.google.com/bigquery?p=bigquery-public-data&d=noaa_gsod
 `bigquery-public-data.noaa_gsod.gsod20*` AS WEA
 ON PARSE_DATE("%Y%m%d", CONCAT(WEA.year, WEA.mo, WEA.da)) = DATE(TRI.starttime)
INNER JOIN
-- Note! Add your zipcode table name, enclosed in backticks: `example_table`
`legalbi.sandbox.zipcodes` AS ZIPSTARTNAME
ON ZIPSTART.zip_code = CAST(ZIPSTARTNAME.zip AS STRING)
INNER JOIN
 -- Note! Add your zipcode table name below, enclosed in backticks: `example_table`
  `legalbi.sandbox.zipcodes` AS ZIPENDNAME
   ON ZIPEND.zip_code = CAST(ZIPENDNAME.zip AS STRING)
WHERE
-- Take the weather from one weather station
  WEA.wban = '94728' -- NEW YORK CENTRAL PARK
 -- Use data for three summer months
AND DATE(TRI.starttime) BETWEEN DATE('2015-07-01') AND DATE('2015-09-30')
```

This query results into a similar table as the previous query, except it focuses on trends from July through September. This might take a few minutes. Once we have downloaded the table, we will be ready to upload it to Tableau to create your dashboard!

CREATING OUR DASHBOARD

Previously, we had created our target tables to consolidate and store the data you pulled from the Cyclistic datasets. These tables will allow us to develop a dashboard using Tableau!

The next thing is for us to create a visualization for the Cyclistic project! we will use your project planning documents and completed target table to build a BI visualization tool.

In this activity, we created data visualizations, a low fidelity mockup to help us plan the components and layout of our dashboard, charts to be included in our visualization, and a dashboard for Cyclistic. we also completed an executive summary document that describes to Cyclistic stakeholders the business needs, project goals, dashboard functionality, and our BI methods.

Link to complete dashboard on tableau- https://public.tableau.com/app/profile/halimah5233/viz/CyclisticDashboardProject_16948792789650/CyclisticExemplar

Summer Trends

<img width="957" alt="Cyclist 1" src="https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/assets/80160857/6f7bc1a7-7290-49aa-a2d3-375d78f7c340">


The first tab of the dashboard is a map of seasonal trends of bike trips in each of the New York boroughs. The largest map shows each of the boroughs. The table compares the number of trips and average trip duration for customers and subscribers in each neighborhood. Three smaller maps focus on July, August, and September: the three months with the highest bike traffic.

This map features several filters to focus on specific bike IDs, user types, metrics, months, starting neighborhoods, and ending neighborhoods. Using any of these filters or clicking on a borough in one of the maps updates the table and maps to focus on your selection in greater detail.

Seasonality

The second tab of the dashboard focuses on seasonality, or trends throughout the year, with the Trip Totals chart and the Trip Counts by Starting Neighborhood table. 

<img width="957" alt="Cyclist 2" src="https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/assets/80160857/51b4a9f3-ee4b-49cc-bc6a-c876b5566239">


Trip Totals chart

The Trip Totals chart visualizes the total number of bike trips taken throughout 2019 and 2020, with a distinction between customers and subscribers. This chart shows that subscribers make up a significantly larger portion of Cyclistic’s users than regular customers. It also shows that there are far more users in warmer months (May–October) than there are in colder months. This makes sense considering that people are less likely to ride bicycles in colder weather.

This chart was made by putting the Start Day (aggregated by month) in the columns field, the sum of Trip Counts in the rows filed, and UserType as color assignment.

Trip Counts by Starting Neighborhood table
The Trip Counts by Starting Neighborhood table lists the total number of bike trips started in each neighborhood in each month of 2019 and 2020. It is organized by zip code, borough, and neighborhood. It also uses a color gradient to emphasize the highest and lowest counts of monthly trips. The greater the number of trips, the darker the value is in the table. It also uses light text on the darker values to ensure that the table is readable and accessible.

Because the starting location is more indicative of where users look for a bike, it is more important to emphasize starting location when determining where to advertise. The most active stations are in the Lower East Side and the Chelsea and Clinton neighborhoods. The most active months are from May to October.

This table was created by putting the Start Day dimension (aggregated by Year and Month) in the Columns field, then the Borough Start and Neighborhood Start dimensions in the Rows field. Then, the color and labels can be set by putting the sum of the Trip Count measure into the Color and Label fields.

Top Trips

The third and final tab of the dashboard is a comparison of the total number of trip minutes by starting neighborhood and ending neighborhood for both customers and subscribers. The two charts are horizontal stacked bar graphs that are ordered from highest to lowest number of minutes (between customers and subscribers combined).

<img width="957" alt="cyclist 3" src="https://github.com/QueenHalimah/Business-Intelligence-Dashboard-Cyclist-Project-/assets/80160857/17d735d3-b676-4224-8450-1f4da9c1e19e">


These charts lend insight into which locations users are most willing to travel long distances to. The charts show that the Lower East Side and Chelsea and Clinton neighborhoods have the highest total trip minutes for both start and end stations. 

To make the starting neighborhood chart, you can put the sum of Trip Minutes in the columns field, and then the Zip Code Start, Neighborhood Start, and Borough Start dimensions in the rows field. Then, set UserType as the color assignments. To make the ending neighborhood chart, complete the same steps but use the Zip Code End, Neighborhood End, and Borough End dimensions.




















