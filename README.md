# Convertible Bond Scraper

Crawl convertible bond information from Taiwan Stock Exchange (TWSE) Market Observation Post System

## Source
* [Taipei Exchange](https://www.tpex.org.tw/web/bond/publish/convertible_bond_search/memo.php?l=zh-tw)
* [Taiwan Stock Exchange Market Observation Post System](https://mops.twse.com.tw/mops/web/t108sb08_1_q2)

## Directory Structure
    .
    ├── configFile                                     # Contains all the configuration files required in the scripts
    │   └── requirements.txt                           # Required Python packages
    ├── output                                         # Output folder (automatically generated)
    │   ├── bond_info                                  # Convertible bond information CSV files (use execution date as file name)
    │   │   └── <YYYY-mm-dd>.csv                       # List of convertible bond information
    │   └── bond_news                                  # Convertible bond news files (sorted by news publication date)
    │       ├── <YYYYmmdd>                             # Convertible bond news by date as text files
    │       │   └── <BOND_NEWS_FILENAME>.txt
    │       └── summary                                # Convertible bond news by year as CSV files
    │           ├── <YYYY_price>.csv
    │           └── <YYYY_transfer>.csv
    ├── template                                       # Convertible bond information CSV downloaded from TWSE website
    │   └── <convertible_bond_publish_YYYY-mm-dd>.csv
    ├── convertible_bond_news_daily_scraper.py
    ├── convertible_bond_news_yearly_scraper.py
    └── convertible_bond_scraper.py

## Outputs
### Convertible Bond Information CSV File
![Bond Info CSV](https://github.com/andy2167565/Convertible-Bond-Scraper/blob/78563052d4904f7f2f65ed98fbd7fb0dc023e7cf/img/bond_info_csv_output_example.JPG)
### Convertible Bond News Text File
![Bond Transfer News TXT](https://github.com/andy2167565/Convertible-Bond-Scraper/blob/78563052d4904f7f2f65ed98fbd7fb0dc023e7cf/img/transfer_news_text_output_example.JPG)
![Bond Price News TXT](https://github.com/andy2167565/Convertible-Bond-Scraper/blob/78563052d4904f7f2f65ed98fbd7fb0dc023e7cf/img/price_news_text_output_example.JPG)
### Convertible Bond News CSV File
![Bond Transfer News CSV](https://github.com/andy2167565/Convertible-Bond-Scraper/blob/78563052d4904f7f2f65ed98fbd7fb0dc023e7cf/img/transfer_news_csv_output_example.JPG)
![Bond Price News CSV](https://github.com/andy2167565/Convertible-Bond-Scraper/blob/78563052d4904f7f2f65ed98fbd7fb0dc023e7cf/img/price_news_csv_output_example.JPG)

## How to Execute
### Install packages
```
pip install -r requirements.txt
```

### Run the script
```
python convertible_bond_scraper.py
python convertible_bond_news_daily_scraper.py YYYY-MM-DD
python convertible_bond_news_yearly_scraper.py YYYY
```
***
Copyright © 2021 [Andy Lin](https://github.com/andy2167565). All rights reserved.
