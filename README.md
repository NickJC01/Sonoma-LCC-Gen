Welcome to our Sonoma County Land-Cover Classification Project. This was a project authored by Broderick Noyes, and Nicholas Slankard, and myself. This project sought to generate accurate land-cover-classifications to a 10-meter pixel map of the entirety of Sonoma County. We sought to do this accurately utilizing only the 64 GEE Embeddings provided by Google without any other supplementary data, implementing a variety of neural networks and computer vision models to do so. 

This project was run on Google Colab, and includes Drive Mounting and Google Earth Engine imports. If you do not have access to our shared drive, the mounting will not work. However, the purpose of the drive mounting is to be able to reference our data with paths. You should be able to run our code on your own drive or local machine by changing the paths accordingly. Many of our models have a cell that looks like this:

_

import ee


ee.Authenticate()
ee.Initialize(project='sonoma-lcc')

_

‘sonoma-lcc’ is a GEE project only we have access to, so this cell will likely return an error. However, only our Infrastructure code really needs this cell, and our models can still be run by skipping it.

The code directory has copies of all of our relevant code files. 
You can also find our code in these directories:

models - Our latest tested models, most of which still have the latest test results on display.

Infrastructure - How we got and formatted the parquet data from GEE. This contains:
Drive Mounting Block (To connect Colab with our shared drive)
Tile generation code (Generates tif tiles from label shapefile & GEE embeddings)
Parquet generation  code (Generates the parquet files by combining the GEE and label tif files
EMB Parquet generation code (Generates parquet files from just GEE embeddings, no labels)

