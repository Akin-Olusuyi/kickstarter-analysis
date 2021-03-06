# Kickstarting with Excel

## Overview of Project
 Analyzing a data set of various fund raising campaigns and their outcomes. All campaigns have been grouped into 9 major categories.

### Purpose
The main purpose of the analysis is to look at the outcomes of the campaigns to determine if there are any correlations or trends based on lauch date and goals. 

## Analysis and Challenges
The kickstarter data was provided in a structured format, so there weren't any major clean-ups required. First step was to insert a filter on the column so it's easily to filter the data set by values in the columns. 

The main challenge I encountered was converting the values for launch date to a meaning value (i.e date format). **Every date in Excel is stored as sequential serial numbers**. By defualt, January 1,1900 is serial number 1. There is a built-in functionality in excel that one can use to easily convert numbers to date format in excel. For example, you can use the **Date()** function in excel or use the formatting tab on the home tool bar. 

In our case we had a 10 digit serial number, which i beilieve is a **Unix date format**. Unix date format consists of the number of seconds that have passed since 1-Jan-1970. Knowing that, it is just a matter of calculating how many days have passed, and then adding those days to 1-Jan-1970. Here is the formula I used to convert the numbers(secods) into proper dates: ***FLOOR(J2/60/60/24,1) + DATE(1970,1,1)***.


### Analysis of Outcomes Based on Launch Date
  ![Outcome based on Launch Date](https://github.com/Akin-Olusuyi/kickstarter-analysis/blob/main/Resources/Theater_Outcomes_vs_Launch.png)
     
### Analysis of Outcomes Based on Goals
  ![Outcomes based on Goals](https://github.com/Akin-Olusuyi/kickstarter-analysis/blob/main/Resources/Outcomes_vs_Goals.png) 



## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
   - Overall, there were more successful campaigns each month over the years compared to failed or  cancelled campaigns. Note this is for the thearter catgory. 

   - Campaigns run in the summer (April - August) have been more successful. You can visual this in the "outcomes by lauch date" graph. The distance (spread)      between the successful line and failed line is larger between April to August. 

- What can you conclude about the Outcomes based on Goals?
    - From the Outcomes vs Goals chart, one can conclude that the lower the goal(amount to raised) the higher probability of having a successful campaign. The inverse holds true for failed campaigns. The higher the goal, the higher the probability of it been a failed campaign. 

- What are some limitations of this dataset?
   - Nothing tells us how the campaigns were marketed or advertised or how much was spent on marketing the campaigns. This could be a significant factor in the outcome of each campaign. One will expect a campaign that spends xxxx amount of dollars on ads or marketing to be more successful than an identical campaign with no significant outlay to marketing or ads. 

- What are some other possible tables and/or graphs that we could create?
   - Outcomes by geographical locations
   - Outcomes based on length of campaings
   - Outcomes based on the number of backers (ranges)
  
