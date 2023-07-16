# GeneExpressionOmnibus_Crawler

![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-59666D?style=for-the-badge&logo=beautifulsoup&logoColor=white)

# :dna: Automated Genome Profiling and Analysis :dna:

This repository contains Python code that performs automated profiling and analysis of human genome bindings using high throughput sequencing data from the NCBI Gene Expression Omnibus (GEO) database. 

## :pushpin: Table of Contents

- [Background](#background)
- [Prerequisites](#prerequisites)
- [Methodology](#methodology)
- [Output](#output)
- [Usage](#usage)
- [Contributing](#contributing)

## :bulb: Background

The code is designed to interact with the NCBI GEO database and perform a thorough search for genome bindings of human genes based on high throughput sequencing data. 

## :computer: Prerequisites

* Python 3.6 or later.
* Required Python libraries: Selenium, BeautifulSoup, pandas.
* Download the appropriate version of `chromedriver` based on your system from [here](https://chromedriver.chromium.org/downloads) and place it in the same directory as your Python script. This is essential for Selenium to automate the web browser for data scraping.

## :chart_with_upwards_trend: Methodology

The code works in the following way:

1. It starts by opening the NCBI GEO database and prepares the search box and search button elements for interaction.
2. It reads an Excel file that contains a list of genes and iteratively performs searches on the database for each gene.
3. For each search, it retrieves all the available information about genome bindings and stores them in a dataframe.
4. It repeats the process for each page of search results until no further pages are available.
5. The dataframe is then written to an Excel file, which contains details about the gene, the title of the study, and the URL link to the detailed information on the database.
6. The process is then repeated for each URL to retrieve more detailed information such as journal name, organization, quality control status, and the number of times the gene appears.
7. The newly obtained data are then appended to the dataframe and written to a new Excel file.

## :floppy_disk: Output

The output of this code is an Excel file that contains comprehensive details of each gene search, including gene name, title of the study, URL link to the study, journal name, organization, quality control status, and the number of times the gene appears in the study.

## :book: Usage

To run this code, simply execute the Python script after ensuring that all prerequisites are met. Make sure the `chromedriver` executable and your input Excel file are located in the same directory as your Python script.

> :warning: This code is provided as is. The user is responsible for ensuring compliance with the terms of use of the NCBI GEO database and any other data sources.

## :handshake: Contributing

Contributions are welcomed! Please feel free to create a pull request for minor issues such as typos or bug fixes. For major changes or new features, please open an issue first to discuss what you would like to change.

