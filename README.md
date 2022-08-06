# Düsseldorf Noise Pollution --- TechLabs 2022
# This was our first DS project which was developed and mentored by TechLabs team

# the aim of the project was to make a dataset which provide information about noise pollution in düsseldorf streets. the whole project can be divided into three steps:
1. gathering datasets 2. making the dataset ready as a csv file to be plotted and used for visualization 3. combining the visualized dataset with some kind of navigation in order to make it interactive

# during our search for dataset we gone through a lot of datasets and there were some problems with most of the datasets that were available such as; 
1. the number of stations were not enough which means that the final visualization would be so much generalized that could not be accurate on the scale of one city at all
2. the provided data were not that much up to date and we did face a lot of valuable datasets which were mainly created and updated some years before 
3. the addresses provided on some of datasets where not accurate enough for us so we couldn't find their accurate Latitude and Longtitude 

# after finding the proper datasets (at opendata.duesseldorf.de) we needed to execute their Latitude and Longtitude in order to be able to visualize them further on a map. we found to ways for getting the Lat and Lng of coordinates:
1. API Calling (the problem with this option was the fact that we had nearly 80,000 rows of coordinates and each key that we used for API Calling got expired after executing about 2800 rows)
2. GeoPy


## Getting started

- Have Python >3.8
- [Install poetry](https://python-poetry.org/)
- Install dependencies with `poetry install`
- Alternative: Install python packages from the requirements.txt file
- run `jupyter lab` to start working on the notebooks
