# CSV to SQL Converter

This Python script reads a CSV file, cleans it up, and converts it into a series of SQL `INSERT` statements.

## Requirements

- Python 3
- pandas

## Usage

1. Replace the `fname` variable with the path to your input CSV file.
2. Replace the `output_fname` variable with the path to your output CSV file.
3. Run the script.

```python
fname = "path_to_your_input_file.csv"
output_fname = 'path_to_your_output_file.csv'

This script performs the following steps:

Removes trailing whitespace from each line in the input CSV file and writes the cleaned lines to a temporary CSV file.
Reads the first line of the temporary CSV file to get the column names.
Strips trailing commas and whitespace from string columns in the DataFrame.
Attempts to convert string columns to datetime columns, if possible.
Writes the cleaned DataFrame back to the temporary CSV file.
Generates SQL INSERT statements for each row in the DataFrame and writes them to an output SQL file.
Cleans up the temporary CSV file.
The output is a SQL file with INSERT statements that can be run against a SQL database to insert the data from the CSV file.
