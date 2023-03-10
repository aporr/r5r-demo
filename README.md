# A Sense of Place: Quick and Dirty Accessibility Analysis Using Open Source Network Analysis Tools

## Author's notes

This repository was created in support of a presentation at the [2022 Ohio GIS Conference](https://gis1.oit.ohio.gov/ogrip/2022OhioGISConferenceAgenda.htm) on September 21, 2022.  For me this represented an opportunity and motivation to learn about a spatial analysis tool that I had not had the opportunity to use previously, namely the [r5r](https://ipeagit.github.io/r5r/) package for the R programming language. This package provides a very simple means of generating multimodal transportation networks based on OpenStreetMap data and GTFS data from transit agencies (among other inputs) and analyzing those networks.  

The presentation was intended to demonstrate the capabilities of the tool from a novice's perspective.  The example use cases presented are contrived applications intended for this purpose alone.  They do not represent rigorous analyses and should not be used for any purpose other than their intended purpose.

The demonstration analyses were implemented using Jupyter notebooks. Network generation and analysis was carried out using a R kernel (as required by the r5r package), but the remaining parts were carried out using the Python kernel.  This was mostly a matter of efficiency and preference since I prefer Python and am more familiar with it.  The entirety of the analysis could have been carried out using R instead.

## Abstract

How many residents live within cycling distance of the planned community center? What are the economic characteristics of the neighbors within walking distance of this library? How many more jobs can a person reach in 30 minutes if we put a bikeshare station at this bus stop? It used to be that answering location intelligence questions like these was expensive and time consuming, but thanks to a suite of open source software and open data, you can answer these and countless other questions that require analysis of complex geospatial networks for free in minutes. In this presentation we'll demonstrate how to use the r5r package for the popular R programming language to build a multi-modal transportation network for Central Ohio from scratch and use it to model some impacts of a large hypothetical industrial development in Licking County.

## Key resources

  - README.md (this file)
  - Presentation slides ([PDF](https://github.com/aporr/r5r-demo/blob/main/A%20Sense%20of%20Place.pdf) | [PowerPoint](https://github.com/aporr/r5r-demo/blob/main/A%20Sense%20of%20Place.pptx))
  - [Step 1 - Prepare input data.ipynb](https://github.com/aporr/r5r-demo/blob/main/Step%201%20-%20Prepare%20input%20data.ipynb) ([HTML export](https://github.com/aporr/r5r-demo/blob/main/Step%201%20-%20Prepare%20input%20data.html))
  - [Step 2 - Network analysis.ipynb](https://github.com/aporr/r5r-demo/blob/main/Step%202%20-%20Network%20analysis.ipynb) ([HTML export](https://github.com/aporr/r5r-demo/blob/main/Step%202%20-%20Network%20analysis.html))
  - [Step 3 - Final analysis.ipynb](https://github.com/aporr/r5r-demo/blob/main/Step%203%20-%20Final%20analysis.ipynb) ([HTML export](https://github.com/aporr/r5r-demo/blob/main/Step%203%20-%20Final%20analysis.html))

## Analysis procedure

If you wish to reproduce the analysis, do the following in order:

  1. Install [Python](https://www.python.org/) (I used 3.10)
  1. Install [R](https://www.r-project.org/) (I used 4.2.1)
  1. Install the [Python Jupyter package](https://jupyter.org/install) (Jupyter Lab or Jupyter Notebook). 
  1. Install [IRkernel](https://irkernel.github.io/installation/) (R support for Jupyter)
  1. Review each of the Jupyter notebooks listed below and install all required Python packages (R packages should get installed automatically).
  1. Run [Step 1 - Prepare input data.ipynb](https://github.com/aporr/r5r-demo/blob/main/Step%201%20-%20Prepare%20input%20data.ipynb) to download the required input data and prepare it for the analysis.
  2. Run [Step 2 - Network analysis.ipynb](https://github.com/aporr/r5r-demo/blob/main/Step%202%20-%20Network%20analysis.ipynb) to generate the network and produce travel time matrices.
  3. Run [Step 3 - Final analysis.ipynb](https://github.com/aporr/r5r-demo/blob/main/Step%203%20-%20Final%20analysis.ipynb) to complete the analysis and generate the visualizations.

## References

I found the following references useful when learning how to use r5r.

  1. [r5r: Rapid Realistic Routing with R5 in R](https://ipeagit.github.io/r5r/) (Project website)
  1. [Intro to r5r: Rapid Realistic Routing with R5 in R](https://ipeagit.github.io/r5r/articles/r5r.html) (Vignette with multi-modal routing example using sample data)
  1. [r5r: Rapid Realistic Routing on Multimodal Transport Networks with R5 in R](https://findingspress.org/article/21262-r5r-rapid-realistic-routing-on-multimodal-transport-networks-with-r-5-in-r) (Published article with accessibility analysis example using sample data)
  1. [Calculating and visualizing Accessibility](https://ipeagit.github.io/r5r/articles/calculating_accessibility.html) (Vignette with accessibility analysis example using sample data)