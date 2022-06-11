# Kickstarter Campaign Analysis

## Overview of Project
Our friend Louise wants to see how different Kickstarter campaigns fared based on the dates of launch and their funding goals.

### Purpose
Analysis to provide insight on different Kickstarter campaigns in relation to their launch dates and funding goals.

## Analysis and Challenges
We filtered the data set for only campaigns regarding theater, and plays specifically. We then performed statistical analysis to find their measures of central tendancy regarding funding goals as well as what actually ended up being pledged.

![Plays_Central_Tendancy](https://user-images.githubusercontent.com/35434608/173207797-8c01797a-b14b-44af-8194-f52236c5b9b3.png)

We found that the mean goal for failed plays was much higher than the median. This means that there is at least one campaign with an unusually high goal skewing the data to the right.

### Coding

Because of the size of the data set we relied on code to quickly count the frequency that a campaign with a goal between a certain range met that goal. For example:

``` =COUNTIFS(Kickstarter!$D:$D, ">=1000", Kickstarter!$D:$D, "<=4999", Kickstarter!$R:$R, "plays", Kickstarter!$F:$F, "successful") ```

The ```COUNTIFS()``` function will tell us how many times a campaign has met any number of criteria. In the example above it counts how many plays with a goal between $1,000 and $4,999 met their funding goal.

### Analysis of Outcomes Based on Launch Date
This graph shows the outcomes of theater campaigns based on their launch dates, with months on the horizontal axis and number of successful, failed, or canceled campaigns on the vertical axis. 

![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/35434608/173206607-a5da7d53-fcbe-466d-a764-46594ecc636a.png)

### Analysis of Outcomes Based on Goals
This graph shows the percentage of campaigns that were successful, failed, or canceled, on the vertical axis, as the funding goals increase on the horizontal axis.

![Outcomes_vs_Goals](https://user-images.githubusercontent.com/35434608/173206499-04f07a6d-b36a-4604-9a3b-07c618f416d1.png)

### Challenges and Difficulties Encountered
Being new to working with Excel took patience, it almost never responded how I would have expected it to. Studying the functions and looking at examples from the official Excel documentation helped to not just get the job done, but understand how to use these tools in new ways.

## Results

- What are two conclusions you can draw about the Outcomes based on Launch Date?
	- The month of May had the highest number of successful campaigns launched at over 1.5 times the amount of any other month.
	- The month of December had the least amount of successful campaigns.

- What can you conclude about the Outcomes based on Goals?
	- 100% of campaigns with funding goals between $45,000 and $49,999 failed while campaigns with funding goals of less than $1,000 were successful 76% of the time. In general, as the funding goals increase, the chance of them being met decreases. Although there is a spike up to 67% for campaigns with goals between $35,000 and $44,999. This tells us that there must be some reason besides higher funding goals that campaigns fail.

- What are some limitations of this dataset?
	- This dataset is limited by the fact that we have no demographic data on the patrons of these campaigns. The annual income, or the general interests of the population might give us some insight into why some campaigns do better than others. It might also give us some idea as to why there was a spike in successful campaigns around the $35,000 range, or why campaigns seem to do much better when launched in the month of May. 

- What are some other possible tables and/or graphs that we could create?
	- It might be useful to make another graph comparing the outcomes of campaigns from different categories against the outcomes from theater and plays. Maybe there is some unifying trend that is less of a mystery in another category that will let us understand our category of interest a little better. 
