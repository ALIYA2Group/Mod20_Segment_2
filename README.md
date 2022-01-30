![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/Header.jpg)

# Arctic Sea Ice Extent - When will it disappear?

[Link to Project Presentation](https://docs.google.com/presentation/d/1ZF7Va3-mu2PNQNj-G3G72x1l8h4IogPnJsUgIxgYmI0/edit#slide=id.p1)


## Github - [Link to Github Repository for Segment 2](https://github.com/ALIYA2Group/Mod20_Segment_2)

Individual Branches:
There is one branch for each team member as follows:
![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/Branches.PNG)

* Each team member has at least four commits for the duration of the second segment:

## Communication Protocols

![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/Communication.PNG)

## Selected Topic

As a region, the Arctic is showing more dramatic signs of climate change than any other part of the planet. These include a warming of air temperatures at a rate two to three times greater than the rest of the planet, and the loss of September sea ice extent at a rate of 13 percent per decade.

![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/seaice.png)

Predicting when polar ice will be gone in the Artic and Antarctic using other scienctic features of global climate change by creating a database, ETL and Machine Learning Model.
Polar Sea ice, found only in the Arctic and Antarctic is comprised of frozen ocean water. The amount of sea ice at each pole changes throughout the year, growing and shrinking. We will analyse data from sources from 2003 to 2020. Sea ice has an impact on the global climate from helping to regulate global temperature to affecting ocean currents and providing a habitat for wildlife. 

## Why was this topic selected?

* Topic excited the team and feels relevant to the current climate change situation
* Opportunity to use new techniques like time-series forecasting, not covered in class modules

## Technologies / Tools Used

![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/technology.jpg)

## Data Exploration Phase (ETL) & Database

Data exploration phase consisted of identifying the factors/features that contribute to the sea ice extent (target) using sources such as global climate reporting agencies, NASA and Google Earth.

* National Snow and Ice Data Center	http://nsidc.org/data/
  * The daily Sea Ice Index provides a quick look at Arctic-wide changes in sea ice.
  * The daily Sea Ice Index provides a quick look at Antarctic-wide changes in sea
  
* Visualize Arctic and Antarctic Sea Ice https://livingatlas.arcgis.com/sea-ice/

* Climate Data Store https://cds.climate.copernicus.eu/cdsapp#!/search?type=dataset

THE ETL process consisted of downloading large datasets in .nc format and subsequently using google colab, cdsapi and terality libraries to import the data into python.
After cleaning and transforming the data to make it consistent across the datasets and merging into the final dataset, we used postgres and hosted it using AWS.

## Data Analysis Phase

We used pandas (plot features) to determine the relationship between the target and features to assess correlation and evolution over time.

![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/features.png)

## Machine Learning Model - Supervised Time-Series Machine Learning Model (Regression)

### METHOD 1: using vector autoregression (VAR)

* Causality testing: used granger causality test to investigate the causality between all combinations of variables in the time series 

* Cointegration test: to establish the presence of a statistically significant connection between two or more time series

* Stationary test: augmented dickey-fuller test (ADF test) to check the stationary of each variable in the dataset. Where stationarity is not achieved, we used differencing and seasonal decomposition.

* Check for serial correlation of residuals (errors) using Durbin Watson statistic

![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/VARoutput.png)

### METHOD 2: Time-series forecasting using tensor flow, including convolutional and recurrent neural networks (CNN and RNN)

* Data split and normalized(scaled) and mapped distribution of features
* 
![image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/Pictures/CNNRNN.png)

# Dashboard

A blueprint for the dashboard is created and includes all of the following:

* Using JavaScript and APIs to display google earth map 
* Github deploy
* Webscrape from NASA's website to get the latest climate change news on the website
* inks to other sections for team information, dataset and code

[image](https://github.com/ALIYA2Group/Mod20_Segment_2/blob/main/seaice.html)

## Next steps for Segment 3 and 4

* Work On Dashboard To Finalize The HTML And Deploy On Github
  * Scrape From NASA Climate Website
  * Scrape To See If Animal Extinction Can Be Incorporated
  * Final Results Can Be Visualized Using Tableau

* Fix Machine Learning Model

* Update Google Slides Based On Any Changes And Updates And Formatting

## Challenges

* Data Sourcing And ETL
  * The Data Was Very Scientific In Nature so it took us a while to understand it
  * The Data Was Not Available In CSV, And Had To Be Converted From A NET CDF (.Nc) Format
  * Consistency Of Data (Uniform Dates) Across Different Time Sets

* Data Pre-processing For Time Series - Time-seriesforecasting was a new concept 

* Limitation Of Model - work in progress

## New Learnings

* How To Use Time-series Forecasting – Tools Such As ARIMA And VAR That Incorporate Autoregression And Moving Averages
* Working With non-CSV files and large data sets
* Exposure to many new tools and libraries




