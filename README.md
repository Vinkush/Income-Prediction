# Income-Prediction
Predicting income of groups of population using demographic data

## Background about the firm
Asteri Home is an American home improvement chain that operates domestically, providing home renovation and repair services via Asteri Home service points and supplying DIY and home improvement tools and products in the Asteri Depot retail stores. The management team at Asteri has decided to expand their business to the Canadian market and sought consultation from the Greek Star consulting firm for market entry strategy.


## The Data

The underlying data set was extracted from data provided by Statistics Canada.

Census tracts (CTs) are small, relatively stable geographic areas that usually have a population between 2,500 and 8,000 persons. They are located in census metropolitan areas and in census agglomerations that had a core population of 50,000 or more in the previous census.

A committee of local specialists (for example, planners, health and social workers, and educators) initially delineates census tracts in conjunction with Statistics Canada. Once a census metropolitan area (CMA) or census agglomeration (CA) has been subdivided into census tracts, the census tracts are maintained even if the core population subsequently declines below 50,000.
For each CT record, there are fourteen attributes, and one output variable. 

The training data set is CensusCanadaTraining.csv and contains all the fields for 5,000 records. The test data set is CensusCanadaTest.csv; it contains 721 records, and is missing the median income field.

## Our Approach

The data science team from Greek Star Consulting utilizes the census tract data from Statistics Canada and analyzes the socioeconomic characteristics relevant to home improvement, including income, population, housing, and construction attributes. 

Using K-Means clustering, 5000 census tracts in the training set are partitioned into 4 clusters. After profiling the clusters based on their unique socioeconomic attributes, three clusters are found suitable for market entry and one cluster is identified as low priority segment that contains too many unfavourable attributes. 

Cluster #3 is primary focus cluster that is suitable for operating both lines of businesses (services and retail stores), since there’re more owner-occupied aged residential buildings. With the same logic, it is recommended to first focus on only the renovation and repair services for Cluster #2 and retail stores for Cluster #4 respectively. 

The team then excludes the income variable from the training data and applies K-Means clustering to generate a new set of clusters for predicting median household income per year for the census tracts. Three prediction models are experimented on the clusters, including K-Nearest Neighbours algorithm (KNN), Classification and Regression Tree (CART), and Random Forest. A combination of models that perform the best for the clusters is identified and used for income prediction on the test dataset.
