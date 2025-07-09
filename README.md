# NEG

Collaborative research space for LLM usage in ESG negative news graph

## Content of the repository

### Notebook

The notebook used for the research paper experimentations / results is `notebook/negraph.ipynb`.

### Data

- The `webz.io` github page should be cloned in the `notebook/data` folder
- The patterns generated through the experimentations are located in the `notebook/patterns/extraction_patterns.txt` file
- The UNGC Principles are all defined in the folder `notebook/ungc_principles` folder, their filename is in the format `principle-X.txt` where `X` corresponds to the UNGC Principle number from 1 to 10. They can be manually extracted from this website by clicking on the respective _Principle X_ hyperlink https://unglobalcompact.org/what-is-gc/mission/principles
- The UNGC Principle summaries generated are also located in the folder `notebook/ungc_principles` folder, their filename is in the format `principle-X-summary.txt` where `X`corresponds to the UNGC Principle number from 1 to 10.

## Local execution

### Setting up a virtual environment

Make sure you have Python installed then execute this command in the terminal / command line

```
python3 -m venv .venv
```

To activate the virtual environment

```
source .venv/bin/activate
```

### Install dependencies

Run the command the following command to install the required dependencies

```
pip install .
```

### Define environment variables

To run the notebook you would need some environment variables, specifically these ones :

```
AZURE_ENDPOINT=
AZURE_API_KEY=
AZURE_API_VERSION=
```

To define them, I would suggest creating a `.env` file at the base of this repository, set up those environment variables in it and then to run this command to export them :

`export $(grep -v '^#' .env | xargs)`

### Use Neo4j

Install `docker` locally

Run the following command to start a local instance of Neo4j

```
bash start_up_neo4j.sh
```

To access Neo4j's UI, in your browser go to http://localhost:7474 and login with :

- Username : neo4j
- Password : password

To stop Neo4j, run :

```
docker stop neo4j-container
```

```
docker rm neo4j-container
```
