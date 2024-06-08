# Amazon Mobile Phones Web Scraping Project

## Introduction

This Python script aims to scrape detailed information about mobile phones listed on Amazon. By extracting data such as model name, brand, specifications, and pricing, the script provides a structured dataset for analysis or comparison purposes.


## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [Disclaimer](#disclaimer)


## Installation

To use this script, ensure you have Python installed on your machine. You will also need to install the following Python packages using pip or you can do it manually:

```bash
pip install -r requirements.txt
```
`requests`: For making HTTP requests to Amazon's website.

`beautifulsoup4`: For parsing the HTML content of the Amazon pages.

`pandas`: For organizing the scraped data into a structured format.

`openpyxl`: For writing the scraped data to an Excel file.

**Note:** Make sure you run this command from the directory where `requirements.txt` is located.

## Usage
1. Clone the repository or download the script.
```bash
git clone https://github.com/MinaNabil730/web-scrapping-from-scratch
```
2.Navigate to the project directory in your terminal
```bash
cd path/to/your/project/directory
```
3. Ensure you have the required packages installed.
4. Run the Jupyter Notebook (`Amazon_Mobile_Phone_Scraper.ipynb`) to initiate the scraping process:

    ```bash
    jupyter notebook amazon_scraper.ipynb
    ```
    if this command doesn't work, you can use:
   ```bash
    python -m notebook
   ```
    Then, navigate to and open `amazon_scraper.ipynb` in the Jupyter Notebook interface.

6. The script will generate an `mobile_data.xlsx` file containing the scraped data.

   
## Project Structure
amazon_scraper/

amazon_scraper.ipynb: Main script for scraping Amazon mobile phone data

requirements.txt: List of required Python packages

README.md: Documentation file explaining project details


## Results

Upon completion, the script produces an `mobile_data.xlsx` file with the following information for each mobile phone:

- Model Name
- Brand
- Operating System
- RAM
- Storage Capacity
- Screen Size
- Resolution
- Refresh Rate
- Cellular Technology
- Product Link (URL)

Troubleshooting
---------------

If the project doesn't work as expected, try the following:

### Changing Headers

If the headers or structure of the data on Amazon's website change, you may need to update the script accordingly:

- Modify the headers in the script (`amazon_scraper.py`) to adapt to any changes required by Amazon's website. Here is an example of headers you might need to adjust:

    ```python
    headers = {
        "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/98.0.4758.102 Safari/537.36",
        "Accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8",
        "Accept-Language": "en-US,en;q=0.9",
        "Accept-Encoding": "gzip, deflate, br",
        "Connection": "keep-alive",
        "Upgrade-Insecure-Requests": "1",
        "Cache-Control": "max-age=0",
        "Sec-Fetch-Dest": "document",
        "Sec-Fetch-Mode": "navigate",
        "Sec-Fetch-Site": "same-origin",
        "Referer": "https://www.amazon.com",
        "Origin": "https://www.amazon.com",
        "Content-Type": "text/html; charset=utf-8",
    }
    ```

- Check for errors in the script output or logs to identify specific issues related to headers or network requests.

### Runtime Note

Please note that the script might take approximately 10 to 20 minutes to run, depending on the number of products being scraped and your internet connection speed.

## Uploading Data File

Initially, the `mobile_data.xlsx` file is included in the GitHub repository for convenience. However, to ensure the data remains up-to-date with the latest information from Amazon, it's recommended to periodically run the script. This will update the file with the most current product details.


## Limitations

Due to variations in seller listings, some fields in the resulting dataset may contain NaN values or incomplete information. Efforts were made to handle these cases gracefully within the scraping script.


## Disclaimer

This project is intended for educational purposes only. Web scraping may violate the terms of service of websites like Amazon. Use this script responsibly and consider obtaining permission from the website owner before scraping their data.


