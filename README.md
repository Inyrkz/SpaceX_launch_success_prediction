# SpaceX_launch_success_prediction

# Overview
In this capstone, we will predict if the Falcon 9 first stage will land successfully. SpaceX advertises Falcon 9 rocket launches on its website with a cost of 62 million dollars; other providers cost upward of 165 million dollars each, much of the savings is because SpaceX can reuse the first stage. Therefore if we can determine if the first stage will land, we can determine the cost of a launch. This information can be used if an alternate company wants to bid against SpaceX for a rocket launch.

The `jupyter-labs-spacex-data-collection-api.ipynb` is for data extraction via the SpaceX API.

The objectives are:
- make a get request to the SpaceX API.
- do some basic data wrangling and formating to clean the requested data.

The output of the notebook is `dataset_part_1.csv`. 

# WebScraping
In this lab, I performed web scraping to collect Falcon 9 historical launch records from a Wikipedia page titled List of Falcon 9 and Falcon Heavy launches
https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches
The notebook is `jupyter-labs-webscraping.ipynb`.

The objectives are:
- Web scrap Falcon 9 launch records with BeautifulSoup.
- Extract a Falcon 9 launch records HTML table from Wikipedia.
- Parse the table and convert it into a Pandas data frame.

The output file is `spacex_web_scraped.csv`.



# Data Wrangling

The objectives are: 
- Perform exploratory Data Analysis and determine Training Labels.
- Exploratory Data Analysis.
- Determine Training Labels.

The `labs-jupyter-spacex-data_wrangling_jupyterlite.jupyterlite.ipynb` notebook is for data wrangling. 

In this lab, we will perform some Exploratory Data Analysis (EDA) to find some patterns in the data and determine what would be the label for training supervised models.

In the data set, there are several different cases where the booster did not land successfully. Sometimes a landing was attempted but failed due to an accident; for example, True Ocean means the mission outcome was successfully landed to a specific region of the ocean while False Ocean means the mission outcome was unsuccessfully landed to a specific region of the ocean. True RTLS means the mission outcome was successfully landed to a ground pad False RTLS means the mission outcome was unsuccessfully landed to a ground pad.True ASDS means the mission outcome was successfully landed on a drone ship False ASDS means the mission outcome was unsuccessfully landed on a drone ship.

In this lab we will mainly convert those outcomes into Training Labels with 1 means the booster successfully landed 0 means it was unsuccessful.

The output of this notebook is the `dataset_part_2.csv` file.



# Exploratory Data Analysis with SQL


