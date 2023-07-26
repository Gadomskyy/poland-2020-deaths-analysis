 ## Project Goals
The main objective of this project is to utilize and enhance proficiency in two essential data analysis libraries - Pandas and Matplotlib. 
By focusing on analyzing the deaths in Poland during the year 2020, this project aims to provide insights into the mortality patterns and trends for that period.
 
 ## Project Steps

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
We can see that the voivodeships with the highest amount of deaths per 1000 people are located mostly in central Poland and Silesia, while the Northern Poland is on the other end of the spectrum.
We can also see that for all voivedeships, the amount of deaths is higher for men than women. Łódzkie is the closest to the 50/50 split.
![deaths_scatter](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/f81f8545-31ea-4e33-8da9-c513f02e7438)
An additional analysis of correlation between number of residents in a voivodeship and number of deaths per 1000 residents has been concluded.
From the plot we can see that the size of a population is unlikely to be a deciding factor in a number of deaths. There is a negative correlation (shown thanks to the regression line) which suggests that the bigger voivodeships have on average lower death rates, but a r= -0.202 suggests that this correlation is not among leading factors


Data contains also information about death numbers for different age groups in 5 year intervals. It allows to identify and analyze the most vunerable age groups.
![deaths_per_age_plot](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/a98cb7a8-6d55-4031-85da-625fc381738f)
The trend follows a mostly linear pattern with the amount of deaths rising as the age increases. The are a few outliers to that trend, notably:
1. The 0-4 group: with the deaths amount being much higher than next few categories, the reason for that is likely an increased risk of death during the birth itself.
2. The 75-79 group: Being lower than 70-74 group, the fact for that decrease could be the expected life expectancy for men and women in Poland, being around 72 and 80 respectively. That means that a number of men are expected to die before reaching that 75-79 age on average, while women are expected on average to surpass it. 

Here is how the death counts looked like for each week for the whole population in 2020. Area in red indicates lower death count than median and the one in blue - higher.
![deaths_per_week_overall](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/557392be-36ff-4c46-b9b2-6c04df09be23)
We can see that the lowest amounts of deaths per week happened in spring and summer weeks, while the autumn and winter have on average higher amounts of deaths per week. The huge increase of deaths happening in the Q4 of 2020 is connected to reasons other than just the seasonality, most notably the Covid-19 pandemic.


On the heatmap we can see the deaths per week for all regions as well as their exact numbers. Same as in the chart above, you can notice a big increase in the last quarter of the year, after a mild summer.
![deaths_per_week_heatmap](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/8c0cdc3d-c823-4a69-afe0-996c1c5034be)
the chart lets us observe that there are no outliers in terms of particular voivodeships in regards to the amount of deaths per week for whole country. All voivodeships follow simillar tendencies as shown of the graph above, with the mildest weeks being in the middle of the year, and the highest increase happening for the last three months of the year.

### 4. Compare men and women death rates
![men_women_compare](https://github.com/Gadomskyy/poland-2020-deaths-analysis/assets/118121980/09314290-4bcc-430b-877e-8bf1333584b8)
With the higher number of men dying in 2020 it is not a surprise to see them being visibly above women death rates on the chart. It's worth noting though that there was not a single week in which the death count of women was higher then men's. The biggest difference was observed in week 44, which was also the week with the highest death count overall. However, the smallest difference was in week 14 which is not a lowest death count week - we can observe an interesting case when from week 13, the amount of men's death has fallen significantly, and the opposite has happened with women, which bridged the gap. From the chart we can see that situations like that were not common and were mostly outliers - both charts showed similar trends for most of the weeks of the year.


