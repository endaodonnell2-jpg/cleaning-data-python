Football Player Data Cleaning with Pandas
Overview
This project demonstrates data cleaning and preprocessing using Pandas on a simulated football player dataset (football_simulated.csv). The main goals are to:

Inspect the dataset for missing values, duplicates, and inconsistencies

Fix a column header typo

Handle missing data by removing rows with multiple missing values and imputing missing values with column means

Save the cleaned dataset for further analysis

Dataset
The dataset contains physical and performance metrics of football players, including:

Height (cm)

Weight (kg)

Thigh circumference (cm) — originally misspelled as ThighCircumerence(cm)

Speed (m/s)

Date of Birth (DOB)

Age

What the Script Does
Load data from football_simulated.csv into a Pandas DataFrame.

Explore data by printing the first rows, dataset info, descriptive statistics, and count of missing values per column.

Fix a typo in the column name from ThighCircumerence(cm) to Thigh_Circumference_cm.

Check for duplicate rows and confirm none exist.

Identify rows with multiple missing values — if any are found, delete them (none found in this case).

Fill missing values in the remaining columns with the mean of each column, rounded to 2 decimal places.

Output updated descriptive statistics to verify missing values are handled.

Save the cleaned DataFrame to football_sim_cleaned.csv without the index column.

How to Use
Make sure you have Python 3 and Pandas installed:
pip install pandas
Place football_simulated.csv in the same folder as the script.

Run the script:
python football_data_cleaning.py
The cleaned data will be saved as football_sim_cleaned.csv.

Important Notes
The descriptive statistics show that weights are clipped at 82kg, possibly indicating data loss for heavier players.

The cleaning process assumes no categorical data needing special handling; missing numeric data is filled with the mean.

Rows with multiple missing values would be dropped, but none were found in this dataset.

Output Sample
Prints initial data preview, info, and stats.

Displays counts of missing cells per column and confirms no duplicates.

Shows descriptive stats before and after filling missing values.

Confirms saving the cleaned file.
