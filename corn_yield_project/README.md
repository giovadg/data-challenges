**Project description**

This project implements a data-driven pipeline to forecast U.S. national corn yield using historical yield data and weather-derived features.  
The notebook documents the modeling choices, assumptions, and exploratory findings developed during the project.


**Corn yield data**

Historical U.S. corn yield data are downloaded from a U.S. government public API.

To run the notebook, the user must:
- create their own API key from the corresponding government website;
- provide the key locally (the key is not included in this repository).

An active internet connection is required to download the data.


**Weather data**

The weather dataset used for feature extraction and forecasting cannot be redistributed.  
It was provided externally, and its provenance and licensing do not allow public disclosure.

- The dataset is not included in this repository.
- The notebook assumes the presence of a weather dataset with the required schema.
- Only code and methodology are shared.


**Notes on results and configuration**

The notebook reports results obtained during exploratory experimentation with the model.

For example, the user can set:

        YEAR_PREDICTION = 2023  
        MONTHS_RANGE         = (5,8) 

to obtain a national yield forecast for 2023 when the core growing-season months (May–August) are included in training.


**Runtime**

Typical runtime is approximately 5–10 minutes, depending on hardware.

The most time-consuming steps are:
- training the Random Forest and Neural Network models;
- computing aggregated weather features.


**Required packages**

- torch  
- scikit-learn  
- numpy  
- scipy  
- statsmodels  
- pandas  
- requests  

(Standard-library modules such as `collections` and `random` are also used.)
