# CASE STUDY: Bellabeat Fitness Data Analysis 
##### Author: Bronson wardle 

##### Date:

##### Sheets docs go here. 

##### 

#

_The case study follows the six step data analysis process:_

###  [Ask](#1-ask)
###  [Prepare](#2-prepare)
###  [Process](#3-process)
###  [Analyze](#4-analyze)
###  [Share](#5-share)
###  [Act](#6-act)

## Scenario
Since it was founded in 2013, Bellabeat has grown rapidly and quickly positioned itself as a tech-driven wellness company for women. The company has 5 focus products: bellabeat app, leaf, time, spring and bellabeat membership. Bellabeat is a successful small company, but they have the potential to become a larger player in the global smart device market. Our team have been asked to analyze smart device data to gain insight into how consumers are using their smart devices. The insights we discover will then help guide marketing strategy for the company. 

## 1. Ask
💡 **BUSINESS TASK: Analyze Fitbit data to gain insight and help guide marketing strategy for Bellabeat to grow as a global player.**

Primary stakeholders: Urška Sršen and Sando Mur, executive team members.

Secondary stakeholders: Bellabeat marketing analytics team.

## 2. Prepare 
Data Source: 30 participants FitBit Fitness Tracker Data from Mobius: https://www.kaggle.com/arashnic/fitbit

The dataset has 18 CSV. The data also follow a ROCCC approach:

- Reliability: The data is from 30 FitBit users who consented to the submission of personal tracker data and generated by from a distributed survey via Amazon Mechanical Turk. 
- Original: The data is from 30 FitBit users who consented to the submission of personal tracker data via Amazon  Mechanical Turk.
- Comprehensive: Data minute-level output for physical activity, heart rate, and sleep monitoring. While the data tracks many factors in the user activity and sleep, but the sample size is small and most data is recorded during certain days of the week. 
- Current: Data is from March 2016 to May 2016. Data is not current so the users habit may be different now. 
- Cited: Unknown. 

  The dataset has limitations:

- Only 30 user data is available. The central limit theorem general rule of n≥30 applies and we can use the t test for statstic reference. However, a larger sample size is preferred for the analysis.
- Upon further investigation to check for unique user Id, the set has 33 user data from daily activity, 24 from sleep and only 8 from weight. There are 3 extra users and some users did not record their data for tracking daily activity and sleep. 
- For the 8 user data for weight, 5 users manually entered their weight and 3 recorded via a connected wifi device (eg: wifi scale).

## 3. Process

Observe and familarize with the data set. 
![bgfvgfd](https://github.com/user-attachments/assets/6fd986ff-7b2a-4609-9640-3eabdb14694e)
Note: This is only a screenshot of the fully cleaned daily activity data set. 

Steps took to clean the data in sheets. 

1. Combined dailyAcitivy.csv and weightloginto.csv files to gather all data into one place.
2. Checked and removed dupicates, NULL/missing values. Also cleaned up values to only have 1 decimal. 
3. Removed columns LoggedActivites, SedentaryActiveDistance, and TrackerDistance. These were removed due to either being not needed, duplicate values or all values were 0.
   - Removed unneeded columns and values as well on the weightloginfo dataset.

Data cleaning has been completed. 

## 4. Analyze 

To analyze the data in sheets, I went ahead and created a pivot table to gather SUMS and averages of the data. 
![s](https://github.com/user-attachments/assets/f69d3a99-e6e1-4c71-8ea0-9c018c00b347)
![re](https://github.com/user-attachments/assets/664a1fc7-5efb-4138-b5b2-f68a3bcb1b7d)

With doing that, I found that 81% of the time the device was used was during a sedentary moment. 
- Only 1.6% of the time was very active.
- 1% of the time was farily active.
- 15% of the time was light activity
- The average steps took a day was at 7,434. As recommended by the CDC, an adult female has to aim for at lease 10,000 steps per day to benefit from general health, weight loss and fitness improvement. Source: Medical News Today article.
- And the average calories burned was only 1600. Could not be interpreted into detail as calories burned depend on several factors such as the age, weight, daily tasks, exercise, hormones and daily calorie intake. Source: Health Line article

The data that was provided is saying that the average time the device was worn was during casual sedentary time. 


## 5. Share


![Rplot](https://github.com/user-attachments/assets/137289c8-692a-4fb0-8ca7-741281d8de53)

Note: The percentages on this chart are rounded up. 

In this pie chart, we are seeing the distrubtion between the types of activity that were logged. 
As you can see, the activity that was logged the most was sedentary. 

This indicates that users are using the FitBit app to log daily activities such as daily commute, inactive movements (moving from one spot to another) or running errands. Or in other words, casual wear. 

App is rarely being used to track fitness (ie. running) as per the minor percentage of fairly active activity (1.1%) and very active activity (1.7%). This is highly discouraging as FitBit app was developed to encourage fitness.

Next I wanted to see how many calories are being burnt per steps taken. 

![Rplot01](https://github.com/user-attachments/assets/dde375cc-881a-4596-96c5-e9a915499b5d)

As you can see in this chart, typically the more steps that were logged the more calories that were burned.
  - But there seems to be some discrepancy with the data that was provided as you can see at the bottom of the graph.
  - 1 of 2 things could cause this, 1. The tracker wasnt logging the calories burnt when the customer was wearing it 2. The tracker was picking up random motions as steps when it should'nt have. This could lead to more steps being tracked than actual. 

Next I wanted to compare how long the customers are using their watch to track their sleep. 
![Rplot02](https://github.com/user-attachments/assets/e5b74727-e1cd-43fb-9156-92d8bc167c80)

In this scatter plot, you can see that the average time spent in bed was between 400 and 600 minutes. 
This resulting more time asleep and more recovery. 



