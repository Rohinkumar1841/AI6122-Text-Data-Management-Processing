README.txt

----------------------------------------------------------------------------------------

# DBLP Dataset Processing and Indexing

This repository contains a Jupyter Notebook (.ipynb) for processing the DBLP dataset, creating an index, and enabling efficient retrieval of academic publications. The code uses third-party libraries to parse the DBLP XML files, extract information, and create a searchable index. This README provides instructions on setting up the system, including the installation of required libraries and how to use the system to perform publication searches.

----------------------------------------------------------------------------------------

## THIRD-PARTY LIBRARIES

The code relies on the following third-party libraries for its functionality, which can be installed via pip:

- NLTK (Natural Language Toolkit): A library for natural language processing.
- lxml: A library for processing XML and HTML.
- Whoosh: A fast, featureful full-text indexing and searching library.
- Matplotlib: A plotting library for creating visualizations.
- Plotly: An interactive, open-source, and browser-based graphing library for Python built on top of plotly.js.
- Wordcloud: library that creates word clouds based on word frequency.
To install these libraries, please refer to the installation guide provided below.

----------------------------------------------------------------------------------------

## INSTALLATION GUIDE

### SYSTEM REQUIREMENTS

Make sure that the system meets the following requirements:

- Operating System: Any compatible with Python 3.x
- Python Version: Python 3.x
- Sufficient RAM and storage space for the dataset and indexing.

### INSTALLATION STEPS

1. Download the DBLP dataset and required DTD file from the URL mentioned below:

   [DBLP Dataset Download](https://dblp.org/)

2. Run the following three lines of code in a Jupyter Notebook cell:

   - `!wget https://dblp.uni-trier.de/xml/dblp.xml.gz`
   - `!wget https://dblp.uni-trier.de/xml/dblp.dtd`
   - `!gzip -d dblp.xml.gz`

3. Install the necessary Python libraries as mentioned in the Third-Party Library section. Run the following codes in a new cell of your Jupyter Notebook:

   - `!pip3 install nltk -q`
   - `!pip3 install lxml -q`
   - `!pip3 install whoosh -q`
   - `!pip3 install matplotlib -q`
   - `!pip3 install plotly -q`
   - `pip install wordcloud` 

----------------------------------------------------------------------------------------

## GUIDE TO RUN THE SYSTEM:

1. Download the provided Jupyter Notebook (.ipynb) file.
2. Open your Jupyter Notebook environment or JupyterLab.
3. Upload the downloaded Jupyter Notebook file to your Jupyter environment.
4. Open the Jupyter Notebook file in your Jupyter environment.
5. Execute the code cells within the Jupyter Notebook. The code processes the DBLP dataset, creates an index, and allows you to search for publications. Follow the instructions of input prompts shared below to retrieve the desired results.

----------------------------------------------------------------------------------------

## SEARCH QUERY FORMAT AND PARAMETERS:

### PROMPT FOR SEARCH QUERY

**Input Format:**
<Query to retrieve title> AND year:<Query to retrieve year> AND authors:<Query to retrieve author>


**Examples:**

- `machine learning AND year:2020 AND authors:John Doe`
- `data analysis OR data mining AND year:2019 AND authors:Jane Smith`

**Prompt:**

When you run the Jupyter Notebook, it will ask you to input a search query. This is where you specify the terms or keywords you want to search for in the academic publications in the above format. You may make use of the logical operator 'OR' in combination with the 'AND' to retrieve a complex search query.

----------------------------------------------------------------------------------------

## SAMPLE OUTPUT:

The code provides sample output in the form of search results. It displays information about publications that match the search query, including title, authors, venue, and year.

------------------------------------------------------------
Rank: 1
Score: 4.385910987
Title: Sample Title 1
Authors: John Doe, Jane Smith
Venue: Conference Name
Year: 2022

------------------------------------------------------------
Rank: 2
Score: 4.203983712
Title: Sample Title 2
Authors: Emily Johnson, Mark Davis
Venue: Journal Name
Year: 2020

This example demonstrates what you can expect when using the Jupyter Notebook to search for publications.

----------------------------------------------------------------------------------------

## EXPLANATION OF RESULTS:

The above sample output shows the top publications that match the provided search query. The results are sorted by relevance, with the top-ranked publications being the most relevant to your query. The code retrieves and displays these publications based on the search query format you provided, and it can handle complex queries using 'AND' and 'OR' operators. You can adjust the search query to find publications that best match your specific research interests.

- **Rank:** Each publication in the search result is assigned a rank based on its relevance to the search query. The top-ranked publication is the most relevant.

- **Score:** The score indicates the relevance score of the publication to the search query. Higher scores indicate a closer match to the query.

- **Title:** This is the title of the publication that matches the search query.

- **Authors:** The list of authors who contributed to the publication.

- **Venue:** The venue where the publication was presented or published, which could be a conference, journal, workshop, etc.

- **Year:** The year in which the publication was published or presented.

The search results are ordered by relevance, with the most relevant publications appearing first in the output.

----------------------------------------------------------------------------------------
Source Code

The Source code file contains two  .ipynb files one for Data analysis and one for the Search engine, Research trend explorer and Application

