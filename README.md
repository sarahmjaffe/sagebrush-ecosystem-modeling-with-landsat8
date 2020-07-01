# NOTE
This repo is a part of a collaborative series of repos that explores the ability of multiple products to characterize sagebrush habitat: 1) multispectral (this repo), 2) hyperspectral (*fill in Kelsey's repo*) and 3) <a href='https://github.com/sarahmjaffe/sagebrush-ecosystem-modeling'>lidar</a>).  Using easy to follow, reproducible workflows, this series of repos is designed assess which products land and wildlife managers might want to further invest time and possible money into for larger-scale surveys where *insitu* isn't sufficient.    

# Sagebrush Ecosystem Modeling with Landsat 8

This repository contains workflows that specifically explore the ability of 30m<sup>2</sup> resolution multispectral imagery to primarily answer:

*Are widely available, free, course resolution images able to sufficiently characterize sagebrush habitats in the western United States?**

It will produce workflows that enable automation to retrieve data and analyze classes through spectral unmixing in order to represent the heterogeneous habitat more realistically (visualizing diversity within 30m<sup>2</sup>). The objective of this repository as it currently is presented is to determine the percent coverage of classes across an area of interest.  Data is sourced from the National Ecological Observatory Network's <a href='https://www.neonscience.org/'>(NEON)</a>, Landsat 8 images courtesy of <a href='https://earthexplorer.usgs.gov/'>U.S. Geological Survey</a> and their <a href='https://earthexplorer.usgs.gov/Spectral'>Spectral Library Version 7</a>.

# Relevance
Sagebrush ecosystems cover much of the western United States and parts of southwestern Canada. Sagebrush ecosystems provide essential forage and habitat for approximately 350 other species of plants an animals, some of which, like the Greater Sage Grouse, are found only in sagebrush habitat. Sagebrush ecosystems are increasingly fragmented through anthropogenic land use, invasive species, and changes in wildfire duration and frequency which are amplified by climate change. While sagebrush still covers much of the western United States, only 10% of current habitats are considered unaffected by fragmentation. Consequently, many plants and animals associated with sagebrush are losing essential habitat and some qualify as endangered or threatened species per the Endangered Species Act. Conservation efforts targeted to sagebrush ecosystems are costly as they require the surveillance and upkeep of millions of acres of public and private land.

This repository offers an alternative to traditional land monitoring strategies through its unique focus on and analyses of sagebrush ecosystems. We expect this code to be useful to other analysts because of its reproducible foundation, which will allow it to be applied to other research areas. While we are using it here to examine sagebrush habitat, the same processes can be run on other sites covered by the aforementioned agencies, allowing versatile analyses of vegetation structure and composition across the United States.

# Workflow Requirements
## Tools and Packages


# Acknowledgements
This series of repos is a collaborative effort between NatureServe, Kelsey Beckrich and Sarah Jaffe.  It was completed as a part of University of Colorado Boulder's Earth Analytics course series, and was guided by Dr. Jenny Palomino, data science faculty at University of Colorado Boulder's Earth Lab.

Other sources that contributed code or ideas (most of which can be found forked in this repo):

1) Bruno Ruas de Pinho's <a href='http://geologyandpython.com/'>blog</a>: Automating Landsat 8 retrieval and TOA calculations.

2) Katy Sill's flood detection <a href='https://github.com/katysill/flood-detection'>repo</a>: Unsupervised kmeans classification

3) Joseph McGlinchy's Earth Lab <a href='https://github.com/earthlab/neon-headwall-data'>repo</a>

A tremendous thank you to all involved directly or indirectly.
