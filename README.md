# PyBer_Analysis
## Module 5 

It would be foolish to start messing around with such a large dataset without knowing exactly what you're trying to get out of it. So you and Omar have a head-to-head to clarify the process and outcomes for this project. You come up with the following list of steps and deliverables:

Import your data into a Pandas DataFrame.
Merge your DataFrames.
Create a bubble chart that showcases the average fare versus the total number of rides with bubble size based on the total number of drivers for each city type, including urban, suburban, and rural.
Determine the mean, median, and mode for the following:
The total number of rides for each city type.
The average fares for each city type.
The total number of drivers for each city type.
Create box-and-whisker plots that visualize each of the following to determine if there are any outliers:
The number of rides for each city type.
The fares for each city type.
The number of drivers for each city type.
Create a pie chart that visualizes each of the following data for each city type:
The percent of total fares.
The percent of total rides.
The percent of total drivers.
Omar has approved the project scope. It's time to get to work!


## Module 5 Challenge

### Background
V. Isualize has given you and Omar a brand-new assignment. Using your Python skills and knowledge of Pandas, you’ll create a summary DataFrame of the ride-sharing data by city type. Then, using Pandas and Matplotlib, you’ll create a multiple-line graph that shows the total weekly fares for each city type. Finally, you’ll submit a written report that summarizes how the data differs by city type and how those differences can be used by decision-makers at PyBer.

What You're Creating
This new assignment consists of two technical analysis deliverables and a written report to present your results. You will submit the following:

Deliverable 1: A ride-sharing summary DataFrame by city type
Deliverable 2: A multiple-line chart of total fares for each city type
Deliverable 3: A written report for the PyBer analysis (README.md)

Deliverable 1: A ride-sharing summary DataFrame by city type (35 points)
Deliverable 1 Instructions
Using the Pandas groupby() function with the count() and sum() methods on PyBer DataFrame columns, get the total number of rides, total number of drivers, and the total fares for each city type. Then, calculate the average fare per ride and average fare per driver for each city type. Finally, add this data to a new DataFrame, then format the columns.

Download the PyBer_Challenge_starter_code.ipynb file into your PyBer_Analysis folder and rename it PyBer_Challenge.ipynb.
Use the step-by-step instructions below to add code where indicated by the numbered comments in the starter code file.
In Step 1, use the groupby() function to create a Series of data that has the type of city as the index, then apply the count() method to the "ride_id" column.
In Step 2, use the groupby() function to create a Series of data that has the type of city as the index, then apply the sum() method to the "driver_count" column.
In Step 3, use the groupby() function to create a Series of data that has the type of city as the index, then apply the sum() method to the "fare" column.
In Step 4, calculate the average fare per ride by city type by dividing the sum of all the fares by the total rides.
In Step 5, calculate the average fare per driver by city type by dividing the sum of all the fares by the total drivers.
In Step 6, create a PyBer summary DataFrame with all the data gathered from Steps 1-5, using the column names shown below:.
In Step 7, use the provided code snippet to remove the index name ("type") from the PyBer summary DataFrame.
In Step 8, format the columns of the Pyber summary DataFrame to look like this:

Deliverable 1 Requirements
You will earn a perfect score for Deliverable 1 by completing all requirements below:

The total number of rides for each city type is retrieved. (5 pt)
The total number of drivers for each city type is retrieved. (5 pt)
​The sum of the fares for each city type is retrieved. (5 pt)
​The average fare per ride for each city type is calculated. (5 pt)
The average fare per driver for each city type is calculated. (5 pt)
A PyBer summary DataFrame is created. (5 pt)
The PyBer summary DataFrame is formatted as shown in the example. (5 pt)

Deliverable 2: A multiple-line chart of total fares for each city type (45 points)
Deliverable 2 Instructions
Using your Pandas skills and two new functions, pivot() andresample(), create a multiple-line graph that shows the total fares for each week by city type.

Use the step-by-step instructions below to add code where indicated by the numbered comments in the starter code file:

In Step 9, create a new DataFrame with multiple indices using the groupby() function on the "type" and "date" columns of the pyber_data_df DataFrame, then apply the sum() method on the "fare" column to show the total fare amount for each date.

In Step 10, use the provided code snippet to reset the index. This is needed to use the pivot() function in Step 11.

In Step 11, use the pivot() function to convert the DataFrame from Step 10 so that the index is the "date," each column is a city "type," and the values are the "fare."

After this step, you’ll see that each cell has the total fare for the date and time, as shown in the following image.
Note: In cells where there is no fare to be summed for that row, the cell will be filled with NaNs.

In Step 12, create a new DataFrame by using the loc method on the following date range: 2019-01-01 through 2019-04-29.
In Step 13, use the provided code snippet to reset the index of the DataFrame from Step 12 to a datetime data type. This is necessary to use the resample() method in Step 15.
In Step 14, use the provided code snippet, df.info(), to check that the "date" is a datetime data type.
In Step 15, create a new DataFrame by applying the resample() function to the DataFrame you modified in Step 13. Resample the data in weekly bins, then apply the sum() method to get the total fares for each week.

Finally, in Step 16, graph the resampled DataFrame from Step 15 using the object-oriented interface method and the df.plot() method, as well as the Matplotlib "fivethirtyeight" graph style code snippet provided in the starter code. Annotate the y-axis label and the title, then use the appropriate code to save the figure as PyBer_fare_summary.png in your "analysis" folder.

Confirm that your multiple-line chart looks like the following image, where each week is a peak or dip in the line graphs.


Deliverable 2 Requirements
You will earn a perfect score for Deliverable 2 by completing all requirements below:

A DataFrame was created using the groupby() function on the "type" and "date" columns, and the sum() method is applied on the "fare" column to show the total fare amount for each date and time. (10 pt)
A DataFrame was created using the pivot() function where the index is the "date," the columns are the city "type," and the values are the "fare." (10 pt)
A DataFrame was created using the loc method on the date range: 2019-01-01 through 2019-04-29. (5 pt)
A DataFrame was created using the resample() function in weekly bins and shows the sum of the fares for each week. (10 pt)
An annotated chart showing the total fares by city type is created and saved to the "analysis" folder. (10 pt)
Deliverable 3: A written report for the PyBer analysis (20 points)
Deliverable 3 Instructions
Use your repository README file to write your analysis of how to address any disparities in the ride-sharing data among the city types.

The analysis should contain the following:

Overview of the analysis: Explain the purpose of the new analysis.
Results: Using images from the summary DataFrame and multiple-line chart, describe the differences in ride-sharing data among the different city types.
Summary: Based on the results, provide three business recommendations to the CEO for addressing any disparities among the city types.
Deliverable 3 Requirements
Structure, Organization, and Formatting (6 points)
The written analysis has the following structure, organization, and formatting:

There is a title, and there are multiple sections. (2 pt)
Each section has a heading and subheading. (2 pt)
Links to images are working and displayed correctly. (2 pt)
Analysis (14 points)
The written analysis has the following:

Overview of the analysis:

The purpose of the new analysis is well defined. (3 pt)
Results:

There is a description of the differences in ride-sharing data among the different city types. Ride-sharing data include the total rides, total drivers, total fares, average fare per ride and driver, and total fare by city type. (7 pt)
Summary:

There is a statement summarizing three business recommendations to the CEO for addressing any disparities among the city types. (4 pt)
Submission
Once you’re ready to submit, make sure to check your work against the rubric to ensure you are meeting the requirements for this Challenge one final time. It’s easy to overlook items when you’re in the zone!

As a reminder, the deliverables for this Challenge are as follows:

Deliverable 1: A ride-sharing summary DataFrame by city type.
Deliverable 2: A multiple-line chart of total fares for each city type.
Deliverable 3: A written report for the PyBer analysis (README.md).
Upload the following to your PyBer_Analysis GitHub repository:

The PyBer_Challenge.ipynb file.
The results need to be kept populated in the PyBer_Challenge.ipynb file. Do not clear the output from the PyBer_Challenge.ipynb file before uploading to GitHub.
The “Resources” folder with the city_data.csv and ride_data.csv files.
The “analysis” folder with the PyBer_fare_summary.png.
An updated README.md that has your written analysis.

