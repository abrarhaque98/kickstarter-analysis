# Kickstarter-Analysis
### Overview of the Project

>The purpose of this analysis was to organize, sort, and analyze the crowd funding data to determine how other campaigns performed in relation to Louise's play "Fever", based on launch dates and funding goals. The dataset contains kickstarter data from other campaigns involving various variables such as category, goals, pledged funds, launch dates, deadlines, etc. The analysis and visualization were performed through excel, found at https://github.com/abrarhaque98/kickstarter-analysis-Module-1/blob/main/Kickstarter_Challenge.xlsx.xlsx

### Analysis and Challenges

> #### **Initial Analysis**
> The initial analysis was to visualize the outcomes of other campaigns by their launch date. To begin the launch date data was provided in epoch timestamps so it had to be converted into standard human readable dates. For example if if Cell J1 read 1434931811 the conversion to a readable timestamp would be =(((J2/60)/60)/24)+DATE(1970,1,1). To extract the year the year function was used on the resulting readable timestamp. 
> Next the data was ready to be sorted into a pivot table as displayed below, the data was filtered to only include campaigns with the parent category of theater and by year. Further more the pivot table was viewed as months of the year by outcomes (successful, failed, and canceled). The counts of the outcomes in each month of the year was then displayed.
![image](https://user-images.githubusercontent.com/85713568/131398225-78ccb86c-33ec-4e1f-a319-f8876ff4562b.png)
> A Line chart with markers was created to visualize the data in the pivot table as shown below. 
> ![Theater_Outcomes_vs_Launch](https://user-images.githubusercontent.com/85713568/131399752-e87a1d78-a468-45c3-b36c-d7f9f00fafb4.png)


