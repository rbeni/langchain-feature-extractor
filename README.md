# Langchain feature extractor

This project aims to extract text from news articles and then use a LLM to extract features from it.

It is divided in two parts:
* The first is a webscraper, capable of finding relevant articles, extracting the available information, cleaning the text and then saving the extracted text as txt files
* The second part is the LLM feature extractor. The texts are loaded and then inserted into the prompt text for analysis.

This webscrapper and LLM are part of another project that I am developing.

The code present is a evolution from the code published by pixegami

There is content in this repository containing copyrighted material from other companies. That copyright belongs to their respective owners. The MIT license covers only the code developed for this project.

## File description

    /news   # Folder containing the webscrapped articles
    news_scrapper.ipynb     # A jupyter notebook containing the code to obtain texts
    process_data.ipynb      # A jupyter notebook containing the code necessary to run the LLM and extract features from the news article

## Getting started

### Prerequisites
Running this project requires the following packages:

* bs4
* langchain-community

### Usage

Both parts of the project work independent. First run the scrapper to get the data, then load each txt file one at the time to feed to the LLM.

The LLM output is structured as a json file, containing a summary of the article provided and a list of entities present in the article alongside their respective sentiment.
