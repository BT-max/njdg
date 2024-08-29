# Judicial Data Scraper

This project is a Python script designed to scrape judicial data from a specified webpage and save it in either CSV format or as a dictionary.

## Prerequisites

- Python 3.x
- pip (Python package installer)

## Installation

1. Clone the repository:
    ```shell
    git clone git@github.com:BT-max/njdg.git
    cd njdg
    ```

2. Install the required packages:
    ```shell
    pip install -r requirements.txt
    ```

## Usage

To run the script, use the following command:

```shell
python scrape.py --url <URL> [--output <csv|dict>] [--filename <filename>]
```
## Arguments
- --url <URL>: Required. The URL of the webpage to scrape.
- --output <csv|dict>: Optional. Specifies the output format. Choose between csv (default) or dict.
- --filename <filename>: Optional. The name of the output file when --output is set to csv. Defaults to judicial_data.csv if not specified.

## Help
To see the help message with all available options, run:
```python
python scrape.py --help
```

## Examples

1. Scrape data and print it as a dictionary:

    ```shell
    python scrape.py --url "https://njdg.ecourts.gov.in/njdgnew/?p=main/index&state_code=27~1" --output dict
    ```

2. Scrape data and save it as a CSV file:

    ```shell
    python scrape.py --url "https://njdg.ecourts.gov.in/njdgnew/?p=main/index&state_code=27~1" --output csv
    ```

## Functions

- `scrape_table_data(url)`: Scrapes table data from the given URL and returns it as a DataFrame.
- `save_to_csv(df, filename)`: Saves the DataFrame `df` to a CSV file with the specified filename.
- `convert_to_dict(df)`: Converts the DataFrame `df` to a dictionary.

## License

This project is licensed under the MIT License. See the LICENSE file for details.
