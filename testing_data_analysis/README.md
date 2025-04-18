# Data analysis 

This directory contains all R code for data analysis, it was developed within JetBrains DataSpell IDE and requires R to be installed.

## Implementation notes

- Due to the size of the results from `pre_testing\model_testing\results`, R has been used to analyze the results
- A SQLite database is created as opposed to attempting to load the entire CSV file into memory
- The original results CSV files are located in `full_results.zip`, extracted
- It is assumed that the .csv file is included within this directory for analysis is huge, so will not be included in the repository
- Make sure there is enough memory available to run the analysis

## Run 

1. Run the `installs.R` first

### Automated testing results (~100,000+ datapoints)
2. Extract the `full_results.zip` file and put it into `automated_testing/results` directory
3. Run the `automated_testing/create_sqllite_db.R` to create a database from the large CSV file generated from results
   1. This will create a SQLite database file in the current directory
   2. JetBrains DataGrip can be used to view the database (or other appropriate tools)
4. Run the `automated_testing/results_analysis.R` to perform the analysis

### Manual testing results (~100+ datapoints)
2. Import the `results.csv` file to `manual_testing/results.csv`
3. Run the `results_analysis.R` file
