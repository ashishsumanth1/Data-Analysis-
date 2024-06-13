# Census 2021 Data Analysis

## Overview
This project analyzes the Census 2021 data to uncover insights from Education and Occupation datasets.

## Table of Contents
1. [Introduction](#introduction)
2. [Data](#Data)
3. [Methodology](#methodology)
5. [Results](#results)
6. [Conclusions](#conclusions)
7. [Installation](#installation)
8. [Usage](#usage)
9. [License](#license)

## Introduction
Census data plays a crucial role in shaping a country's infrastructure and policies, providing a comprehensive picture of the population, including demographic, economic, and social information. The 2021 Census marks a significant milestone in the history of data collection, leveraging advanced technology for digital data collection and processing to enhance accuracy and coverage.

Project Overview
This project aims to analyze the 2021 Census data to uncover insights into the employment landscape across different electoral wards. The analysis focuses on the correlation between educational qualifications and occupations, the impact of age demographics on employment rates, and the mismatch between the supply of qualified individuals and job opportunities.

### Project Aims and Objectives

#### Aim
Our primary aim in undertaking this project is to delve deep into the qualifications and occupations datasets from Census 2021 provided by the ONS. By analyzing the inherent correlations and trends between these two sets, we endeavor to:

- Analyze Qualification-Occupation Correlation: Examine how different levels of educational qualifications align with job roles, highlighting areas with significant mismatches.
- Identify outliers and their significance in the broader spectrum of the data.
- Impact of No Qualification on Employment Rates: Investigate the employment rates among individuals without formal qualifications.
- Explore the implications of qualification preferences like classroom-based education versus apprenticeship programs.
- Examine the predominant occupations inwards based on different types of qualifications.
- Assess the influence of higher education and specific occupations on employment rates in electoral wards.
- Identify potential mismatches or gaps between acquired qualifications and the jobs people eventually engage in.
- Create a machine learning model designed to predict an individual's chances of securing a job based on their qualifications and the patterns observed in the electoral ward data.

## Data
#### Data Acquisition
**Source Identification**: The foremost step involved pinpointing a reliable data source. The datasets have to be broad and relevant to the study. The Office for National Statistics (ONS) website, specifically the URL "[https://www.ons.gov.uk/](https://www.ons.gov.uk/)", was identified as a prime source due to its comprehensive nature and extensive coverage of the Census 2021 data.

#### Data Pre-processing
In this project, the data pre-processing phase was crucial to transform and prepare the datasets for subsequent analysis and model building. Below is a summary of the key steps undertaken during the data pre-processing:
1. Data Importation:

The datasets related to qualifications and occupations were imported from CSV files using Python's pandas library.

2. Data Transformation:

Pivoting Data Frames: The initial datasets were restructured into a pivot table format. This transformation allowed for more accessible representation and facilitated aggregating and comparing data across different categories and electoral wards.
Renaming Columns: Certain columns in the qualification datasets were renamed to ensure clarity and consistency. This step was essential for removing ambiguities and ensuring that the column names were succinct and self-explanatory. Unnecessary columns were removed, making the dataset more suitable for our analytical goals.

3. Data Integration:

The transformed datasets for qualifications and occupations were merged into a single dataset. This integration was based on the "Electoral wards and divisions" as the common identifier. The result was a consolidated dataset that brought together the crucial data points from both qualifications and occupations, paving the way for in-depth analyses.

## Methodology

This methodology section presents our structured approach to ensure robust and meaningful insights into achieving the project's aims and objectives.

#### Exploratory Data Analysis (EDA)
**Data Visualization**: Graphs, plots, and charts were employed to get a preliminary understanding of the data distributions, trends, and patterns.

**Statistical Analysis**: Key statistical measures were computed to understand the central tendencies, variations, and other characteristics of the data.

#### Advanced Data Analysis
**Correlation Analysis**: We extensively looked at the linear relationships between educational qualifications and occupational categories. This thorough analysis aimed to clarify the degree to which different educational backgrounds may impact or direct people towards particular professional fields.

**Cluster Analysis**: K-means clustering was employed, segmenting the data into clusters based on inherent similarities. This provided insights into how qualifications and job types naturally group together, revealing any mismatches.

### Methodology for Calculating Employment Rate
This is a key measure that gives us an idea of how many people in a particular area are working compared to those who are not. The employment rate is the ratio of the number of employed individuals to the total workforce (i.e., the sum of employed and not employed individuals). The formula we employed to determine this is:

Employmentate=(Number of Employed)/(Number of Employed+Number of Not Employed)

This method was widely used, including by respected organizations like the Office for National Statistics in 2019. This approach helps provide a clear picture of the employment situation in any given area.

### Employment-Based Ward Categorization
The methodology adopted in this study for classifying each ward into distinct categories — 'High', 'Medium', and 'Low' — is based on the employment rate of each ward. This categorization is given to the machine learning algorithm as the target feature.

#### 1. Determining the Thresholds for Categorization:
Instead of arbitrarily choosing cut-offs, we turned to statistical measures that would offer an objective way to segment the wards. Specifically, we calculated two crucial percentiles of the employment rate:
- The 33rd percentile is also known as the lower third. This value serves as the boundary between the 'Low' and 'Medium' categories.
- The 66th percentile, which is the upper third. This acts as the boundary separating the 'Medium' and 'High' categories.

#### 2. Categorizing the Wards:
With these thresholds established, we proceeded to categorize each ward based on its employment rate:
- Wards with employment rates exceeding the 66th percentile (upper threshold) were classified as 'High probability'. This suggests that a significant majority of their residents are employed.
- Wards with employment rates falling between the 33rd percentile (lower threshold) and the 66th percentile were designated as 'Medium probability'. This indicates a moderate level of employment among its residents.
- Wards that had employment rates below the 33rd percentile were labeled as 'Low probability'. These are areas that might require closer attention due to their lower employment figures.

## Results
Summarize the key findings of your analysis.
- Include images of key visualizations.
- Highlight important insights.

## Conclusions
Discuss the implications of your findings and any potential next steps.


