# Cyclistic bike-share analysis- a Google Data Analytics Capstone Project (using Python & Tableau)

This project is part of the Google Data Analytics Professional Certification Course. Its purpose is to demonstrate the application of skills acquired during the course, including formulating SMART questions, employing structured thinking, managing data, cleaning data, and conducting data analysis and visualization.

The analysis of this case study will adhere to a structured methodology, following chronological phases: ask, prepare, process, analyze, share and act phase.

![bike_sharing](images/bike-sharing-4196725_1280.jpg)

## Introduction
### About the Company
Cyclistic is a bike-sharing company in Chicago, which has since expanded to include a fleet of 5,824 geotracked bicycles stationed at 692 locations across Chicago. The bikes can be unlocked at one station and returned to any other station within the network at any time. Individuals buying single-ride or full-day passes fall into the category of casual riders, while those acquiring annual memberships become recognized as Cyclistic members.

### Scenario
I am a junior data analyst working in the marketing analyst team at Cyclistic. The director of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore, my team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights, my team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives must approve your recommendations, so we must be backed up with compelling data insights and professional data visualizations.

## Phase 1: Ask
>In this phase, we will define the problem, ask SMART and effective questions and use structured thinking to communicate and manage our team and stakeholders' expectations.

### Business Task
Explore how annual members and casual riders utilize Cyclistic bikes to uncover valuable insights into their distinct preferences and patterns of usage and make data-driven strategic marketing decisions for Cyclistic.

### Stakeholders
* **Lily Moreno:** The director of marketing and your manager. Moreno is responsible for the development of campaigns and initiatives to promote the bike-share program. These may include email, social media, and other channels.
* **Cyclistic marketing analytics team:** A team of data analysts responsible for collecting, analyzing, and reporting data that helps guide Cyclistic marketing strategy. You joined this team six months ago and have been busy learning about Cyclistic’s mission and business goals and how you, as a junior data analyst, can help Cyclistic achieve them.
* **Cyclistic executive team:** The notoriously detail-oriented executive team will decide whether to approve the recommended marketing program.

## Phase 2: Prepare
>In this phase, we should grasp the process of data generation and collection, as well as recognize various data types, formats, and structures for effective utilization in data analysis. Moreover, we should ensure ethical data analysis practices and address issues of bias and credibility of the data.

### About the Dataset
The data is publicly available on an [AWS server](https://divvy-tripdata.s3.amazonaws.com/index.html). We were tasked to work with an entire year of data, so I downloaded files (CSV format) containing data from December 2022 to November 2023, one file for each month.

### Data Integrity and Credibility
The fictional company Cyclistic was created for this capstone project. The datasets are appropriate and have been made available by Motivate International Inc. under this [license](https://divvybikes.com/data-license-agreement).

A good data is ROCCC: **Reliable, Original, Comprehensive, Current, and Cited.**

**Reliable** - Despite the disclaimer of accuracy in the license agreement, the large sample size contributes to the overall reliability of the data.

**Original** - The data's originality is confirmed by its traceability to the initial data source, indicating a reliance on primary data rather than secondary or tertiary sources.

**Comprehensive** - While reviewing downloaded files, it is evident that certain fields contain no values (NULL) necessary for addressing the given business question. To enhance data comprehensiveness, I will address this issue during the data cleaning process.

**Current** - The data's relevance is maintained as it encompasses the past 12 months, ensuring its currency and alignment with current conditions.

**Cited** - Lastly, the data's credibility is bolstered by being cited, as it undergoes vetting by Motivate International Inc. and falls under its licensing agreement.

Overall, I can say that the dataset follows the **'ROCCC'** guidelines and is sufficient & valid for analysis.

### Data Structure
Each .csv file contains a table with 13 columns with varying data types as shown below. Each column stands for a field that describes how people use Cyclistic's bike-sharing service. Each row represents an observation with the details of every ride.

- ride_id = col_character(),
- rideable_type = col_character(),
- ride_id = col_character(),
- rideable_type = col_character(),
- started_at = col_datetime(format = ""),
- ended_at = col_datetime(format = ""),
- start_station_name = col_character(),
- start_station_id = col_character(),
- end_station_name = col_character(),
- end_station_id = col_character(),
- start_lat = col_double(),
- start_lng = col_double(),
- end_lat = col_double(),
- end_lng = col_double(),
- member_casual = col_character()

## Phase 3: Process 
>In this phase, we will clean and transform data while maintaining the data’s integrity. Documenting the data-cleaning process is essential to keep track of the changes made to the dataset.

I planned to use Rstudio to combine and clean the dataset. However, RStudio keeps on freezing and I can't proceed with cleaning the dataset. I switched to Python using Google Colab. You can view the Jupyter Notebook for the Process phase [here](https://github.com/ecleodominique/google_data_analytics_capstone_project/blob/main/02%2603_Prepare_and_Process.ipynb)

Here are the steps that I did during this phase
1.	Check for null and duplicates
2.	Additional columns and data transformation (change the data type, remove trailing or leading spaces, etc.)
3.	Extract data for analysis

