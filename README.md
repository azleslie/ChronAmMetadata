# ChronAmMetadata
This repository contains a tidier and less redundant metadata file for the [Chronicling America project](https://chroniclingamerica.loc.gov/), as well as all the code used to produce it. It is intended in particular for any projects that require each page of newsprint data to correspond to only one metadata entry (web scraping, mapping, etc). Consolidation choices were made with this aim in mind.

Most of the consolidation choices merely remove a repeated entry when newspapers were listed twice for two different locations. (For example, the "Ceredo crescent." did not change locations from Virginia to West Virginia: it was published in what would become, over the course of its run, the newly-formed state of West Virginia.) Others reflect papers that were published in more than one location during their lifetime but remained stationary during the period for which Chronicling America has data. In some cases where a newspaper was indeed published in more than one location during the period for which data is available, however, I retained the entry for the most stable publishing location. (For example, the "The Chattanooga Daily Rebel." was published in Georgia and Alabama in addition to Tennessee, but the majority of the data comes from its tenure in Chattanooga, TN.) Chronicling America essays were consulted for all choices.

Error reporting is much appreciated.

Up to date as of October 21, 2018; the comment before `write.csv` indicates the sum to check for possible updates against.

## File Guide
**clean_paperdata_oct18.csv** Tidied metadata file for newspapers in Chronicling America.

**clean_paperdata+_oct18.csv** The same file as above but with two additional variables: latitude and longitude coordinates for the publishing location of each newspaper and the population according to the 1880 census for the publishing location of each newspaper with over 20,000 inhabitants.

**ChronAmMetadata.Rmd** Used to produce clean_paperdata_oct18.csv.