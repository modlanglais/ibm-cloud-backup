# IBM Cloud Backup Tool

A Python script to backup data from specific IBM Cloud services. If you are interested in having functionality for another service, please create a pull request.

:heart: -> To do

:yellow_heart: -> In progress

:green_heart: -> Complete

This tool is a work-in-progress. When the first iteration is complete, it will include the ability to backup data from the following services:
- Watson Assistant :green_heart: (workspaces, entities, intents)
- Discovery :green_heart: (documents from all collections, training data) >> Please note, this section may take quite some time depending on how many documents and collections you have.
- Cloud Object Storage :green_heart: (contents in every bucket)
- Kubernetes Clusters :heart:
- App ID :heart:
- Databases for PostgreSQL :heart:
- Databases for MongoDB :heart:

------
## Setup

### Dependencies:
- [Python3](https://www.python.org/downloads/)
- [python-dotenv](https://pypi.org/project/python-dotenv/)
- [ibm-cos-sdk](https://github.com/IBM/ibm-cos-sdk-python)
- [pymongo](https://api.mongodb.com/python/current/)


### To Run:
1.) Install prerequisites.

2.) Rename `example.env` to `.env`

3.) Add your service credentials to the .env file.

4.) Run `python3 IBM_Cloud_Backups.py`

------

## Important notes:

Please keep in mind that with Data and AI services, training data is not saved.

If you want to run this tool only for a subset of the listed services, simply leave the credentials for all the other services BLANK.

If you get a timeout error for MongoDB, you may need to add your IP address to the Whitelist on the settings tab of the Databses for MongoDB service.

Issues will arise if you don't use pymongo version 3.4.0. To install, `pip install pymongo==3.4.0` or `pip3 install pymongo==3.4.0`

------

### Disclaimer
This code is provided as-is and IBM assumes no responsibility for it.
