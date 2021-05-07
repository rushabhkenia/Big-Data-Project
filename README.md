# Big-Data-Project

Please refer the steps to reproduce in the report uploaded for a better understanding of how to  run the code and what datasets to use.

### Abstract
Monitoring the gun violence activities in NYC is the main problem
that will be assessed in the project. We will draw out conclusions
taking the impact of the pandemic into account as well as the historic
data. Also, we are going to take into considerations various
other factors such as socio-economic impact an area has on such
incidents, jurisdiction, time of occurrence of such events, perpetrator
background, etc. to list a few. Another important factor we will
be examining is the impact of occurrence of such events before and
after the Covid-19 pandemic to answer a few questions like if there
is a decrease in the count of such incidents or did it increase? are
there any other factors contributing to the growth or decline in gun
violence? We propose to study the occurrence and trends of such
activities over the period of 2006 to 2020 in New York City but on a
more detailed level to understand what is the most common time
or location of such activities and which people are involved keeping
into mind a variety of factors such as socio-economic impact,
income groups, age groups, gender, race etc.

### 1. Data Collection: 
Data acquisition is the process of gathering data. We have kept in
mind the four V’s of Big Data during this whole process: Volume,
Variety, Velocity and Value. All the data sets used in this projects
were acquired from different sources:
- [NYPD Shooting Incident Data (Historic)](https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Historic-/833y-fsy8)
- [NYPD Shooting Incident Data (Year To Date)](https://data.cityofnewyork.us/Public-Safety/NYPD-Shooting-Incident-Data-Year-To-Date-/5ucz-vwe8)
- [Median Incomes](https://data.cccnewyork.org/data/table/66/median-incomes#66/107/62/a/a)
- [Historical NYC labor force participation data](https://dol.ny.gov/labor-statistics-new-york-city-region#:~:text=The%20city’s%20seasonally%20adjusted%20unemployment,8.5%20percent%20in%20March%202021.)
- [NYC geojson for drawing maps](https://data.beta.nyc/dataset/nyc-zip-code-tabulation-areas)


### 2. Data Cleaning: 
Data cleansing or data cleaning is the process of detecting and correcting
(or removing) corrupt or inaccurate records from a record
set, table, or database and refers to identifying incomplete, incorrect,
inaccurate or irrelevant parts of the data and then replacing,
modifying, or deleting the dirty or coarse data.
- Zip codes and reverse geocoding: Both 2020 and historic
data with zip codes were processed using Openrefine. The
process included deleting unused data and fixing bad data
from reverse geocoding. Around 20 bad return data were
verified with Google Maps and changed manually in Openrefine.
The steps are described in openrefine_zipcode.json.
2020_result.csv was then joined with 2020 shooting incidents
data to produce 2020_incident_with_zipcode.csv. historic_
result.csv was joined together with historic data to produce
historic_incident_with_zipcode.csv. Join_zipcode.py
was used for the joining operations.
- Data sets 1 and 2 :
After successfully, acquiring the data set, we found that
the it had inconsistent but necessary data, which would
be required for the analysis. This process is crucial and emphasized
because wrong or inconsistent data can drive an
analysis to wrong decisions, conclusions, and poor analysis,
especially if the huge quantities of big data are into the picture.
Thus, first we checked for any duplicate entries in the data
set. We removed all the duplicate entries and made the data
consistent.Next, we checked for the missing values in the data set. To
our surprise a lot of data was missing but cannot be ignored
as in such cases sometimes the perpretators are not found or
victim cannot be identified and hence, After finding missing
values in column PERP_RACE, we normalized the values by
using random function. This helped us make the data more
consistent and accurate. Similarly, we normalized the values for the below columns
too: PERP_AGE_GROUP,PERP_SEX,LOCATION_DESC,
JURISDICTION_CODE.
- Data sets 3 :
The aforementioned database was already cleaned and integrated
by CCC. No obvious error was found in the data.


### 3. Data Analysis/Visualization: 
Data analysis is a process of inspecting, transforming, and modeling
data with the goal of discovering useful information, informing
conclusions, and supporting decision-making. Once the datasets
are cleaned, it can then be analyzed. Analysts may apply a variety
of techniques, referred to as exploratory data analysis, to begin
understanding the messages contained within the obtained data.
The process of data exploration may result in additional data cleaning
or additional requests for data; thus, the initialization of the
iterative phases may be required. Descriptive statistics, such as,
the average or median, can be generated to aid in understanding
the data. Data visualization is also a technique used, in which the
analyst is able to examine the data in a graphical format in order to
obtain additional insights, regarding the messages within the data.
The main strategy for analysis and visualization was to compare
the count of such occurrences with respect to various locations in
New York City area over the years keeping into account various
factors such as age, sex, race etc. of an individual involved. We did
our analysis using Jupyter and Google Colab notebooks by creating
various kinds of visualizations. For this we used Numpy, Pandas,
Geopandas, Matplotlib, Plotly and Seaborn.
We started our data analysis by using various visualizations such
as bar graph, maps , pie-chart, line-chart, to give a better understanding
of the data which we used. We compared



