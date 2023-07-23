# Project: Data Enrichment with Web Scraping
## Project Description
This project provides an opportunity to learn how to enrich datasets with relevant data obtained from external sources. Businesses use data enrichment to learn more for better decision making. Using publicly available data, you’ll learn how to scrape online data and transform it into clean, structured data that can be merged with other relevant datasets for enrichment. Since today’s businesses often tend to automate data processing, you’ll also learn how to use Alteryx to automate the process of data transformation and integration.

## Project Objectives:
- Perform data aggregation to enrich datasets with relevant data obtained from other sources.
- Perform data transformation to convert data format, structure, or values to address data challenges.
- Implement data integration to merge related datasets to a dataset in use.
- Apply industry automation tools to automate data transformation and integration to address business needs.

## Scenario
In the highly competitive movie streaming services market, your client has asked for help with enriching their data with publicly available data. Using a dataset from your client containing different data about movies, you are tasked with scraping online publicly available data from the Internet Movie Database (IMDb), one of the most popular websites that contains large amounts of data on movies. You’ll need to transform the scraped data into a structured format and integrate it with your client’s data to come up with an enriched dataset.

## Key Tasks
This project has two parts with multiple tasks and separate deliverables for each part. For this project, we will focus on part A.

### PART A: Data Gathering, Transformation, and Enrichment.
Performed data gathering using web scraping to enrich your client’s dataset (`Movies.csv`) containing top voted 500 movies released between 2018 and 2020. The dataset includes the following fields:
- `movie_id`: alphanumeric unique identifier of the title.
- `originalTitle`: original title, in the original language.
- `titleType`: the type/format of the title (e.g., movie, short, tvseries, tvepisode, video, etc.).
- `isAdult`: 0 for non-adult title; 1 for adult title.
- `genres`: includes up to three genres associated with the title.

The dataset is available in the `data` folder.

1. Conducted Data Gathering:
   - Scraped this [IMDb webpage](https://www.imdb.com/search/title/?at=0&sort=num_votes,desc&start=1&title_type=feature&year=2018,2020) of movies released between 2018 and 2020, sorted by votes in descending order. Pulled movie_id, rank, title, year, rating, runtime, and votes for the top 500 movies sorted by user number of votes in descending order.
   - Transformed the scraped data to a structured format and write it to a CSV file (name it `IMDb_TopVoted.csv`).

2. Conducted Data Enrichment:
   - Imported the `Movies.csv` dataset to a pandas DataFrame called df1.
   - Imported the scraped data from the `IMDb_TopVoted.csv` file to a pandas DataFrame called df2.
   - Implemented data cleansing and transformation to convert the columns datatype for the df2
        - For example, movie runtime should be a numeric datatype.
   - Enrich the given dataset (df1) by merging it to the scraped data (df2).
   - Rearrange the dataset fields to be listed in the following order:
       - `movie_id`, `rank`, `votes`, `title`, `originalTitle`, `year`, `rating`, `titleType`, `isAdult`, `runtime`, `genres`
   - Export the enriched dataset to a CSV file: `Movies_Enriched.csv`.