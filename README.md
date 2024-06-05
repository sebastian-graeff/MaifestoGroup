# Manisiesta

## Description
Using several features of a country, the goal is to determine whether there is a connection between these features and the gini coëfficient, a measurement of inequality. The features used are the rile score, the political orientation of the leading party, social welfare spending, level of democracy, GNI, with a main focus on the stance positivity score calculated using the Manifestoberta data.

Because of the varying definitions of conservatism and liberalism in geographical areas, there is a focus on Europe. 
Because of possible major shifts between left and right / conservatism and liberalism in certain time periods, the initial research is focused on a time period: 2005-2020.

This research is done through a linear (?) regression model.

## Table of Contents
1. [Installation] (#installation)
2. [Usage] (#usage)
3. [Acknowledgements] (#acknowledgements)

## Installation

To install this project, you need access to the private repository / the file has to have been shared with you personally. Please ensure you have been granted the necessary permissions.

Clone the repository:
```bash
 git clone https://github.com/sebastian-graeff/ManifestoGroup.git
```

## Usage
In order to make the set up of the project more clear and make everything run smoothly, this is an overview of what everything is and in what order everything is best to run in:
1. Folder: 2015-Country-Manifestos
    This folder contains manifestos retrieved from the manifesto project database using an API (this code can be found in the MANIFESTO RETRIEVAL folder)
2. Folder: CLEAN_DATA
    This folder contains all data after each stage of cleaning, merging, or changing it.
3. Folder: MANIFESTO RETRIEVAL
    This folder contains the code for the API and the API key to retrieve the manifestos from the manifesto project database.
4. Folder: RandomManifestos
    This folder contains the random manifestos selected and a separate folder with their translations, the manifestos are translated in the TranslateManifesto.ipynb file.
5. Folder: RAW_DATA
    Contains the raw data for each variable.
6. Folder: SURVEY_DATA
    Contains the data collected through the data and the cleaning and evaluation files.
7. Folder: TRAIL AND ERROR
    This folder contains codes for things we tried to further improve the project, that didn't end up working.
8. File: data_cleaning.ipynb
    # RUN THIS FILE FIRST
    This code cleans all the data and combines the datasets into one whole.
9. File: groupby_country.ipynb
    # RUN THIS FILE THIRD
    This code groups all countries and election years together. This way we get a dataset that represents per country, per year.
10. File: interactive_variable.ipynb
    # RUN THIS FILE FOURTH
    This code creates an interactive variable out of all the variables together.
11. File: Kmeans.ipynb
    # RUN THIS FILE AFTER RUNNING LinearRegression.ipynb
    This code groups all election years and countries that have similar features.
12. File: LinearRegression.ipynb
    # RUN THIS FILE FIFTH
    This code represents our model.
13. File: stance_positivity_score.ipynb
    # RUN THIS FILE SECOND
    This code calculates the positivity score variable.
14. File: survey_chunk_selection.ipynb
    # RUN THIS FILE AFTER TranslateManifestos.ipynb
    This code selects random chunks from the selected manifestos to use in our survey.
15. File: TranslateManifestos.ipynb
    # TIME OF RUNNING THIS FILE DOES NOT MATTER
    This is the code that translates the manifestos.

## Acknowledgements
This project was an assignment for the Computational Social Science course at the University of Amsterdam.
The main dataset used was data from the manifesto-project [https://manifesto-project.wzb.eu/]
The GNI was retrieved from the World Bank databank (World Development Indicators) [https://databank.worldbank.org/reports.aspx?source=world-development-indicators]
The level of democracy was retrieved from the v-dem dataset [https://v-dem.net/data/the-v-dem-dataset/]
The social welfare spending was retrieved from OECD [https://stats.oecd.org/Index.aspx?datasetcode=SOCX_AGG]

The project was a collaboration between:
- Emma Bösz
- Sebastian Gräff
- Vincent Hendriksen
- Sanne van Loo