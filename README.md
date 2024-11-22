# **ImmoData - Exploratory data analysis and visualisation**
## Table of Contents

- [Introduction](#Introduction) 
- [Project Overview](#project_overview)
- [Prerequisites](#Prerequisites)
- [Installation-Environment setup](#Installation-Environment-setup)
- [Usage](#Usage)
- [Structure](#Structure)
- [Contributors](#Contributors)

## **Introduction**

This repo contains the results of the second group project in a series aimed at completing a data science workflow from start (data collection) to finish (modelling using machine learning) during my AI and Data science bootcamp training at BeCode (Brussels, Belgium). The final goal is to create a machine learning model capable of predicting real estate prices in Belgium.

The specific aims for this project are to:
1. Use pandas and data visualization libraries (Seaborn, matplotlib)
2. Clean a dataset for analysis
3. Draw conclusions from a dataset
4. Answer supplementary questions

Specifications for the final dataset are:
- Clean data (no duplicates, no blanks, no missing values)
- Answer questions about the data
    - Number of rows and columns
    - What is the correlation between the variables and the price? And among predictors?
    - Which variables most/least affect price?
    - How many qualitative and quantitative variables are there? How would you transform these values into numerical values?
    - Percentage of missing values per column?
- Interpret the data
    - Plot the outliers
    - Which variables would you delete and why ?
    - Represent the number of properties according to their surface using a histogram.
    - In your opinion, which 5 variables are the most important and why?
    - Most and least expensive municipalities according to region (average, median, price per square meter)

My personal contributions to this project can be found in the contributors section of this README.

The repository contains multiple branches
- Main: contains the code for scraping the chosen website
- KevinDataClean: my working branch, containing in addition a jupyter notebook used for data cleaning and start of exploratory data analysis
- Other working branches for contributors


# Project Overview
This is a project done as a part of Data Science and AI course at Becode in 2024.
The mission is to to execute exploratory data analysis and visualisation of a dataset, including information about at least 10.000 properties all over Belgium. 
Main steps of the project are:
1. Cleaning of the scrapped data (handaling duplicates, missing data and outliers)
2.  Data analysis and interpretation(examination of correlation and visulization of target variable with the most correlated ones)

## **Description**
## Exploring real estate data

Following steps were taken to clean the data: 
- Duplicates handled (complete row duplicates, listings posted more than once on the website)
- Address data type constraints
- Identify patterns in missingness and address missing values with logical choices first
- Verify value constraints for categorical variables
- Remove outliers based on response variable, assuming differences in distribution for houses and apartments
- Deal with outliers in predictor space using multivariate method (DBSCAN)
- Impute remaining missing values (after outlier removal to ensure no bias introduced) using KNN

Packages used:
- pandas
- numpy
- matplotlib
- seaborn
- missingno
- sklearn

Following data cleaning, EDA was carried out according to following steps:
- Verification of distributions and relationships between numerical data variables
- Correlations between numerical variables - including response variable
- Verification of multicollinearity with **V**ariance **I**nflation **F**actor
- Attempt at dimension reduction utilising **P**rincipal **C**omponent **A**nalysis
- Identifying relationships between categorical predictors and response (Kruskal-Wallis and Mann-Whitney-U + example of post-hoc testing)
- Associations between categorical predictors (Χ squared)

Packages used:
- pandas
- numpy
- matplotlib
- seaborn
- sklearn
- scipy
- statsmodels

# Prerequisites
Make sure you have the following:

1. Python 3.x installed.
2. pip for managing Python packages.
3. for the required libraries please refer to 
    requirements.txt --- install using the command pip install -r utils/requirements.txt

   ## **Installation-Environment setup**

You can create a virtual environment for the script using venv.
```shell
python -m venv C:\path\to\new\virtual\environment
```

Or using conda.
```shell
conda create --name <my-env>
conda activate <my-env>
```

Included in the repository is a cross-platform environment.yml file, allowing to create a copy of the one used for this project. The environment name is given in the first line of the file.
```shell
conda env create -f environment.yml
conda activate wikipedia_scraper_env
conda env list #verify the environment was installed correctly
```

## **Usage**

Create a local copy of the repository by cloning and navigate to the directory using CLI. Running the following command runs the main.py script, which will scrape the real estate website search pages (for houses and apartments excluding annuity sales) for a specified number of pages. 333 pages were scraped for the project, resulting in over 15.000 listings. However, for the sake of brevity, a much smaller amount of pages is set in the code. This can be changed in the main.py file. The script will create initial URL and full URL lists, as well as export the data in csv format in the Data directory.

```shell
python main.py
```


# Usage

This script will:
1. Load a dataset previously scrapped from Immoweb
2. Cleans it in regarding duplicates, missing data and outliers
3. Investigates correlation to indicate the most important influential variables
4. Visualize the result of EDA
5. The final output could be used for analysing the housing market in Belgium using ML


# Structure
The project has the following core components:

1.
    
2. 

3. requirements.txt : contains list of dependencies for the project.

# Contributors 
This proects is done by:
1. [Kevin](https://github.com/kvnpotter)
2. [Maxim](https://github.com/MaximSchuermans)
3. [Fatemeh](https://github.com/Fatemeh992)


