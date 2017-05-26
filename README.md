# Long tail recovery project for soils

THIS IS A DRAFT. PROJECT IS IN PRELIMINARY PHASE AND SUBJECT TO CHANGE AT ANYTIME.

## Purpose

The purpose of this project is to aggregate data sets related to soils research. This includes field surveys, field manipulation studies, and labortory experiments. 
The hope is that this will serve as an open community resource to uncover new mechansims and quantify effects related to soil processes that are globally generalizable.

This project is not a repository or data archive.
End users are responsible for complying with ALL data use policies, please check with the orginal archives and reposities to ensure you are complying with use policies.
Data repositiories with relatively unrestricted (citation/acknowledgement but no co-authorship requirements) reuse policies are prioritized for data scripting.

## How to contribute

There are three main ways to contribut to this project:
1) *Identify* data sets of interest
2) *Code* data processing scripts to ingest new data sets
3) *Review* submitted scripts for complience with larger data set

Once a data set is found please start an issue including full citation and link to the archived data, this should be updated and used to coordinate data migration from identification to fully processed.
Copy the data locally to a folder into 'repoData/\$PI\$year' but do not commit the data to the repository.
In the data folder, inlcude a README.txt with any notes about the data set (including a full citation and contact information for the data provider if possible).
Processing scripts should be submitted to [SoilDataR](https://github.com/ktoddbrown/soilDataR) via a pull request and filenames should follow the 'processData_\$PI\$year.R' format.

Contributers who identify, code and/or review will be acknowledged as co-authors during data set versioning milestones. Please ensure that your name, affiliation and role is correctly identified in the CONTRIBUTORS.txt file. 
Repository versions will be assigned DOIs.
Any manuscripts which use data aggregated here are asked to cite the appropreate version but are not required to list contributers as co-authors.

Data contributes are welcome, however the data set must be previously archived elsewhere with an assigned DOI.
Data providers are encouraged to collaborate with coders to ensure correct data ingestion.

## Open data calls
Below are active data calls that have reviewers interested in targeted data types for future manuscripts.

1) Labratory incubated soil respiration response to moisture manipulation. Reviewers: K Todd-Brown and B Bond-Lamberty

## Data permissions
Data sets with unrestricted reuse policies are priority incorperation in this project.
Data permissions and reuse are identified in the *Study* Table.
Data may be excluded from versioning due to data permissions and study authors are encouraged to check permissions before publication.

## License
The aggregation scripts here are licensed under XXX.

# Table structure
Currently there are 6 main tables in this data base. 
1) *Vocabulary* (measurement) table has measurement [measurement_ID, measurement_type, measurement_method]
2) *Field site* has [field ID, time (collection date), depth.min, depth.max, depth.unit, latitude, longitude, description]
3) *Field treatment* has [field treatment ID, type, quantiy, units, method]
4) *Lab* has [lab ID, individualName.givenName, individualName.surName, positionName, electronicMailAddress, onlineUrl, ORCID, organizationName] (labs are made up of organizations and personel)
5) *Lab treatment* has [lab treatment ID, type, quanity, units, method]
6) *Sample* has [sample ID, field ID, field treatment ID, lab ID, lab treatment ID, study ID, time, time unit, mesurement type, measurment value, measurement unit]
7) *Study* has [study ID, DOI, data permissions]


# References of interest

rOpenSci Project: https://ropensci.github.io/

R package for interacting with DataOne: https://jsta.github.io/2017/03/28/dataone.html

Five ways consortia can catalyse open science, Nature, 2017 http://www.nature.com/news/five-ways-consortia-can-catalyse-open-science-1.21706

National Data Service: http://www.nationaldataservice.org/
