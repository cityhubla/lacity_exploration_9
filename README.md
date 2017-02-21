# lacity_exploration_9
Comparing LACITY Open Data with Official Reports

* This exploration looks at data reported in the Aug 25, 2016 Quarterly Status Report of [Mayor Garcetti's Executive Directive 13, Support for Affordable Housing](http://www.lamayor.org/mayor-garcetti%E2%80%99s-executive-directive-13-support-affordable-housing).
* The status report, addresses the Mayor's goal of permitting 100,000 new housing units by 2021 as there are not enough housing to keep up with the demand in one of the nation's most expensive metropolitan regions.
* Can open data be used to reach the numbers as reported by the Mayor's Office?
  * Open data can only go so far in analysis due to the limited information municipal goverments are willing to give in the public datasets. This may be due to an issuing department's concerns of the quality of the data, or their unawareness of the need for more detailed datasets.
  * The methods outlined here may or may not arrive to the official numbers, and documenting them here on github invites others to participate in testing out alternative ways and try other datasets that could reach a more accurate representation of the housing status in the City of Los Angeles.
  * In the end, it's not about the results but to see if citizens, academics and professionals can use open data in support of improving the quality of information published by municipal governments.

##Open Data Sources
* Building and Safety Permit Information from the [LACITY Open Data Portal](https://data.lacity.org) | Issued by the Department of Building and Safety | Last Updated Aug 15, 2016 | [Link to full permit dataset](https://data.lacity.org/A-Prosperous-City/Building-and-Safety-Permit-Information/yv23-pmwf)
  * Note: Permit issue dates start at 1/01/2013 to 8/11/2016
  * This dataset contains building permits, electrical permits, and mechanical permits.
  * Copy of full dataset from this update can be downloaded in this repo.
 
##Reports and other prepared datasets
* [US Census Building Permits Survey](https://www.census.gov/construction/bps/) | The data provides the number of housing units authorized by building permits
 * Data for LA city can be found on this repo.
* [Los Angeles Department of Building and Safety Newsletters](http://ladbs.org/forms-publications/publications/newsletter)
* Annual Element Progress Report, Housing Element Implementation | 
 * [2010](http://cityplanning.lacity.org/HousingInitiatives/HousingElement/Final/APR_2010_Final.pdf) | [2011](http://cityplanning.lacity.org/PolicyInitiatives/Housing/ProRept/APR2011.pdf) | [2012](http://planning.lacity.org/PolicyInitiatives/Housing/ProRept/APR2012.pdf) | [2013](http://cityplanning.lacity.org/PolicyInitiatives/Housing/ProRept/APR2013.pdf) | [2014](http://cityplanning.lacity.org/PolicyInitiatives/Housing/ProRept/APR2014.pdf)
 * Previous years can be found at the [California Department of Housing and Community Development](http://www.hcd.ca.gov/regulations/)
 
##Explorations and methods
###Total Dwelling Units reported in Building Permits

**9.1.2016**

The mayor's office published status report on 8.25.2016 indicated that since July 1, 2013 to June 30th 2016, the city has issued permits for 40,805 dwelling units. Further research with other reports data sources come close to the reported total, this includes:
* 40,911 - LADBS Newsletters
* 40,100 - Census Building Permits Survey

Raw permit data is published on the city's data portal, which has a terrific detailed breakdown of permits by address, permit type, description and it also includes geocoordinates for mapping. There is opportunities for further analysis on a local level which can include totals by Council District, Community Plan, Neighborhood Council. The geocoordinates can be used to generate maps for additional inquiry.

**9.2.2016**

The raw data is filtered by Fiscal Year, so its consistent with the reports. Using the socrata platform, the data was filtered using:
* `Permit Type` is `Bldg-New`
* `Issue Date` is after `End Fiscal Year`
* `Issue Date` is before `Start Fiscal Year`
* `# of Residential Dwelling Units` is greater than `0`

Filtered results in comparison to reported totals. Also included is the number of building permits (All types) issued. Links to raw results.
* [FY 2013](https://data.lacity.org/A-Prosperous-City/Dwelling-Units-FY-2013/dkug-ccem)
* [FY 2014](https://data.lacity.org/A-Prosperous-City/Dwelling-Units-FY-2014/ah75-kk4t)
* [Fy 2015](https://data.lacity.org/A-Prosperous-City/Dwelling-Units-FY-2015/n22z-viyx)

| Data Comparison of LACITY Reports with Open Data |  |  |  |  |  |
|---------------------------------------------------------|----------------------|------------------|------------------|--------------------|--------------------|
|  |  |  |  |  |  |
| Note: A fiscal year (FY) begins in July 1st - June 30th |  |  |  |  |  |
|  | Dwelling Units | Dwelling Units | Permits Issued | Permits Issued | Dwelling Units |
|  | 8/2016 Status Report | LADBS Newsletter | LADBS Newsletter | LACITY Data Portal | LACITY Data Portal |
| 2014 Fiscal Year |  |  |  |  |  |
| FY14Q1 | 1,665 |  |  |  |  |
| FY14Q2 | 2,977 |  |  |  |  |
| FY14Q3 | 3,247 |  |  |  |  |
| FY14Q4 | 3,146 |  |  |  |  |
| FY14TOTAL | 11,035 | 11,035 | 134,000 | 130,180 | 9,879 |
|  |  |  |  |  |  |
| 2015 Fiscal Year |  |  |  |  |  |
| FY15Q1 | 2,580 |  |  |  |  |
| FY15Q2 | 3,420 |  |  |  |  |
| FY15Q3 | 4,518 |  |  |  |  |
| FY15Q4 | 4,376 |  |  |  |  |
| FY15TOTAL | 14,894 | 15,000 | 141,000 | 137,794 | 13,765 |
|  |  |  |  |  |  |
| 2016 Fiscal Year |  |  |  |  |  |
| FY16Q1 | 3,819 |  |  |  |  |
| FY16Q2 | 4,523 |  |  |  |  |
| FY16Q3 | 3,470 |  |  |  |  |
| FY16Q4 | 3,064 |  |  |  |  |
| FY16TOTAL | 14,876 | 14,876 | 157,000 | 153,061 | 13,756 |
| Total | 40,805 | 40,911 | 432,000 | 421,035 | 37,400 |

## sectionla
This exploration is part of [section.la] (https://github.com/cityhubla/sectionla/blob/master/README.md), a collection of maps and data visualizations exploring Southern California, one section at a time. 

The analysis, maps and code behind the explorations contribute to the services I offer as a consultant developing analog and digital tools and visualizations for Civic Engagement, Planning, Land Use Development and Public Policy. Think you could use my services?

Contact me Omar Ureta | [Twitter](https://twitter.com/theworksla) | Email : omaru[at]theworks.la | [Website](http://www.theworks.la/) | [linkedin](https://www.linkedin.com/in/omar-ureta-87195a55)

