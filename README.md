# 📊 Netflix Movies and TV Shows — Data Cleaning Project

## 🧹 Overview
This task focuses on **data cleaning and preprocessing** of the Netflix Movies and TV Shows dataset using **Python and Pandas**. The goal is to prepare the data for further analysis or modeling by handling missing values, parsing inconsistent formats, and transforming columns for better usability.

---
## 📌 Technologies Used

- Python
- Jupyter Notebook
- Libraries - `Pandas`, `NumPy`, `Matplotlib`, `seaborn`

---

## 📁 Dataset Description
The dataset contains metadata about movies and TV shows available on Netflix.  
Key columns include:

| Column         | Description                                |
|----------------|--------------------------------------------|
| `show_id`      | Unique identifier for each title           |
| `type`         | Movie or TV Show                           |
| `title`        | Title of the content                       |
| `director`     | Director of the movie/show                 |
| `cast`         | List of main cast members                  |
| `country`      | Country of origin                          |
| `date_added`   | Date the content was added to Netflix      |
| `release_year` | Original year of release                   |
| `rating`       | Age-based content rating                   |
| `duration`     | Duration in minutes or seasons             |
| `listed_in`    | Genre(s) the content belongs to            |
| `description`  | A short description of the content         |

---

## ✅ Data Cleaning Tasks Performed

- **Missing Value Handling**
  - Filled missing `director`, `cast`, and `country` values with `"Unknown"`.
  - The missing values in rating was imputed with its mode, since this attribute was discrete.
  - Records with missing values in the date_added column were dropped, since they were significantly low (10)

- **Duplicate Removal**
  - There were no duplicates in the dataframe.

- **Changing Datatype**

  - **Duration**
    - Typecasting of 'duration' from string to integer
    - For Tv shows, the duration represents 'number of seasons'
    - For movies, the duration represents 'movie length in minutes'
 
  - **Date Parsing**
    - Converted `date_added` to datetime format.
    - Extracted `year_added` and `month_added` from `date_added`.
    
- **Whitespace Removal**
  - Removed leading and trailing whitespaces from all string columns.

- **Column Name Standardization**
  - Renamed all column headers to lowercase and replaced spaces with underscores.

- **Data Export**
  - Exported cleaned dataset to a CSV file for downstream use.

---
