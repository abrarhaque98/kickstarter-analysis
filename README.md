# Kickstarter-Analysis
### Project Overview

>The purpose of this analysis was to organize, sort, and analyze the crowd funding data to determine how other campaigns performed in relation to Louise's play "Fever", based on launch dates and funding goals. The dataset contains kickstarter data from other campaigns involving various variables such as category, goals, pledged funds, launch dates, deadlines, etc. The analysis and visualization were performed through excel, found at https://github.com/abrarhaque98/kickstarter-analysis-Module-1/blob/main/Kickstarter_Challenge.xlsx.xlsx

### Analysis and Challenges

> ##### **Initial Analysis**
> The initial analysis was to visualize the outcomes of other campaigns by their launch date. To begin the launch date data was provided in epoch timestamps so it had to be converted into standard human readable dates. For example if if Cell J1 read 1434931811 the conversion to a readable timestamp would be =(((J2/60)/60)/24)+DATE(1970,1,1). To extract the year the year function was used on the resulting readable timestamp. 
> Next the data was ready to be sorted into a pivot table as displayed below, the data was filtered to only include campaigns with the parent category of theater and by year. Further more the pivot table was viewed as months of the year by outcomes (successful, failed, and canceled). The counts of the outcomes in each month of the year was then displayed.
> 
>![image](https://user-images.githubusercontent.com/85713568/131398225-78ccb86c-33ec-4e1f-a319-f8876ff4562b.png)

> A Line chart with markers was created to visualize the data in the pivot table as shown below. 
> 
> ![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/85713568/131399752-e87a1d78-a468-45c3-b36c-d7f9f00fafb4.png)

>##### **Second Analysis**
>The next analysis was done to analyze the outcomes based on the funding goals of other plays. To begin the number of successful, canceled, and failed projects were counted against several different goal values. The function for counting the number of successful plays with a goal under 100 would look like =COUNTIFS('Data '!R:R,"plays",'Data '!D:D,"<1000",'Data '!F:F,"successful"). This was performed for all the listed goal values and outcomes. Then the percentage of each outcome was weighted against the total number of projects for plays, and visualized by a line graph denoting the percentage of outcomes across the various goal ranges.
>
>![image](https://user-images.githubusercontent.com/85713568/131399938-e57e9607-aeaa-47eb-a5f7-66fd0bb64f27.png)
>
>![Outcomes_vs_Goals](https://user-images.githubusercontent.com/85713568/131399987-40cdd7c7-2a9f-4286-b6ba-59841f4414b5.png)

>##### **Challenges**
>Some challenges were encountered throughout the analysis, the first being the epoch date to human readable date conversion, to address the issue a careful conversion of epoch date to a readable timestamp had to be undergone. Another difficulty encountered was for the second analysis when performing the countif functions. The countif functions had to be written in such a way where it would only count the data if it included the play subset and not just all campaign subsets so additional formatting was required. To adjust the counts in order to only count the plays the countif function contained 'Data '!R:R,"plays" as the condition necessary to sort for only plays. 


### Results 

> With the visualization of the Theater Outcomes by Launch Date and Outcomes based on Goals some conclusions can be made. For the first analysis, it appears that the greatest absolute number of successful theater outcomes were launched in the month of May with the number slowly decreasing throughout the year. So based of this chart someone wanting to launch their campaign in theater may want to wait until May. From the chart it also seems that the lowest amount of successful theater outcomes was in December so to avoid a failed project someone would avoid launching their campaign in December.
> 
> In the Outcomes Based on Goals chart the percentage of successful campaigns is at its peak when the goal is under 1,000 with the next peak at 1,000 to 4,999 with the second largest peak plataeuing from 35,000 to 45,000. Campaigns with a goal above 45,000 seem to have a low rate of success under 20%. When it comes to setting a goal for a project a person looking to launch a campaign under the play subcategory may want to keep their goals under 5,000 or between 35,000 to 45,000.
>
> The dataset does contain limitations, for example the comparison in the first analysis was between the parent category theater while the second analysis became more niche and focused on plays, to avoid this one type of category whether it be a general parent category or specific subcategory should have been used for consistency amongst both analysis. The data also does not compare the duration of each campaign which would have an impact on how long people would be allowed to pledge. 
> 
> Additional graphs that can be included could be the percentage of outcomes vs launch date because the original analysis only works in absolute numbers and does not factor in the difference between outcomes. Another graph to include would be an outcome by duration of campaign to visualize whether or not campaign length had an effect on the outcome.
