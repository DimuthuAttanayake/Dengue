# Dengue

This is the final project for [Computing Foundations](https://journalism.columbia.edu/ms-data-journalism), Fall 2025.

This project builds an auto-updating map for weekly dengue cases in Sri Lanka. Dengue is the mosquito borne disease that could be deadly. 
This map uses data from [Ministry of Health, Sri Lanka](https://www.epid.gov.lk/weekly-epidemiological-report/weekly-epidemiological-report).

## Methodology

### Scraping and cleaning data
 
* The most up to date pdf from the above link is scraped with BeautifulSoup
* Python library, Natural pdf is used to read, and extract the table on page 4 of the pdf. Then, the second and the last raw that has no data is dropped and the table is saved as a dataframe
* A copy of the dataset is made,where the column headers are renamed to reflect the actual data in each column: weekly and cumulative epidemiological data for selected diseases. 
* Weekly dangue data for each district is extracted and saved to a new dataframe. The rows for "Kalmunai", and "SRILANKA" are dropped since they are not districts.
* Each district is geocoded with latitudes and longitudes and then saved to a CSV as "Epid.csv".

### Live updates on the map

* The python script,the csv, and the file is then saved to a github repository.
* Github actions are turned on, and a .yml file is created.

### Creating the Website

* Index.html file created with a placeholder for the map, and pushed it to github repo.
* Turn on github pages to set up the website.

### Visualizations

* Create a map and a heatmap indicating data for each district in Sri Lanka with Datawrapper, by linking the CSV file from the github repository.
* Embed the mapto Index.html

## New Skills

* Using github actions to create a live updating website.
* Working with .yml file and updating cron.
* Creating a webpage with html.
* Setting up the website with github pages.
* Linking the CSV file from the github repository to datawrapper.
* Overall Learned to think through the entire process, from the point of data scraping to the point the live map with the website is published.
* This was an iterative process for me, but I learned how to think through for the next time.

## What more would I like to do?

* To weigh the dengue numbers for each district by population stats in this link:[Mid-year Population by District and Sex](https://www.statistics.gov.lk/Resource/en/Population/Vital_Statistics/Mid-year_population_by_district_and_sex_2025.pdf)
, before creating the map.
* To find out how many cases make it an outbreak and make this appear red on the map



## Contact

Dimuthu Attanayake, [dca@columbia.edu](mailto:dca@columbia.edu)


