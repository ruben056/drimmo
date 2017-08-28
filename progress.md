Progress
========


TODO
----
* create framework for importing data (Loader)
** READER/parsers for instance csv READER
** WRITER for instance mongodbwriter

Base this stuff on the idea of te xml pipelines at Sofico
but use JSON instead. Also add a optional debugWriter Decorator to be added
ad hoc in the pipeline to output the intermediate result of each stage of the transformation in a debug/log folder somewhere ...

With first implementation:
import cities from csv from http://portal.openbelgium.be/ne/dataset/gemeentecodes/resource/f20e9b3b-d5f9-4041-a5cc-8e7f70fa3e39
*CityLoader* with the
--> *OpenBelgiumCitiesReader with generics stuff in CSVReader*
--> *CitiesDBWriter with generic stuff in MongoDBWriter*

* load date from immoweb
** Create READER/parser/crawler to retrieve/scrape info from immoweb with generic stuff in webReader or something.
** Create UnitDBWriter with generic stuff in mongodbwriter

DONE
----
* defined initial requirements for short term prototype
* created git repo

