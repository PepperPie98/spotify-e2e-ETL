# spotify-e2e-ETL
spotify api (src )→ extract data and deploy code to lambda → and store raw data in S3 

from S3 we do transformation using lambda and store in S3

use crawler to read metadata and inferschema and store in Data Catalog

use Athena to analyze data stored in Data Catalog

 

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/ce55dcec-a9ee-444a-876c-c299adafaa70/32b5cea1-6c0a-4183-80d1-62ad793bb499/Untitled.png)

In S3 we created 2 folders

1. raw data → 
    1. already processed
    2. to be processed 
2. transformed Data →
    1. album data
    2. artist data

to be processsed will have extract data from spotify playlist

which will be processed by lamba to create files in album and artist data

after src files  in to be processed should be to moved already processed folder and then delete those srcfiles from to be processed folder

Later use GLue crawler to inferschema and metadata and load to GLue catalog

Connect to Athena to analyze from Glue catalog
