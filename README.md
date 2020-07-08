# NOTE
This repo is a part of a collaborative series of repos that explores the ability of multiple products to characterize sagebrush habitat: 1) multispectral (this repo), 2) <a href='https://github.com/kessb/sagebrush-ecosystem-modeling-hyperspectral/'>hyperspectral</a> and 3) <a href='https://github.com/sarahmjaffe/sagebrush-ecosystem-modeling'>lidar</a>.  Using easy to follow, reproducible workflows, this series of repos is designed to assess which products land and wildlife managers might want to invest time and possible money into for larger-scale surveys where *insitu* isn't sufficient.    

# Sagebrush Ecosystem Modeling with Landsat 8

This repository contains workflows that specifically explore the ability of 30m<sup>2</sup> resolution multispectral imagery to primarily answer:

*Are widely available, free, course resolution images able to sufficiently characterize sagebrush habitats in the western United States?**

It will produce workflows that enable automation to retrieve data and analyze classes through spectral unmixing in order to represent the heterogeneous habitat more realistically (visualizing diversity within 30m<sup>2</sup>). The objective of this repository as it currently is presented is to determine the percent coverage of classes across an area of interest.  

# Relevance
Sagebrush ecosystems cover much of the western United States and parts of southwestern Canada. Sagebrush ecosystems provide essential forage and habitat for approximately 350 other species of plants an animals, some of which, like the Greater Sage Grouse, are found only in sagebrush habitat. Sagebrush ecosystems are increasingly fragmented through anthropogenic land use, invasive species, and changes in wildfire duration and frequency which are amplified by climate change. While sagebrush still covers much of the western United States, only 10% of current habitats are considered unaffected by fragmentation. Consequently, many plants and animals associated with sagebrush are losing essential habitat and some qualify as endangered or threatened species per the Endangered Species Act. Conservation efforts targeted to sagebrush ecosystems are costly as they require the surveillance and upkeep of millions of acres of public and private land.

This repository offers an alternative to traditional land monitoring strategies through its unique focus on and analyses of sagebrush ecosystems. We expect this code to be useful to other analysts because of its reproducible foundation, which will allow it to be applied to other research areas. While we are using it here to examine sagebrush habitat, the same processes can be run on other sites covered by the aforementioned agencies, allowing versatile analyses of vegetation structure and composition across the United States.

# Workflow Requirements
First, all notebooks will require the packages in the landsat-unmixing-env.yml.  This environment can be downloaded and activated locally, but be forewarned, it is quite a large file.  

Second, the workflow of most immediate interest is the unsupervised spectral unmixing.  This notebook (#3 in the Repo Organization table below) is completely reproducible as is, however, there are many other notebooks that may be of interest.  

At the moment, please consider this repo a work-in-progress.  It will be updated regularly.  Plans include making sure all examples are 100% reproducible, making all notebooks PEP8 compliant, processes and results thoroughly described through markdown cells, and adding several needed functions.  

## Repo Organization

| SUBDIRECTORY                                                                                                     	| FILE                                                                                 	| PURPOSE                                                                                                                                                                                	| STATUS                                                   	|
|---------------------------------------------------------------------------------------------------------------	|--------------------------------------------------------------------------------------	|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|----------------------------------------------------------	|
| modules: Independent functions that can be called in any notebook                                             	| 1) retrieve-landsat8-level1-scenes.ipynb                                             	| Uses an aoi and dates to retrieve level-1 Landsat 8 scenes                                                                                                                             	| Completed                                                	|
|                                                                                                               	| 2) retrieve-NEON-site-boundary.ipynb                                                 	| Accesses NEON's polygons of site boundaries used in the workflows                                                                                                                      	| Completed                                                	|
| notebooks: Workflows of processing and analysis                                                               	| 3) Unsupervised-Spectral-Unmixing.ipynb                                              	| Uses downloadable input (cropped, stacked level-2 Landsat 8 image) to run through unsupervised spectral unmixing                                                                       	| Needs markdown and Pep8 clean-up                         	|
| notebooks/examples: [Will be] reproducible workflows showing how everything works with downloaded source data 	| 4) Find-Overlapping-Landsat-Scenes.ipynb                                             	| Showcases: retrieve-landsat8-level1-scenes and retrieve-NEON-site-boundary functions Uses importable input (AOI polygon) to identify and download level-1 Landsat 8 scenes of interest 	| Needs editing for reproducibility, markdown and clean-up 	|
|                                                                                                               	| 5) Kmeans-Unsupervised-Classification.ipynb                                          	| Uses downloadable input (cropped, stacked level-2 Landsat 8 image) to run through unsupervised pixel-sized classification                                                              	| Needs editing for reproducibility, markdown and clean-up 	|
|                                                                                                               	| 6) Landsat8-cropped-and-stacked.ipynb                                                	| Uses importable input (AOI polygon) and a pre-downloaded level-2 Landsat 8 scene to create a cropped, stacked numpy array                                                              	| Needs editing for reproducibility, markdown and clean-up 	|
| notebooks/testing: Workflows still being tested and worked through                                            	| Ignore these for now.  Once working, they will be moved to the appropriate directory 	| NA                                                                                                                                                                                     	| NA                                                       	|


## Data Sources
Data is sourced from the National Ecological Observatory Network's <a href='https://www.neonscience.org/data/about-data/spatial-data-maps'>(NEON)</a>, Landsat 8 images courtesy of <a href='https://earthexplorer.usgs.gov/'>U.S. Geological Survey</a> and their <a href='https://earthexplorer.usgs.gov/Spectral'>Spectral Library Version 7</a>.  See table below for more details.

| SOURCE                	| PURPOSE                              	| DATA TYPE                                           	|
|-----------------------	|--------------------------------------	|-----------------------------------------------------	|
| NEON                  	| AOIs                                 	| shapefiles (polygons)                               	|
| USGS EARTH EXPLORER   	| Level-1 and Level-2 Landsat 8 scenes 	| GeoDataFrames (7 bands, 30m<sup>2</sup> resolution) 	|
| USGS Spectral Library 	| Spectral signatures                  	| text files                                          	|
|                       	|                                      	|                                                     	|

# Acknowledgements
This series of repos is a collaborative effort between NatureServe, Kelsey Beckrich and Sarah Jaffe.  It was completed as a part of University of Colorado Boulder's Earth Analytics course series, and was guided by Dr. Jenny Palomino, data science faculty at University of Colorado Boulder's Earth Lab.

Other sources that contributed code or ideas (most of which can be found forked in this repo):

1) Bruno Ruas de Pinho's <a href='http://geologyandpython.com/'>blog</a>: Automating Landsat 8 retrieval and TOA calculations

2) Katy Sill's flood detection <a href='https://github.com/katysill/flood-detection'>repo</a>: Unsupervised kmeans classification

3) Joseph McGlinchy's Earth Lab <a href='https://github.com/earthlab/neon-headwall-data'>repo</a>: Unsupervised spectral unmixing

4) K. Arthur Endsley's <a href='https://github.com/arthur-e/unmixing/tree/master/docs'>repo</a>: Supervised spectral unmixing

A tremendous thank you to all involved directly or indirectly.
