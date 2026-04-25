# Los Angeles Crime Analysis Project

![Los Angeles](https://img.shields.io/badge/City-Los%20Angeles-blue?style=flat-square) ![Data Source](https://img.shields.io/badge/Data-LAPD%20Open%20Data-orange?style=flat-square)

## Project Overview
This project focuses on identifying patterns in criminal behavior across Los Angeles to assist the Los Angeles Police Department (LAPD) in effective resource allocation. By analyzing historical crime data, the project uncovers insights related to the timing, location, and demographic distribution of various offenses.

## The Dataset
The analysis utilizes a modified version of publicly available crime data from **Los Angeles Open Data**. The dataset includes approximately 185,715 records with 12 key features:

* **DR_NO**: Official file number (Division of Records Number).
* **Date Rptd**: The date the crime was reported.
* **DATE OCC**: The date the crime occurred.
* **TIME OCC**: Time of occurrence in 24-hour military format.
* **AREA NAME**: One of 21 geographic patrol divisions (e.g., Hollywood, Southwest).
* **Crm Cd Desc**: Description of the crime committed.
* **Vict Age / Sex / Descent**: Demographic information about the victim.
* **Weapon Desc**: Description of the weapon used, if applicable.
* **Status Desc**: Current status of the crime (e.g., Investigation Continued).
* **LOCATION**: Street address of the incident.

## Analysis Workflow
The analysis is conducted in a structured Python notebook (`Crimes.ipynb`) involving the following stages:

1.  **Data Integrity & Cleaning**:
    * **Missing Value Handling**: Identification of optional or poorly recorded fields. Specifically, missing values in `Weapon Desc`, `Vict Descent`, and `Vict Sex` were filled with "Unknown".
    * **Duplicate Removal**: Verification that no duplicate records exist in the dataset.
    * **Standardization**: Cleaning column names by converting them to lowercase, stripping whitespace, and replacing spaces with underscores.
2.  **Exploratory Data Analysis (EDA)**:
    * **Demographic Analysis**: Investigation into victim age groups, revealing that crimes mainly affect working-age adults rather than the very young or elderly.
    * **Temporal Patterns**: Analysis of monthly crime frequency, which identified a significant spike in crimes during the month of **June**.
3.  **Insights & Planning**:
    * Identification of common urban incidents such as assault, theft, and non-violent financial crimes.
    * Providing a foundation for LAPD to plan prevention strategies based on predictable crime patterns.

## Key Findings
* **Seasonality**: June shows a notable increase in crime occurrences.
* **Target Demographics**: Working-age adults are the most frequent victims in the recorded data.
* **Predictability**: Crime patterns in LA are influenced significantly by time, location, and demographics, making them partially predictable for strategic planning.

## Technical Requirements
To run the analysis notebook, the following Python libraries are required:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
