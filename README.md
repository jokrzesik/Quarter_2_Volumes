# Quarter 2 Volumes Overview - *Excel Project*
## The Data
The data for this project was downloaded off of [TMB Analytics](https://www.tmbanalytics.com/excel-for-analytics) website. The file included an Excel file with 3 sheets: sample email instructions; list of client IDs, dates, and volumes; and list of client IDs by location ID.

## Instructions
The first sheet in the file contained an email providing context for the project.
> "Hey,
> 
> The board is asking to see how volume looked in Q2. I got some data (attached), but didn’t have a chance to pull anything together and was hoping you could take a stab at it.
> 
> I think they just want to see Q2 2021 volume by region and wanted to know if everything was looking good. I think this file has what you need. I don’t remember all the region codes – I know NAM ends in 1, EMEA ends in 3 and APAC and LATAM are 2 and 4, but I don’t remember which is which. I do know LATAM has the lowest volume so just go ahead and assign that to which ever comes out lowest.
> 
> I appreciate your help!"				
Based on the email, the goal of this project is to examine the Q2 2021 volumes by region and make sure they are on track compared to other quarters or years.  This project would also involve some cleaning since part of the email includes matching regions to their specific code. 

## Cleaning
The file had two sheets of data.  The first (Volume Data) contained 908 rows that looked like this:  
|CLID|Date|Vol|
| --- | --- | --- |
|CL11420|03/31/2020|884|
||04/30/2020|886|
||05/31/2020|968|

The second sheet (Geo Data) had 54 rows of:
|CLID|GEOID|
|---|---|
|C-CL69323|GEO1001|
|C-CL97995|GEO1001|
|C-CL87299|GEO1003|

The cleaning process began by creating a new column in the Geo Data sheet to rewrite the client ID to match the one from the volume sheet.  

## Analysis

## Presenting
