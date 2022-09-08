# Düsseldorf Noise Pollution --- TechLabs 2022
### TechLabs Düsseldorf, Digital Shaper Program
### Sommer Term 2022

**Developers**
* @MehraveMokhtarian
* @joejosephgeorge
* @af-pedro

**Mentor support from**
* @semalfni

## Overview

This project provides an overview of noise pollution in düsseldorf streets using different visualisation technics.

## Our journey 

The whole project can be divided into three steps:

1. Gathering datasets 
2. Making the dataset ready as a csv file to be plotted and used for visualization 
3. Combining the visualized dataset with some kind of navigation in order to make it interactive

### Challenges

1. finding and importing dataset  2. data manipulation  3. visualization

During our search for dataset we gone through a lot of datasets and there were some problems with most of the datasets that were available such as:

1. the number of stations were not enough which means that the final visualization would be so much generalized that could not be accurate on the scale of one city at all
2. the provided data were not that much up to date and we did face a lot of valuable datasets which were mainly created and updated some years before 
3. the addresses provided on some of datasets where not accurate enough for us so we couldn't find their accurate Latitude and Longtitude 

After finding the proper datasets (at opendata.duesseldorf.de) we needed to execute their Latitude and Longitude in order to be able to visualize them further on a map. we found two ways for getting the Lat and Lng of coordinates:

1. API Calling (the problem with this option was the fact that we had nearly 80,000 rows of coordinates and each key that we used for API Calling got expired after executing about 2800 rows)
2. GeoPy

after the mentioned steps+manipulation process the dataset was ready to be visualized;
basically we had two alternatives for visualizing: 1. interactive map 2. plotting multiple maps

by the first alternative everything was ready and we just needed to work with some libraries 
by the second option, we faced problems on subplotting, which was caused by having various CRS for different files. so we neede to unite the Coordinate Reference System of our shapefile and our csv visualization.

the last decision to make on visualization step was regarding the scale of the maps; whether we want to present information on neighborhood scale or on street scale. in the end we decided to go for both of them and provide two different maps.

## Structure of the repository

### notebooks explanation

1. loading and cleaning data.ipynb >>> it is what it is
2. geometry extraction using geopy & merging csv.ipynb >>> in order to extract Lat and Lng as it is explained above
3. eda.ipynb >>> explorative analysis of the data
4. GeoPandas_Static.ipynb >>> working with spatial data

and other notebooks are just different ways of visualizing that we tried.

## How to run the notebooks on your own

- In order to run the notebooks you may need to create an python environment and install the needed packages.
- Have Python >3.8
- [Install poetry](https://python-poetry.org/)
- Install dependencies with `poetry install`
- **Alternative**: Install python packages from the *requirements.txt* file
- run `jupyter lab` to start working on the notebooks
