# Boardgame Retail Success Predictor

Play around with the model and make predictions using the [web app](https://frozen-sierra-31974.herokuapp.com/)
I made using [Streamlit](https://www.streamlit.io/).

Checkout my [blog post](https://brianhtam.github.io/).

#### Description
Predicting Boardgame retail volume using by fitting a linear regression model on the data from the BoardGameGeek 
API. Success is measured by the number of people who indicated that they own the game on BoardGameGeek's website.  

This project was developed over a 2-week span in October 2020 as a project for 
the [Metis](https://thisismetis.com) data science program.

The model in `data/final_model.pkl` was trained on BoardGameGeek statistics and other data defined below, using a Lasso 
linear model. The R2 score is `##` and it has a RMSE is `##`. The blog post about it is 
[here](https://brianhtam.github.io/).

#### Data Sources
* [BoardGameGeek](https://boardgamegeek.com/browse/boardgame) 
* [BGG XML API2](https://boardgamegeek.com/wiki/page/BGG_XML_API2)
* [Amazon](https://www.amazon.com/)
* [Kickstarter](https://www.kickstarter.com/)

#### File Contents
* `data/`
    - `final_model.pkl` is a pickled version of a pre-trained scikit-learn Lasso regression model.
* `notebooks/`
    - `Data Acquisition & Cleaning.ipynb` contains all web-scraping, API requests, and 
       data cleaning/preparation for this project.
    - `EDA & Modeling Workbook (Project V1).ipynb` contains the analysis and modeling for predicting 
       Boardgame retail success. 
* `utilities/`
    - `data_acquisition_utilities.py` contains functions used in `Data Acquisition & Cleaning.ipynb`.
    - `modeling_utilities.py` contains functions used in the modeling Jupyter Notebooks.
* `app.py` contains code for a [Streamlit](https://www.streamlit.io/) app that can be used to play around 
  with the model and make predictions.
* `Procfile` and `setup.sh` are files necessary for deploying the streamlit app to Heroku.

#### Dependencies

The Python packages required for this project are listed in both `requirements.txt` & `environment.yml`. 
You can install the packages via:

`pip install -r requirements.txt`

or by creating an Anaconda environment:

`conda env create -f environment.yml`.

Additionally, in order to completely run `Data Acquisition & Cleaning.ipynb` notebook, you'll need to:

1. Install [ChromeDriver](https://chromedriver.chromium.org/getting-started).
