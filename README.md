# BELLABEAT MARKET ANALYSIS

## TABLE OF CONTENTS

- [INTRODUCTION](#introduction)
- [BUSINESS TASK](#business-task)
- [DATA SOURCES](#data-sources)
- [LICENSING AND PRIVACY OF DATA](#licensing-and-privacy-of-data)
- [DATA ORGANIZATION](#data-organization)
- [OBJECTIVES](#objectives)
- [CREDIBILITY OF THE DATASET](#credibility-of-the-dataset)
- [IMPORTING DATASETS INTO EXCEL](#importing-datasets-into-excel)
- [DATA ANALYSIS](#data-analysis)
- [CONCLUSION](#conclusion)
- [RECOMMENDATIONS](#recommendations)

## INTRODUCTION

[Bellabeat](https://bellabeat.com/) is a high-tech driven manufacturer of health-focused smart products for women, aiming to empower them with knowledge about their health and habits. It is a successful small company, and has the potential to become a larger player in the global smart device market. Their app and devices collect data on activity, sleep, stress, menstrual cycle, and mindfulness habits.
 
To unlock new growth opportunities in the global smart device market, Bellabeat aims to analyze smart device fitness data. They are keen to utilize consumer data for strategic insights and want to focus on analyzing the usage patterns of one of their products to optimize their marketing strategies: Bellabeat app.


## BUSINESS TASK

Examining user data from non-Bellabeat smart devices that track activity metrics like steps and calories burned, as well as sleeping patterns. The objective is to derive meaningful insights into user behavior and how they engage with their smart devices to monitor their activities. These insights, in the form of trends identified from the data, will be utilized to inform and shape upcoming marketing strategies.

The key stakeholders are:

- Urska Srsen – Co founder and Chief creative officer
- Sando Mur – Co founder and mathematician
- Bellabeat marketing analytics team

## DATA SOURCES

A public data set named [Fitbit fitness tracker data](https://www.kaggle.com/datasets/arashnic/fitbit) containing the personal fitness data of 30 Fitbit users, made available by [Mobius](https://www.kaggle.com/arashnic) and stored on Kaggle website.

## LICENSING AND PRIVACY OF DATA

The data has been confirmed to be open source and so can be used without asking for permission under copyright laws, the platform where the data is hosted, is recognized for its security measures and operates under appropriate licensing.

## DATA ORGANIZATION

The 18 CSV documents are available with each document representing different quantitative data tracked by Fitbit; [CLICK HERE]() to preview CSV datasets in *Bellabeat datasets.docx*.

## OBJECTIVES

Considering the datasets at my disposal, I intend to analyze user behavior primarily within daily time frames to identify overarching trends. I will concentrate on examining the *daily activity* and *sleep datasets*, sorting and filtering them using an Excel spreadsheet.

## CREDIBILITY OF THE DATASET 
The data originates from a reliable source, but it's worth noting that the sample size is quite small, comprising only 30 users over 31 days. This small sample size raises concerns about potential sampling bias. Additionally, an important caveat is the absence of any demographic information in the dataset.

## TOOLS USED
I made use of `Excel` as my primary tool for data cleaning and manipulation due to its relative ease of use and accessibility and `Tableau` for visualization.

## IMPORTING DATASETS INTO EXCEL
Importing and optimizing FitBit Fitness Tracker data sets involves the removal of redundant datasets and aggregation of essential datasets required for querying and analyzing specific information.  Considering my emphasis on identifying high-level trends in the data for analysis, I opted to import and exclusively utilize the *Dailyactivities_merged*, *SleepDay_merged* and *Hourlysteps_merged* datasets.

I created a CHANGELOG documenting my cleaning and formatting process within Excel [CLICK HERE](https://github.com/paschaldubem/Bellabeat-Market-Analysis/blob/main/BELLABEAT%20CHANGE%20LOG.pdf)

For more details on cleaning and formatting check [Bellabeat case study]() 

## DATA ANALYSIS

   - USER ID COUNT
     
When using pivot tables to go through the intended datasets to be analyzed, I discovered that although 30 user ids were the supposed ideal number of users documented, the actual user count found was slightly varied in my respective data sets; *Dailyactivity_merged* (33 users), Hourlysteps_merged* (33 users) and *Sleepday_merged* (24 users) respectively. 

This discrepancy likely arises from several factors. In the case of the *dailyactivities* and *hourlysteps* datasets, the higher-than-expected number of users (33) could be attributed to certain users utilizing multiple smart devices. On the other hand, the lower-than-expected number of users (24) in the *Sleepday* dataset may result from some users choosing not to share their activity tracking information publicly. This variance in user counts can be attributed to these specific scenarios.

## DATA VISUALIZATION IN TABLEAU

Subsequently, I imported the refined dataset into Tableau, leveraging its capabilities to craft informative and interactive visualizations and dashboards. This approach allows for a more profound comprehension of the dataset under examination

![BELLABEAT STEPS ACTIVITY DASHBOARD](https://github.com/user-attachments/assets/09b05c6e-6f63-467e-bf28-ee536d172f2a)


   - WEEKLY STEPS ACTIVITY

Utilizing the *dailyactivities_merged* dataset, I will construct a plot in tableau that visualizes the distribution of total steps per weekday. This analysis aims to provide insights into user behavior patterns regarding their smart device usage, specifically identifying the most and least active days of the week.

 ![Weekly Steps Activity](https://github.com/user-attachments/assets/a3551d03-3162-4f2f-9841-83c3d973d796)

Based on the above plot, we can observe that, on average, Tuesday emerges as the most active day, while Sunday appears to be the least active. This discrepancy is likely influenced by the fact that Sunday is typically associated with being a day of rest and so many users are likely to be at home, engaging in less physical activity. Saturday, however, ranks closely behind Tuesday, possibly due to the weekend effect where people often engage in health-focused activities like running and exercising, leading to a notable increase in their overall activity levels.  On average, weekdays exhibit higher user engagement in various activities, as reflected by their average total daily steps.

   - AVERAGE HOURLY STEPS
     
Following my data analysis, I identified Tuesdays as the most active day of the week. Now, I will delve deeper to determine, on average, the most active hours of the day for the Fitbit users.

 ![Average hourly steps](https://github.com/user-attachments/assets/fdc24329-cccb-4312-9f89-6f48e2c98e01)

The visualization provides a detailed breakdown of daily activity levels, focusing on the average steps taken by Fitbit users. It's evident that users are typically more active during daytime hours, starting from 8 a.m. and continuing until around 7 p.m. The activity levels tend to decrease after 8 p.m. On average, we observe peak activity during two distinct periods: from 12 p.m. to 2 p.m. and from 5 p.m. to 7 p.m. Interestingly, the least active time during the 24-hour period is at 3 a.m., which aligns with the common sleeping hours for most people.

   - USER SLEEP QUALITY
     
The duration of user sleep is a crucial parameter tracked by smart devices and holds a lot of significance health wise. Leveraging the available data, I constructed a visualization that provided deeper insights into user sleep patterns.

 ![Average user sleep duration](https://github.com/user-attachments/assets/749a9b62-77db-4470-ba44-38245a15211b)

The visualization above indicates a notable trend among Fitbit users, with the majority failing to attain sufficient sleep, as their average sleep durations consistently fall below the recommended daily 8-hour threshold.
he visualization above indicates a notable trend among Fitbit users, with the majority failing to attain sufficient sleep, as their average sleep durations consistently fall below the recommended daily 8-hour threshold.

- CORRELATIONS
  
I will attempt to determine if there is a relationship between steps taken by users and the number of calories burnt.

![Daily average steps and Daily average calories burnt](https://github.com/user-attachments/assets/e79c8f60-b5c2-42bb-bf62-218b7b6f10f8)


 ![Average Steps Vs Average Calories burnt](https://github.com/user-attachments/assets/edd5397d-61e6-4185-bfe8-de273a028ed0)


From the first visualization above, it's not immediately apparent how the &daily average total steps* and *daily calories* relate when considered individually. Consequently, opting for a scatter plot to underscore their connection reveals a positive correlation between these variables. This correlation arises from the fact that increased walking (total steps) is a form of physical activity, leading to a higher expenditure of calories. It's important to emphasize, however, that correlation does not imply causation, signifying that one variable is not the sole cause of changes in the other, and vice versa.

To view more interactive charts and dashboards on Tableau [CLICK HERE](https://public.tableau.com/app/profile/mgbecheta.paschal/viz/BellabeatUserAnalysis/BELLABEATSTEPSACTIVITYDASHBOARD#1).


## CONCLUSION

Based on my analysis, I've observed that users tend to be more active on weekdays compared to weekends, with Tuesdays being the peak day for activity. `Daily activity` shows peaks between 12 PM to 2 PM and 5 PM to 7 PM, while `nighttime exhibits` lower activity levels, likely indicating rest. It's worth noting that most Fitbit users do not achieve the recommended 8 hours of sleep, with a substantial number falling short of this target. Furthermore, I found a positive relationship between total steps and total calories, as calories burned is directly linked to the number of steps taken. However, it's essential to emphasize that correlation doesn't imply causation, meaning that total steps alone do not cause increased calorie burn and vice versa.

## RECOMMENDATIONS
  
My recommendation for Bellabeat is to implement improved engagement strategies to maintain user interest in their activity levels. One effective approach could involve introducing a daily steps streak system, which users can share on social media. This would not only motivate individuals to stay consistent in their physical activity but also encourage their friends and family to participate, fostering a sense of community and collective commitment to personal health.

   - `Bellabeat` should consider providing users with access to their historical activity data for informational purposes. This will empower users to take charge of their individual fitness journeys, allowing them to monitor their progress and track their improvements over time. This access to past activity data can serve as a valuable tool for users in achieving their health and fitness goals.

   - The `Bellabeat` app could enhance user experience by offering features that provide notifications to guide users on optimal bedtime preparations (wind down), ensuring they consistently achieve the recommended sleep duration. This proactive approach can contribute to better sleep habits and overall health for app users.

   - A beneficial strategy for `Bellabeat` would be to periodically deliver health tips to users, emphasizing the benefits of adhering to the daily recommended steps and sleep patterns. This serves as a gentle reminder to encourage users to make mindful decisions that contribute to their overall well-being.




























