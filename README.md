# Data-Visualization-Project---Python-Altair
Data Visualization on Boonsong Lekagul waterways readings using Python Altair \
This solution was submitted as part of my coursework CST4060 Visual Data Analysis 
### Problem Overview:
(All the people, places, groups, technologies, contained therein are fictitious). \
Mistford is a mid-size city to the southwest of the Boonsong Lekagul Wildlife Preserve. \
The city has a small industrial area with four light-manufacturing endeavors. \
Mistford and the wildlife preserve are struggling with the possible endangerment of the RoseCrested Blue Pipit, a locally loved bird. \
The birdʼs nesting pairs seem to have decreased alarmingly. \
An investigation last year (VAST challenge 2017) indicated that the Kasios Office Furniture, a Mistford manufacturing firm, may be linked to this. Though there is no firm evidence. \
Now the company insists that they have done nothing wrong. \
It is time for more visual analytics investigation. 
#### Dataset
Several years of water sensor readings from rivers and streams in the preserve. \
These samples were taken from different locations scattered throughout the area. \
Contain measurements of several chemicals of possible interest. 
#### Task
The task is to investigate the sensor readings to find possible link to the bird population deduction.

## Task 1: Data Quality Analysis:
### 1. Understanding Missing Values:
![missing values](https://github.com/BrammiJ/Data-Visualization-Project---Python-Altair/blob/main/visuals/missing%20values.png) 
**Findings:** In terms of missing data, it is clear from the above chart that there are some missing values in the dataset. The analysis reveals varying patterns in the presence of measures across different years. While some measures exhibit presence throughout all the years, others had zero values and only recorded in certain years. For instance, Potassium is consistently recorded from 1998 to 2016, while PCB 101 appears only in 2003, 2008, and 2009. \
**Reason for choosing this chart type:** In a bar chart, missing values can be represented by an empty bar, making them stand out distinctly. This allows viewers to immediately identify the presence of missing values without needing to interpret the data points along a continuous line. Since the goal of this task is not to identify trends across years, we do not choose line chart, bar chart is the most effective visualisation for this task. \
**Marks:** Line \
**Channels:** Vertical Position (years), Horizontal Position (measures) and Area (Empty bars for missing data) \

### 2. Understanding Collection frequency:
![collection frequency](https://github.com/BrammiJ/Data-Visualization-Project---Python-Altair/blob/main/visuals/collection%20frequency.png)  \
**Findings:** The collection frequencies range from 3 to 381 readings per month. Each location displays the frequency of sensor readings spanning from 1998 to 2016. Upon analysis of the chart, it becomes evident that three locations—**Tanasanee, Decha, and Achara**—lack readings for 10 years from 1998 to 2008. From this, we could conclude that either the **sensors malfunctioned in these locations from 1998 to 2008**, (or) the **sensors were installed in these locations only from 2009**. \
It is observed from the heatmap that the data collection frequency is higher in the middle years from **2003-2012** than in the beginning and end of the dataset. \
It is also observed that in locations Boonsri, Chai, Kannika and Sakda, the frequency of data collected is higher than in the other locations. \
This chart helped us to narrow down the locations and years for further analysis. \
**Reason for choosing chart type** Heatmaps provide a visual representation of data density or frequency across both time (years) and locations. By using colour intensity to represent the frequency of sensor readings, heatmaps allow us to easily identify temporal patterns, such as periods with higher or lower data collection, and spatial patterns, such as disparities in data availability across different locations. \
**Mark:** Grid of rectangles \
**Channels:** Colour channel to encode quantitative values  

## Task 2: Trend and Anomaly Analysis:
### TRENDS:
#### Task: Identify locations that show consistently higher or lower values over the years when compared to all the other sites
![trend 1](https://github.com/BrammiJ/Data-Visualization-Project---Python-Altair/blob/main/visuals/site%20anomalies.png) \
**Findings:** **Boonsri** exhibited consistently high trends when compared to all other locations for **Cadmium**, particularly during the period from 2004 to 2007 with the measures of Cadmium, Fecal coliforms, 'Chemical Oxygen Demand (Cr). \
Similarly, **Chai** showcased consistently higher trends in values, reaching a peak level of 350 in 2010 for the measure of **fecal coliforms**. \
However, for **chemical oxygen demand**, all locations experienced fluctuations within the same timeframe, while **Boonsri** exhibited consistently lower values when compared to other locations. \
We could conclude that these locations experienced a contamination event that led to them exhibiting trends significantly different than other locations, leading to the decrease in population of the rose-crested blue pipits. \
**Reason for choosing chart type:** Line charts proved instrumental in revealing nuanced trend patterns. We consolidated all line charts into a cohesive visual display, enhancing our ability to discern insights across the spectrum of contaminants. \
**Mark:** Line. \
**Channels:** Positions x-axis (sample date) & y-axis (values). 
####  Identify measures that show similar growth over a particular period 
![trend 2](https://github.com/BrammiJ/Data-Visualization-Project---Python-Altair/blob/main/visuals/similar%20growth%20measures.png) \
**Findings:** Our focus on the trends of two key measures, **Aluminium and Selenium**, revealed striking **similarities in growth patterns between October 2008 and April 2009** where it is observed to see a consistent growth in the mentioned timeframe. We could conclude that this could be a possible contamination event that could have lead to the decrease in population of rose-crested blue pipits. \
**Reason for choosing chart type:** Line charts proved instrumental in revealing nuanced trend patterns with contaminant values represented on the x-axis and years on the y-axis the lines illustrate the behaviour of two measures over the time. \
**Mark:** Line \
**Channels:** Positions x-axis (sample date) & y-axis (values). \
**Advanced Features:** Sort and filter measures, add tooltip for interaction. \
**Advanced Altair Features:** Selection interval and vertically concatenate line charts. 
### ANOMALIES:
**Contamination Event 1** \
![CONTAMINATION EVENT 1](https://github.com/BrammiJ/Data-Visualization-Project---Python-Altair/blob/main/visuals/contamination%201.png) \
**Findings:** During our analysis of filtered measures (iron, manganese, copper, chromium, lead, and nickel), we **observed spikes on August 15, 2003**, across multiple locations. From this, we could conclude that a contamination event could have occurred on 15th August 2003, leading to the decrease in population of the rose-crested blue pipits. \
**Reason for choosing chart type:** The line chart proves particularly valuable for comparing anomalies and determine spikes across multiple locations simultaneously. \
**Mark:** Line \
**Channels:** Positions x-axis (sample date) & y-axis (measure level) \
**Contamination Event 2**\
![contamination event 2](https://github.com/BrammiJ/Data-Visualization-Project---Python-Altair/blob/main/visuals/contamination%202.png) \
**Findings:** Each bar chart corresponds to a particular measure, with its height representing the concentration level. One commonality among all the measures in this chart is that these measures are **pesticides/insecticides**, and their presence was recorded only in the time period of **2005-2007**. \
From this, we conclude that this could be a possible contamination event occurring over the period of 3 years, which could’ve led to the decrease in population of the rose-crested blue pipits. \
**Reason for choosing chart type:** Bar chart allows to have comparisons between various categories and their respective metrics. \
**Mark:** Line \
**Channels:** Vertical Position (years), Horizontal Position (values)

### Conclusion:
1. By performing Data Quality analysis, we were able to identify the various data quality issues in the dataset and narrowed down measures, years, and locations for further analysis. 
2. By analysing the various trends and anomalies in in the dataset, we were able to identify possible contamination events that could have led to the decrease in population of the rosecrested blue pipits.
