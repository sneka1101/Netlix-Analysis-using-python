# Netflix Data Analysis Using Python

## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning/Preparation](#data-cleaningpreparation)
- [Analysis Tasks](#analysis-tasks)
  - [1. Remove Duplicate Records](#1-remove-duplicate-records)
  - [2. Check for Null Values](#2-check-for-null-values)
  - [3. Show Information for 'House of Cards'](#3-show-information-for-house-of-cards)
  - [4. Year with Highest Number of Releases](#4-year-with-highest-number-of-releases)
- [Other question](#Otherquestion)


## Project Overview
---
This project involves analyzing the Netflix dataset to perform various data cleaning and exploratory data analysis tasks. The dataset is analyzed to answer specific questions, identify and handle missing values, and visualize trends in the data.

## Data Sources
---
The primary dataset used for this analysis is a CSV file named `netflix_titles.csv`, which contains information about Netflix TV shows and movies. The columns include:

- `Show_Id`: Unique ID for each show
- `Title`: Title of the show
- `Director`: Director of the show
- `Cast`: List of cast members
- `Country`: Country of origin
- `Release_Date`: Release date
- `Rating`: Rating of the show
- `Duration`: Duration of the show
- `Listed_In`: Categories
- `Description`: Description of the show

## Tools and Technology
---
- **Python**: Used for data analysis and manipulation.
- **pandas**: For handling dataframes.
- **matplotlib**: For plotting graphs.
- **seaborn**: For visualizing data, especially for heatmaps.
- **Google colab**:For writing and implementation.

## Data Cleaning/Preparation
---
In the data cleaning and preparation phase, the following tasks were performed:

1. **Loading the Data**: Imported the CSV file into a pandas DataFrame.
2. **Handling Missing Values**: Identified and addressed any missing values in the dataset.
3. **Data Formatting**: Cleaned and formatted the data to make it suitable for analysis.

## Analysis Tasks
---
### 1. Remove Duplicate Records

Check for duplicate records and remove them if found.

```python
# to read the file
import pandas as pd 
df=pd.read_csv('/content/file (1).csv')
df


# to check for duplicate values
df[df.duplicated()]
#remove duplicate
df.drop_duplicates(inplace = True)
```

### 2. Check for Null Values

Check for Null value in Data set.

```python
# to checj null
df.isnull()
#sum of null value
df.isnull().sum()

```

### 3. Show Information for 'House of Cards'

ind the Show_Id and Director for the show 'House of Cards'.

```python
df[df['Title'].isin(['House of Cards'])]
# method 2
df[df['Title'].str.contains('House of Cards')]

```

## Some other question includes
- Show only the Titles of all TV Shows that were released in India only.
- Show Top 10 Directors, who gave the highest number of TV Shows & Movies to Netflix ?
- Show all the Records, where "Category is Movie and Type is Comedies" or "Country is United Kingdom".
- In how many movies/shows, Tom Cruise was cast ?

