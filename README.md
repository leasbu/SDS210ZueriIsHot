## **Urban Heat in Zurich**

In this project you will analyse the LST and NDVI of the city of Zurich form 1985 to 2024 by using Landsat raster data for the 40 year time span, in three-year jumps. By analysing spatial trends, temporal varibility, and utilsing different staitical calculations and plots, you can uncover how the NDVI and the LST influence each other and how they have changed over teh last 40 years. 

## Research questions answered in this project:

Are certain Zurich neighbourhoods experiencing faster increases in land surface temperatures than others, and to what extent are these differences associated with changes in the vegetation measured by the NDVI?
Sub questions:
1)	Which neighbourhoods show the strongest increase in LST over time?
2)	Does a lower NDVI indicate lower LST?
3)	Has the LST-NDVI relationship changed over time?


## Data Sources
Landsat tifs: 
https://drive.google.com/drive/folders/1SmEzlCAJJGYY-TdB58JX6ADvVxSQrMqj 

District map: 
Stadt Zürich (https://www.stadt-zuerich.ch/geodaten/download/Stadtkreise)

## Software and Libraries needed for the project:

%pip install rasterio

%pip install folium

%pip install scipy

%pip install geopandas

%pip install seaborn


import pandas as pd

import numpy as np

import matplotlib.pyplot as plt

from pathlib import Path

import json

import rasterio

import folium

from folium.raster_layers import ImageOverlay

from scipy.stats import spearmanr

import geopandas as gpd

from rasterio.warp import calculate_default_transform, reproject, Resampling

import seaborn as sns


## Reproducing the Environment
This project requires a specific spatial software stack. To recreate the environment:
1. Ensure you have Conda installed.
2. Run: `conda env create -f environment.yml`
3. Activate: `conda activate Zueriishot`

Execution Order: 
Run the `UrbanHeatZh.ipynb` notebook from top to bottom