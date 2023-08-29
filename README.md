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

The cleaning process began by creating a new column in the Geo Data sheet to rewrite the Client ID to be the same format as the one from the volume sheet.  I was then able to use an `XLOOKUP` in Volume Data to match a Geo ID to each Client ID.  From there, I created a side table for the four Geo IDs and used a `SUMIFS` to gather volume totals.  Based on the information based on the email, I was able to determine each regions Geo ID.  Next, I created a column in Volume Data for region name and used `VLOOKUP` to fill it.  Lastly, I made a separate table to store the date ranges for each quarter by year and used another `VLOOKUP` to add that information to the Volume Data table.

The final Volume Data table looked like this:
|CLID|Date|Vol|Xlookup Region ID|Region Name|Quarter|
|---|---|---|---|---|---|
|CL11420|3/31/20|884|GEO1004|LATAM|Q1 2020|
|CL11420|4/30/20|886|GEO1004|LATAM|Q2 2020|
|CL11420|5/31/20|968|GEO1004|LATAM|Q2 2020|


The final Geo Data sheet looked like this:
|CLID|GEOID|Right|Region|
|---|---|---|---|
|C-CL69323|GEO1001|CL69323|NAM|
|C-CL97995|GEO1001|CL97995|NAM|
|C-CL87299|GEO1003|CL87299|EMEA|


## Analysis

## Presenting
