# banks_project
# Banks Data ETL Project

## Overview
This project involves extracting, transforming, and loading (ETL) data related to the largest banks from a specified webpage. The goal is to gather information on the top banks, including their rankings, names, and market capitalization in USD billion. The project follows a series of ETL operations to process and store the data for further analysis.

## Workflow

### 1. Extraction
The `extract` function retrieves data from a designated URL, focusing on the table containing information about the largest banks. It parses the HTML content, extracts relevant details such as bank names and market capitalization, and prints a table displaying the banks in USD billion.

### 2. Transformation
The `transform` function processes the extracted data. It utilizes exchange rates from a CSV file to convert market capitalization to other currencies, including GBP, EUR, and INR. The transformed data is then printed as a table, showcasing additional columns with values in different currencies.

### 3. Loading
The final data frame is loaded into a CSV file using the `load_to_csv` function. Additionally, the data is loaded into a SQLite database table named 'Largest_banks' using the `load_to_db` function.

## Logging and Querying
Throughout the process, a logging mechanism records progress and timestamps into a log file. Queries are run on the SQLite database to retrieve and print specific information, such as the average market capitalization in GBP and the names of the top 5 banks.

## Execution
The project execution involves calling the relevant functions in sequence, starting from data extraction to logging completion. The entire workflow is encapsulated within the script, ensuring a streamlined and repeatable process.

## Dependencies
- `requests` for making HTTP requests
- `pandas` for data manipulation and analysis
- `BeautifulSoup` for HTML parsing
- `numpy` for numerical operations
- `sqlite3` for SQLite database operations

## Output
The final output includes a CSV file ('Largest_banks_data.csv') containing the transformed data and relevant log entries in the 'code_log.txt' file.

---

*Note: Ensure proper configuration of the project environment, including the specified URL, file paths, and dependencies, for successful execution.*
