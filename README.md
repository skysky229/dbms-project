# DBMS Project
- Each service is in a single folder. Inside each folder, there are detail instructions of how to start and use each services. 
- There are two main services: Spark, which is in charge of processing, and Minio, which is in charge of storing data and the lakehouse. 

## How to use scripts?
- Currently, there are five notebooks:
	- demo: just a demo notebook to test functionality
	- import_csv_to_lakehouse: import a csv file to a table in lakehouse. 
	- ML: read the CV and assign a category to it
	- parse_text_cv: parse the CVs as text and get the necessary information
	- insert_to_postgres: insert a lakehouse table to warehouse
- To run a script:
	- Create two buckets raw-bucket and cleaned-bucket
	- Upload two folders text_cv and image_cv to raw-bucket
	- Start Spark services
	- Access the Spark Notebook UI at localhost:8888. Read README.md in Spark folder for more information.
	- Run the scripts
- NOTE: Due to shortage of resources, it is not possible to run two notebooks at the same time. In order to run another notebook, we have to SHUT DOWN the existing ones. There are two options:
	- Use icon stop kernel in the UI (may not work in some cases)
	- Access Spark Master UI at localhost:8080 -> See Running Applications -> Kill the one that need to be stopped


