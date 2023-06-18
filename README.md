# Covid-Data-Analysis-Project
This is My First project on Data analysis. In this project I learned basics of Data Analysis.

The code utilizes various Python libraries, including pandas, numpy, matplotlib.pyplot, seaborn, and plotly.express, to import, clean, analyze, and visualize the data. The datasets used for analysis are "covid_19_india.csv" and "covid_vaccine_statewise.csv."

## 1.Importing Libraries
The code begins by importing the necessary libraries for data analysis and visualization, including pandas, numpy, matplotlib.pyplot, seaborn, plotly.express, plotly.subplots, and datetime. These libraries provide powerful tools for data manipulation, numerical computations, plotting graphs, and handling date-time objects.

## 2.Loading the Data
The code uses the pandas library to read the CSV files named "covid_19_india.csv" and "covid_vaccine_statewise.csv" and assigns them to the variables "covid_df" and "vaccine_df," respectively. These datasets likely contain information about COVID-19 cases and vaccination in India, including various attributes such as dates, states, cases, and other relevant data.

## 3.Data Cleaning and Preparation
The code performs several data cleaning and preparation steps on the COVID-19 dataset ("covid_df"):
* Dropping unnecessary columns: The code drops the columns "Sno," "Time," "ConfirmedIndianNational," and "ConfirmedForeignNational" using the drop function, indicating that these columns are not required for the analysis.
* Converting date format: The code uses the pd.to_datetime function to convert the "Date" column to a datetime format, assuming it was initially in the '%Y-%m-%d' format.
* Calculating active cases: The code creates a new column called "Active_Cases" by subtracting the sum of "Cured" and "Deaths" from the "Confirmed" column. This column represents the active COVID-19 cases for each entry.
## 4. Exploratory Data Analysis and Visualization
The code utilizes various visualization techniques to explore and present insights from the COVID-19 and vaccination datasets:
* Statewise analysis:
   * The code generates a statewide summary table using pd.pivot_table and 
     calculates the recovery rate and mortality rate.
   * The statewide summary table is sorted in descending order based on the 
     "Confirmed" column.
   * A styled background gradient is applied to the statewide summary table to 
     highlight the values.
* Top 10 states with the most active cases:
   * The code creates a bar plot using sns.barplot to visualize the top 10 
     states with the highest number of active COVID-19 cases.
* Top 10 states with the most deaths:
   * The code generates a bar plot to display the top 10 states with the 
     highest number of COVID-19 deaths.
* Trend analysis for the top 5 affected states:
   * The code plots a line graph using sns.lineplot to compare the active
     COVID-19 cases over time for the top 5 affected states: Maharashtra, 
     Karnataka, Kerala, Tamil Nadu, and Uttar Pradesh.
* Vaccination analysis:
   * The code performs analysis on the vaccination dataset ("vaccine_df") and 
     cleans the data by dropping irrelevant columns.
   * A pie chart is created using px.pie to visualize the distribution of 
     vaccination between males and females.
* Top 5 and bottom 5 vaccinated states:
   * The code generates bar plots to display the top 5 and bottom 5 states in 
     terms of the total number of individuals vaccinated.
