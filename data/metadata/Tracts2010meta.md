- `Title`: Tracts2010
- `Abstract`: census tracts from the 2010 Census for Chicago containing with demographic data joined from the P2 
- `Spatial Coverage`: The city of Chicago, Illinois
- `Spatial Resolution`: Tracts
- `Spatial Reference System`: EPSG 6454
- `Temporal Coverage`: Specify the temporal extent of your study---i.e. the range of time represented by the data observations.
- `Temporal Resolution`: 2010
- `Lineage`: Data was downloaded from Middlebury College Geog 120 Week 04 Lab: Urban Models of Segregation by Race and Class which collected the data from Steven Manson, Jonathan Schroeder, David Van Riper, and Steven Ruggles. IPUMS National Historical
Geographic Information System: Version 13.0 [Database]. Minneapolis: University of Minnesota. 2018. http://doi.org/10.18128/D050.V13.0.
- `Distribution`: Data is available 
- `Constraints`: Legal constraints for *access* or *use* to protect *privacy* or *intellectual property rights*
- `Data Quality`: State any planned quality assessment
- `Variables`:

- For each variable, enter the following information. If you have two or more variables per data source, you may want to present this information in table form (shown below)
  - `Label`: variable name as used in the data or code
  - `Alias`: intuitive natural language name
  - `Definition`: Short description or definition of the variable. Include measurement units in description.
  - `Type`: data type, e.g. character string, integer, real
  - `Accuracy`: e.g. uncertainty of measurements
  - `Domain`: Expected range of Maximum and Minimum of numerical data, or codes or categories of nominal data, or reference to a standard codebook
  - `Missing Data Value(s)`: Values used to represent missing data and frequency of missing data observations
  - `Missing Data Frequency`: Frequency of missing data observations: not yet known for data to be collected

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










