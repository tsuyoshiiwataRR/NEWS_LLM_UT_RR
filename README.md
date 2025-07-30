# Aligning ESG Controversy Data with International Guidelines through Semi-Automatic Ontology Construction

## Content of the repository

### Notebook

The notebook used for the research paper experimentations / results is `research_notebook.ipynb`.

### Data

- The `webz.io` github page (https://github.com/Webhose/free-news-datasets) should be cloned in the `notebook/data` folder
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
