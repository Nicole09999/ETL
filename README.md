# ETL
# ETL Pipeline for Data Transformation

This Python script demonstrates an ETL (Extract, Transform, Load) pipeline for transforming data from various file formats (CSV, JSON, XML) into a unified CSV format. The script processes files in the current directory, extracts data from each file format, applies transformations, and saves the transformed data into a CSV file.

## Requirements

To run this script, you need:

- Python 3.x installed on your system.
- Required Python libraries: `glob`, `pandas`, `xml.etree.ElementTree`, `datetime`.

You can install the required libraries using pip:

```
pip install pandas
```

## Usage

1. Place the script in the directory containing the files to be processed.
2. Update the file paths (`log_file` and `target_file`) if needed.
3. Run the script using Python:

```
python script_name.py
```

## Functions

- **extract_from_csv(file_to_process)**: Extracts data from a CSV file and returns a pandas DataFrame.
- **extract_from_json(file_to_process)**: Extracts data from a JSON file and returns a pandas DataFrame.
- **extract_from_xml(file_to_process)**: Extracts data from an XML file and returns a pandas DataFrame.
- **extract()**: Extracts data from all files in the directory using the above extract functions.
- **transform(data)**: Applies transformations to the extracted data (converts units from inches/pounds to meters/kilograms).
- **load_data(target_file, transformed_data)**: Saves the transformed data to a CSV file.
- **log_progress(message)**: Logs progress messages with timestamps to a log file.

## Execution Flow

1. The script initializes and logs the start of the ETL job.
2. It extracts data from files using the `extract()` function and logs the extraction phase.
3. Data is transformed using the `transform()` function, and the transformed data is printed to the console.
4. The script saves the transformed data to a CSV file and logs the load phase.
5. Finally, it logs the completion of the ETL job.

The script provides a structured approach to handle data transformation tasks, facilitating reproducibility, and ensuring traceability through logging.
