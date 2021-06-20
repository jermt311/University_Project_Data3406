# Data3406 Assignment 2

## Team Contract

**Standard group meeting time:** Saturdays 3pm (unless otherwise arranged)

**Contact Details:**
- Facebook messenger between group
- Uni emails (unikeys are given in the repository members)


**Group Roles:**
- *Team Leader*: William
- *Tracker*: Serena
- *Github Manager*: Benjamin
- *Jupyter Notebook Manager*: Martin
- *Writer*: Jeremy
- *Editor*: Stanley
- *Data Collection Overseer*: Jeremy
- *Data Exploration*: Everyone
- *Ethics Manager*: Serena, Jeremy

---

## Assignment Topic: Personal Informatics

**Driving question:**

> What is the difference between the Althoff et al (2017) calculation of step counts with one that requires 10-hours of the day with steps for a small number of users?


---

## Brief Introduction to the Driving Problem

The core goal of this analysis is to consider and answer the question: What is the difference between the Althoff et. al (2017) calculation of step counts with one that requires 10-hours of the day with steps for a small number of users?

Step data was collected from a number of anonymised participants. Based on the collection device used, this data was either back-dated over a number of years or calculated for a period of approximately one week during the collection process. 

We provide multiple methods for reading in step-data counts from different sources, and then present a number of aggregation methods that may be used to account for outliers and non-adherence problems. Finally, we compare the impact of these filtering and aggregation processes on both numeric and graphical analysis of step-count data. 

All code is written in Python, and the raw data is stored in the Github repository.

---

## Table of Contents
1) Getting Started <br />
2) Data Input Notebooks<br />
3) Analysis Notebooks<br />
4) Process Notebooks<br />
5) Other Files<br />

---

### 1) Getting Started
There are a few important files to understand to get started with the project. The *Product Notebook* gives the final product of the project, which gives the ethical principles, data processing pipeline, analysis and final conclusions that answer the driving question. We also have a reflection report which elucidates the group's teamwork throughout the project.

The rest of the repository is split into *minutes*; which keeps the minutes of each team meeting, *data*; which stores the raw and cleaned versions of each participant's step data that was used in the final analysis, and *code*; which includes all the process notebooks used along the way to perform EDA or pipeline development.

All of the notebooks that are part of this respository are *Jupyter Notebooks*, with all coding written in *Python*. Jupyter Notebook is updated to version 6.1.4, which runs on Python 3.7.3. We give the versions of each package used:
- numpy>=1.18.4
- pandas>=1.1.3
- matplotlib>=3.3.2
- seaborn>=0.10.1
- statsmodels>=0.11.1
- scipy>=1.4.1
- scikit-learn>=0.23.1
- dateutil>=2.8.1
- xmltodict==0.12.0
- pmdarima>=1.7.1
- python-datetil>=2.8.1

Note that xmltodict is not included as part of the standard Anaconda suite of packages, and needs to manually installed. The repository can be found [here](https://github.com/martinblech/xmltodict), and can be installed through the Anaconda prompt window by *pip install xmltodict*.

### 2) Process Notebooks
Our process notebooks were separated into two (2) folders. <br />
1) Reading <br />
2) Processing <br />

**Reading** consists of notebooks that allow us to read the csv files of the participant step data and convert it into our desired format. Participants used three (3) different types of pedometer trackers **QS Access**, **Pacer** and **Apple Health**. as such we created three (3) methods to read these files. <br />
The notebooks in this folder that should be noted are:
- **readingPacer_V1_MG_2510.ipynb**: Reads and converts Pacer app data into the desired format
- **readingQS_V1_MG_2510.ipynb**: Reads and converts QS Access app data into the desired format
- **readingXML_V1_MG_3110.ipynb**: Reads and converts Apple Health app data into the desired format 
- **DataCleaning_V1_MG_0611.ipynb**: A compilation of the three (3) reading functions for easier use during the period of the project.<br />

**Processing** consists of notebooks that we used to create our **Step Count Methods** and **Adherence Methods** <br />

- **dailystepcount_V3_BW_20201107.ipynb**: The Pipeline functions that are used to pass our data through. This pipeline contains the adherence filter functions and step count methods.
- **adherenceComp_V1_SG_25102020.ipynb**: This sets up adherence comparisons and visualisations.

### 3) Analysis Notebooks
Our Analysis Notebooks consisted of notebooks exploring the statistical significance of our findings and data, in-depth Exploratory Data Analysis, various plots and prediction of our data based on the implementation of the various adherence filters and step count methods.

- **User_EDA_V1_MG_11112020.ipynb**: Includes some introductory EDA, various statistics of our collected participant step data and visualisation of participant step data after adherence filters have been applied.
- **seasonPlots_SG_02112020.ipynb**: A qualitative analysis by defining functions that create visualisations of various participant step data over a selected period of time (years)
- **U1_U2_Statistical_Significance_Tests_V1_WY_10112020.ipynb**: Statistical tests performed to check the validity of the data obtained from participants
- **SARIMA_Guide_JT_16112020.ipynb**: The steps that were taken to implement the (S)ARIMA prediction of time series data for the various adherence filters and step count methods. (Note, this file was used as a template for the rest of the (S)ARIMA applications as each adherence filter required different parameters to be implemented)

### 4) Process Notebook
Our **Process Notebook** incorporates all the functions, statistical analysis and visualisations that we felt were necessary to present our findings. In the process notebook, you will find the following;
- Introductory EDA
- Implementation of Adherence Filters
- Implementation of Step Count Methods
- Visualisation of Step Count Data
- Statistical Analysis
- Conclusion/ Further Work
- Discussion

### 5) Other Files
There are other non-notebook files in the repository whih will be important to understanding the project. Here we give a brief explanation of the following:
- **Ethics.md**: Gives an overview of the ethical considerations of the projects.
- **Reflection Report.pdf**: Gives a reflection on the group work and how effectively various tasks were carried out by the group.
- **Survey Questions.pdf**: Shows the formatting and questions given to participants of the study when they agreed to hand over their step data.
- **minutes**: A folder containing all of the minutes taken at each group meeting, highlighting the developmental process of this project.
