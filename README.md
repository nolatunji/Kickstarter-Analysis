# An Analysis of Kickstarter Campaigns
This analysis of Kickstarter campaings is aimed at uncovering and communicating the trends we found that lead to successful Kickstarter campaigns. This analysis focuses specifically on Kickstarter campaigns in the theater category.
# Kickstarting with Excel

## Overview of Project
The Kickstarter Analysis project provides insight into the outcomes of Kickstarter crowdfunding campaigns that were aimed at raising funds for theater projects. Our client Louise is a playwright who is planning to launch a new crowdfunding campaign and has asked for an analysis of campaign outcomes based on the launch date of the campaign and the goal amount. 

### Purpose
The purpose of the project is to maximize Louise's probablity of success with launching her current theater crowdfunding camapign. This will be accomplished by analyzing during which months the most successful campaigns are launched. Additionally the analysis will include insight into the funding goal amounts that have been the most successful in the past. 

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date
The first part of the analysis looked at the outcomes of past theater campaigns based on the launch date of the campaign. Campaigns that were analyzed fell into one of three outcome categories: successful, failed, or cancelled. Using a pivot table the data from the main Kickstarter worksheet was analyzed using the 'outcomes' and 'launch date' fields in a new worksheet. This data was filtered for parent category to only include campaigns that were aimed at theater projects. The PivotTable used can be viewed here: 
![Theater _Outcomes_vs_Launch](https://user-images.githubusercontent.com/96552268/148687613-fdd63ebc-474e-47c3-9154-7c170e7e7857.png)

Using the information from the PivotTable a line chart was used to visualize the Theater campaigns by outcome data. The graph can be viewed here:
![Theater_Outcomes_vs_Launch_date](https://user-images.githubusercontent.com/96552268/148686988-ebfdb7db-b22d-4b31-a1ba-d1f036555da0.png)

### Analysis of Outcomes Based on Goals
The next part of the analysis looked at the outcomes of theater campaigns based on the funding goal of the campaigns. Using the COUNTIF function in Excel the number of successful, failed, or cancelled projects were counted based on their goal amounts. The campaigns were counted and organized into twelve goal amount ranges starting from $0 to greater than $50,000. A line chart was also created for this data to assist with the visualization and analysis of the information. The Campaign Outcomes vs Goal amount line chart can be viewed here: 
![Outcomes_vs_Goals](https://user-images.githubusercontent.com/96552268/148688098-6d065ff0-0921-41ac-8928-7a8b64865132.png)

### Challenges and Difficulties Encountered
One challenge that was encountered during the analysis was in formatting the data on the 'Outcomes Based on Goals' worksheet. After creating the line chart based on the data it was noticed that parts of the line graph did not match the expected outcomes for that line graph. After reviewing the data and the cells containing the 'COUNTIF' formula, an error was detected in the 'Success' column of the table: 
 ![Outcomes Based on Goals Table](https://user-images.githubusercontent.com/96552268/148688433-094be73c-49b7-4e67-b166-3ab2c8118c8b.png)
 
In the formula that was used in cell B3 =COUNTIFS(Kickstarter!D:D, ">=1000",Kickstarter!E:E, "<=4999",Kickstarter!F:F, "successful", Kickstarter!R:R, "plays") the equal sign was placed before the greater than sign which changed the result of the formula. This formula was then copied to other cells in the column. After reviewing the formula the error was detected and corrected. 

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
- 
The analysis of Kickstarter campaign outcomes based on the launch dates revealed that most of the successful campaigns are launched in late spring through the summer months. The highest number of successful campaigns were launched in the month of May, followed by June and July with the 2nd and 3rd highest number of successful campaigns respectively. December was the month that had the lowest number of successful campaigns. Conclusions drawn from the analysis are that campaigns tend to be more successful when they are launched between the months of May thorugh July. It is not advisable to launch a campaign in December which had the lowest number of successful campaigns. 

- What can you conclude about the Outcomes based on Goals?
- When analyzing the outcomes of kickstarter campaigns based on funding goals the data tended to follow the general trend that as funding goals increased the percentage of successful campaigns decreased. 

- What are some limitations of this dataset?
-A limitiation of the analysis is within the "Outcomes by Launch Date" data. This analysis could be made stronger by adding the percentage of successful campaigns based on launch date. For instance the highest month for successful launched campaigns was the month of May but that was also the month that had the highest total campaings were launched. Therefore the high number of successful campaigns could be due to the larger number of overall campaigns launched that month. Similarly December had the lowest number of successful campaigns but also had the lowest number of total campaigns launched.
Adding the percentage to the analysis would give a clearer picture of the months with the highest probability of producing a successful campaign based on the total campaigns launched. 

- What are some other possible tables and/or graphs that we could create?
- In addition to the charts and analysis of the dataset that have already been completed, another analysis of the dataset could look at the funding goals of successful campaigns compared to the number of backers. The analysis would use the funding goal ranges used in the "Outcomes based on Goals" worksheet. We would find the average number of backers needed to acheive a successful campaign at each funding range. 
