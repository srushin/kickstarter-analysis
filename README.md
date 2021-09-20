# An Analysis of Kickstarter Campaigns.

## Overview of Project

Analysis of Kickstarter data to discover trends and generate insight into what makes a campaign successful. This project focused on Kickstarter campaigns involving theatrical plays with a fictional client Louise. Graphical representations were used to show data concerning launch dates, outcomes, and goal amounts. In this exercise, Louise has generated much of the funding for her goal in a quick amount of time and wanted to see how other campaigns for theatrical plays had faired. 

## Analysis and Challenges

The analysis for Louise was comprised of two main components: outcome of campaigns based on launch date and outcomes of campaigns based on goal amount. 

### Outcome of Campaigns Based on Launch Date

Here we were asked to create a pivot table and line chart representing the outcomes of plays only using the categories, “successful,” “failed,” and “canceled.” This was visualized over the months of the year and not by year. The biggest challenge here was getting the pivot table formatted correctly, however, it didn’t take too long. 

><img width="335" alt="Theater_Outcomes_vs_Launch_Pivot" src="https://user-images.githubusercontent.com/78064648/108111333-65562500-7049-11eb-8c85-5c6ae97095d1.png">

><img width="631" alt="Theater_Outcomes_vs_Launch" src="https://user-images.githubusercontent.com/78064648/108113098-e57d8a00-704b-11eb-9b8d-f2d5f0b03c40.png">

### Outcomes of a Campaign Based on Goals

This analysis was a bit more challenging as it required a new spread sheet and the use of the `COUNTIFS()` function, referencing other spreadsheets within the workbook. Here is a a sample of the code written to fetch the data `=COUNTIFS(Kickstarter!G:G, "successful", Kickstarter!D:D, ">=$1000", Kickstarter!R:R, "plays", Kickstarter!D:D, "<=$4999")` for the “Number Successful” column and the “$1000 to $4999” row. Total projects column data was created using the `=SUM()` function across the corresponding rows and all percentages were calculated using the mathematical formulas and cell formatting. Finalized spreadsheet below.

><img width="1112" alt="Screen Shot 2021-02-16 at 11 31 18 AM" src="https://user-images.githubusercontent.com/78064648/108112668-46f12900-704b-11eb-8a2e-07c88ecb7334.png">

Next, a line chart was created to communicate the data visually. 
><img width="1113" alt="Outcomes_VS_Goals" src="https://user-images.githubusercontent.com/78064648/108113276-2c6b7f80-704c-11eb-84f7-03f4703218e1.png">

### Other Results

The way this was challenge was structured, we failed to gain insight into the true correlation between outcome based on goals and launch date. This was due to the fact that we allowed the launch data to include all Kickstarter campaigns within the “Theater” parent category. This is visualized in the amount of cancelled (albeit small) campaigns in the launch data and the absence of cancelled campaigns in the goals data. It would be more helpful to show a visualization of launch data restricted to plays only (see below graph for plays only data).

> <img width="641" alt="plays_only" src="https://user-images.githubusercontent.com/78064648/108116312-3d1df480-7050-11eb-818b-becd1553b427.png">

We could have also seen some other information about the theatrical subcategories that worked and didn’t work, as well as,the subject of the plays themselves (ie: genres, periods, cast size, etc..). It may have given greater insight as to which were the most successful.

  
