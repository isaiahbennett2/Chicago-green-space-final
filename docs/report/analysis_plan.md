# Reproduction of Urban Environmental Justice of Green Space Access in Chicago
### Authors

- Isaiah Bennett

### Abstract

This study is a *reproduction* of:

The lab called "Urban Environmental Justice of Green Space Access in Chicago" from Middlebury College's Human Geography with GIS class. 

The abstract of the original study is as follows: 

Green space provides numerous public health, social, and environmental benefits to cities and their residents. These include
mitigation of urban heat, improved stormwater management and water quality, improved air quality, expanded access to
exercise, and the social-psychological benefits of enjoying nature.

In this lab, we will conduct a GIS study similar to Wolch, Wilson and Fehrenbach's (2005) research on access to green
spaces in Los Angeles, California. Wolch et al's purpose was to assess the environmental justice implications of municipal
green spaces and recreation funding policies (Proposition K), asking whether minority groups, and especially minority
children, were disproportionately excluded from access to green spaces. They operationalized the concept of "access" in
terms of both the proximity and the total area of green spaces, and found significant disparities between racial/ethnic
groups, rooted in histories of bias and segregation.

Our purpose is to assess people's access to green space (parks and forests) in segregated neighborhoods of Chicago. To do
so, we will estimate indicators of access to green space according to regions where Asian, Black, Latinx, or White
ethnic/racial groups are the majority (60% of the population or more), and Mixed neighborhoods where no single group
makes up 60% or more of the population. The indicators of green space access are:

• Percentage of people living within 0.25 miles of a green space

• Green space area per person (in square meters)
A graphical abstract of the study could also be included as an image here.

### Study metadata

- `Key words`: Comma-separated list of keywords (tags) for searchability. Geographers often use one or two keywords each for: theory, geographic context, and methods.
- `Subject`: select from the [BePress Taxonomy](http://digitalcommons.bepress.com/cgi/viewcontent.cgi?article=1008&context=reference)
- `Date created`: date when project was started
- `Date modified`: date of most recent revision
- `Spatial Coverage`: Specify the geographic extent of your study. This may be a place name and link to a feature in a gazetteer like GeoNames or OpenStreetMap, or a well known text (WKT) representation of a bounding box.
- `Spatial Resolution`: Specify the spatial resolution as a scale factor, description of the level of detail of each unit of observation (including administrative level of administrative areas), and/or or distance of a raster GRID size
- `Spatial Reference System`: Specify the geographic or projected coordinate system for the study, e.g. EPSG:4326
- `Temporal Coverage`: Specify the temporal extent of your study---i.e. the range of time represented by the data observations.
- `Temporal Resolution`: Specify the temporal resolution of your study---i.e. the duration of time for which each observation represents or the revisit period for repeated observations
- `Funding Name`: name of funding for the project
- `Funding Title`: title of project grant
- `Award info URI`: web address for award information
- `Award number`: award number

#### Original study spatio-temporal metadata

- `Spatial Coverage`: The city of Chicago, Illinois
- `Spatial Resolution`: Tracts
- `Spatial Reference System`: EPSG 6454
- `Temporal Coverage`: Decennial census
- `Temporal Resolution`: 2010

## Study design

This study is a reproduction study of an unpublished geography study that was made for Middlebury College's Human Geography with GIS class to be done in QGIS. I completed the study last spring when I was in the course Human Geography with GIS, but wanted to revisit it through a computational environment to contribute to the world of reproducible science. Since this is not a computationally intensive study, its purpose is to act as a simple example to show new GIScientists what the world of reproduction lools like by demonstrating easily digestible components of reproducible research such as making a preanalysis plan (preregistration), setting up a reproducible computational environment, sharing data and metadata, sharing methods and code, working through a reproduction study notebook, and exploring a research compendium. 

The main research question at hand is to see if this QGIS study can be accurately reproduced using python packages such as GeoPandas and Pandas.

## Materials and procedure

### Computational environment

This study will be conducted on a MacBook Air 2022 on MacOS 13.5.2 using Jupyter Labs. Packages loaded in the study include pyhere, pandas, geopandas, folium, branca.colormap, matplotlib.pyplot, and matplotlib.patches

### Data and variables

#### Tracts2010

**Standard Metadata**

- `Title`: Tracts2010.shp
- `Abstract`: census tracts from the 2010 Census for Chicago containing with demographic data joined from the P2 
- `Spatial Coverage`: The city of Chicago, Illinois
- `Spatial Resolution`: Tracts
- `Spatial Reference System`: EPSG 6454
- `Temporal Coverage`: 
- `Temporal Resolution`: 2010
- `Lineage`: Data was downloaded from Middlebury College Geog 120 Week 04 Lab: Urban Models of Segregation by Race and Class which collected the data from Steven Manson, Jonathan Schroeder, David Van Riper, and Steven Ruggles. IPUMS National Historical
Geographic Information System: Version 13.0 [Database]. Minneapolis: University of Minnesota. 2018. http://doi.org/10.18128/D050.V13.0.
- `Distribution`: Data is available 
- `Constraints`: No legal constraints
- `Data Quality`: No planned quality assessment

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| fid| :--: | object id | int
| STATEFP10| :--: | state id | int
| COUNTYFP10| :--: | county id | int
| TRACTCE10| :--: | tract id | int
| GEOID10| :--: | geography id | int
| NAME10| :--: | ? |  int
| NAMELSAD10| :--: | census tract name | string 
| GISJOIN| :--: | uniquely identifies tracts for purpose of joining to geographic data | string
| PopTotal| :--: | total population |  int
| Latinx| :--: | total Hispanic or Latino/Latina population | int
| NotLatinx| :--: | total non-Hispanic White population | int
| White| :--: | total non-Hispanic White population | int
| Black| :--: | total non-Hispanic Black or African American population | int
| Asian| :--: | total non-Hispanic Asian population | int
| TwoOrMore| :--: | ? | int
| MedHouseVa| :--: | median house value for owner-occupied houses | int
| MedGrossRe| :--: | median gross monthly rent (including utilities) | int
| pctWhite| :--: | percent white population | double
| pctBlack| :--: | percent black population | double
| pctLatinx| :--: | percent latinx population | double
| pctAsian| :--: | percent asian population | double

#### Blocks 2010

**Standard Metadata**

- `Title`: Blocks2010.shp
- `Abstract`: census blocks from the 2010 Census for Chicago containing with demographic data joined from the P2
- `Spatial Coverage`: The city of Chicago, Illinois
- `Spatial Resolution`: Block groups
- `Spatial Reference System`: EPSG 6454
- `Temporal Coverage`: Specify the temporal extent of your study---i.e. the range of time represented by the data observations.
- `Temporal Resolution`: 2010
- `Lineage`: Data was downloaded from Middlebury College Geog 120 Week 07 Lab which collected the data from Steven Manson, Jonathan Schroeder, David Van Riper, and Steven Ruggles. IPUMS National Historical
Geographic Information System: Version 13.0 [Database]. Minneapolis: University of Minnesota. 2018. http://doi.org/10.18128/D050.V13.0.
- `Distribution`: Data is available 
- `Constraints`: No legal constraints
- `Data Quality`: No planned quality assessment

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| GEO.id | ... | Id | string | ... | ... | ... | ... |
| GEO.id2 | ... | Id2 | string | ... | ... | ... | ... | 
| GEO.display-label | ... | Geography | geometry | ... | ... | ... | ... |
| D001 | ... | Total Population | int | ... | ... | ... | ... |
| D002 | ... | Hispanic or Latino | int | ... | ... | ... | ... |
| D003 | ... | Not Hispanic or Latino | int | ... | ... | ... | ... |
| D004 | ... | Not Hispanic or Latino: - Population of one race | int | ... | ... | ... | ... |
| D005 | ... | Not Hispanic or Latino: - White alone | int | ... | ... | ... | ... |
| D006 | ... | Not Hispanic or Latino: - Black or African American alone | int | ... | ... | ... | ... |
| D007 | ... | Not Hispanic or Latino: - American Indian and Alaska Native alone | int | ... | ... | ... | ... |
| D008 | ... | Not Hispanic or Latino: - Asian alone | int | ... | ... | ... | ... |
| D009 | ... | Not Hispanic or Latino: - Native Hawaiian and Other Pacific Islander alone | int | ... | ... | ... | ... |
| D010 | ... | Not Hispanic or Latino: - Some Other Race alone | int | ... | ... | ... | ... |


#### Parks

**Standard Metadata**

- `Title`: parks.shp
- `Abstract`: parks in Chicago
- `Spatial Coverage`: The city of Chicago, Illinois
- `Spatial Resolution`: park polygons 
- `Spatial Reference System`: EPSG 6454
- `Temporal Coverage`: Specify the temporal extent of your study---i.e. the range of time represented by the data observations.
- `Temporal Resolution`: 2010
- `Lineage`: Data was downloaded from Middlebury College Geog 120 Week 07 Lab Urban Environmental Justice of Green Space Access in Chicago
- `Distribution`: Data is available 
- `Constraints`: No legal constraints
- `Data Quality`: No planned quality assessment

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| parkName | :--: | names of every park in Chicago | string |


#### Forests

**Standard Metadata**
​
- `Title`: forest.shp
- `Abstract`: forest areas in Chicago
- `Spatial Coverage`: The city of Chicago, Illinois
- `Spatial Resolution`: forest polygons
- `Spatial Reference System`: EPSG 6454
- `Temporal Coverage`: Specify the temporal extent of your study---i.e. the range of time represented by the data observations.
- `Temporal Resolution`: 2010
- `Lineage`: Data was downloaded from Middlebury College Geog 120 Week 07 Lab Urban Environmental Justice of Green Space Access in Chicago
- `Distribution`: Data is available 
- `Constraints`: No legal constraints
- `Data Quality`: No planned quality assessment 

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
|  NAME | :--: | single multi part polygon with all forest areas | string | 

### Prior observations  

This is a reproduction study and I have already seen and conducted this study in QGIS.  

### Bias and threats to validity

**Boundary Effects:** Restricted to the extent of the city of Chicago the hard boundary of the city’s border could cut off people along the edges who might access a park within 0.25 miles outside of the city making it seem like they have less access to green space than people within the city.

**Modifiable Aerial Unit Problem:** The population with access to green space is calculated based on block groups which is one of the smallest enumeration units.  This decreases the chances that diversity in spatial trends is generalized. The racial majority groups are calculated at the tract level, however, which might ignore varying trends between racial majority groups at the block group level.

**Spatial Heterogeneity:** This poses an issue when looking at the differences in greenspaces. Not all greenspaces have the same amenities or quality for their communities to access–just because it technically counts as a greenspace does not mean it has the same inherent value as other greenspaces. The size of the greenspace presents a parallel problem. Since access to greenspace is determined by a constant buffer of 0.25 miles it does not account for the fact that smaller spaces can reach more people proportionally to the size of the green space. Perhaps smaller green spaces should have a smaller buffer since they do not have a proportional capacity of use when compared to larger parks with the same 0.25-mile buffer.


### Data transformations

The first data transformation is joining the parks and forests shapefiles since they come from different sources but together represent the total green space of Chicago. 

The construction of a new variable, the majority group column, in the tract data frame must also be calculated to continue with the analysis. The majority group is calculated by a threshold of 60% population, so if a tract has a single-race population percentage over 60% then it is given the designation of that race. Only White, Black, Asian, and Latinx are considered in this study as they were the most dominant in Chicago in 2010. The 60% threshold is a seemingly arbitrary choice in the original study design and could be modified to see how it influences the final results.  

### Analysis
First, the green space will be buffered by 0.25 miles to create a catchment area to show which blocks are able to access it easily. Using a spatial overlay, blocks with access will be selected if their centroids intersect with the green space buffer. These access blocks containing population data will then be aggregated to the tract level based on their tract id. Population data for each tract is then summed based on their racial majority group. Area calculations are made for the total area that each majority group inhabits, and then subsequently after a clip overlay that selects all of the green space area that overlaps their tracts. Variables of Percent of Population with Access and Green Space Per Person (sqm) are also derived from existing variables.


## Results

Results will be presented through a single choropleth map that represents the racial majority groups of tracts with green spaces overlayed, and a table that shows the values for Population, Population with Access, Area (sqm), Green Space Area (sqm), Percent Population with Access, and Green Space Per Person (sqm). 

## Discussion

Results will be interpreted based on differences between majority groups to see if there is any demographic that has a disproportionate lack of access to green space. This will be shown most clearly by the Percent of Population with Access and Green Space per Person so that it is standardized for each population. 

## Integrity Statement
The authors of this preregistration state that they completed this preregistration to the best of their knowledge and that no other preregistration exists pertaining to the same hypotheses and research.


## Acknowledgements

- `Initial help`: Tate Sutter and I were originally going to work on this together, therefore he contributed to the initial steps of writing the requirements txt to set up the computational environment as well as loading in the the tracts2010 data. Everything after will be conducted by me, Isaiah Bennett.  

This report is based upon the template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences, DOI:[10.17605/OSF.IO/W29MQ](https://doi.org/10.17605/OSF.IO/W29MQ)

## References
