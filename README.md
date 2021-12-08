# BundestagSpeeches
Dataset containing speeches in the Bundestag from 7 September 1949 (1st period) to 24 October 2017 (18th period).
If possible, every speech is assigned a speaker and an ID corresponding to the pageid from the LegislatoR R package data.
By merging the two datasets, additional information on the speaker can be retrieved.
IDs are only present, if the speaker has been part of the German Bundestag in the corresponding period. For some minister this is not the case, which is why no ID was assigned.
The dataset does NOT contain speeches by the president of the Bundestag because of his entirely administrative position. Furthermore speeches of Staatssekretäre, Staatsminister, Bürgermeister, Ministerpräsidenten etc. have been removed. Those might be added in future versions of the data.
The text has already been converted to lowercase letters. Unfortunately, some small stopwords ("so","im","vom") had to be removed to enable the scraping process correctly.

# Data Collection
The data was collected by scraping the protocols of the Bundestag Session provided by the German Bundestag.
1. XML files were downloaded and parsed via Phython
2. After minor preprocessing steps, the speaker were identified by using regular expressions.
3. The data was merged with the data of the LegislatoR R package
4. Minor deviations were fixed manually


The data contains 367889 speeches, where 364962 have an assigned ID while 2927 haven't.
