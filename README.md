﻿## Project Steps

### 1. Data Acquisition
 Obtained the death count data for the year 2020 from https://stat.gov.pl/obszary-tematyczne/ludnosc/ludnosc/zgony-wedlug-tygodni,39,2.html
 Dataset includes relevant attributes such as age, gender and geographic information.
 Additional dataset about death cause has been generated from https://bdl.stat.gov.pl/bdl/dane/podgrup/temat "Zgony wg przyczyn"


### 2. Data Preprocessing
 Cleaned and preprocessed the data. Performed data wrangling tasks, such as data type conversions and merging relevant datasets if needed, to ensure the data is in a suitable format for analysis.
 Merged the "Warszawski stołeczny" (city of Warsaw) and "Mazowiecki regionalny" (Masovian voivodeship without Warsaw) into one region for data uniformity.
 
### 3. Exploratory Data Analysis
 Found and noted basic statistics of the death count data, such as mean, median, standard deviation, minimum, and maximum values for different regions and age groups.
 Additional data regarding the each voivedeship population has been accesed in order to relate the amount of deaths in regards to the total population.
 That data has been found in stat.gov.pl "Ludność wg miejsca zamieszkania i płci w podziale na miasto i wieś". Next the death ratio per 1000 people has been calculated.

 For the whole population in all age groups and regions, 485 604 people have died, which averages to 9162,34 per week or 12,05 deaths per 1000 people.
 Median deaths per week is 8184. Maximum amount of deaths per week is 16244 (T45) and minimum - 7309 (T28)

 The voivodeship with the highest total amount as well as the highest maximum and minimum value was Mazowieckie voivodeship, which is not surprising due to the fact
 that it has the highest poplation (5 517 616). If we take that fact into consideration, the voivodeship with the highest amount of death per 1000 people is Łódzkie (15,09), 
 followed by Świętokrzyskie (14,61) and Śląskie (13,83). Pomorskie has the lowest number in that statistic with 11,08 deaths per 1000 people.


Total deaths per voivodeship and deaths per 1000 people per voivodeship. Plots have been created using Python (pandas and matplotlib)
![totalDeathsBarCharts](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/b8277cb9-e83b-4997-9109-fd17f02c43e6)
Cartogram plus diagrams for deaths per 1000 people per region plus a male/female death ratio
![Deaths_per_region](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/a3296e65-51d8-4e4e-a44d-5d600d99e4a1)




Data contains also information about death numbers for different age groups in 5 year intervals. It allows to identify and analyze the most vunerable age groups.
![deaths_per_age_plot](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/a98cb7a8-6d55-4031-85da-625fc381738f)

Here is how the death counts looked like for each week for the whole population in 2020. Area in red indicates lower death count than median and the one in blue - higher.
![deaths_per_week_overall](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/557392be-36ff-4c46-b9b2-6c04df09be23)
On the heatmap we can see the deaths per week for all regions as well as their exact numbers. Same as in the chart above, you can notice a big increase in the last quarter of the year, after a mild summer.
![deaths_per_week_heatmap](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/8c0cdc3d-c823-4a69-afe0-996c1c5034be)




