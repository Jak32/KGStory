# KGStory

This project processes benchmark datasets and interacts with the OpenAI API and GEMINI API to generate coherent text based on RDF triples. The project is divided into two main parts: processing LMDB and DBpedia datasets. 

## Table of Contents

- Installation
- Usage
- [Environment Variables](#environment-variables)
- Notebooks
  - CHATGPT_LMDB.ipynb
  - CHATGPT_DBPEDIA.ipynb
- License

## Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/Jak32/KGStory.git
   cd KGStory
   ```

2. Create a virtual environment and activate it:
   ```sh
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install the required packages:
   ```sh
   pip install -r requirements.txt
   ```

## Usage

1. Ensure you have the necessary environment variables set up in a [`.env`](command: ".env.example") file (see [Environment Variables](#environment-variables)).

2. Run the Jupyter notebooks to process the datasets and interact with the OpenAI API.

## Environment Variables

Create a [`.env`](command: ".env.example") file in the root directory of your project and add the following variables:

```plaintext
CHATGPT_API_KEY="your-chatg-api-key"
GEMINI_API_KEY="your-gemini-api-key"
```

## Notebooks

### CHATGPT_LMDB.ipynb

This notebook processes LMDB benchmark datasets and interacts with the OpenAI API to generate coherent text based on RDF triples.

#### Key Steps:
1. Load environment variables.
2. Process `.txt` files in the [`data/lmdb`](command: "/data/lmdb") directory. (A .txt file contains a number = Folder ID and a URL)
3. Read the txt file and parse it.
4. Make requests to the OpenAI API or Gemini and store the responses.
5. Save the results to JSON files at data/lmdb/ESBM*/ESBM*_output*.json

### CHATGPT_DBPEDIA.ipynb

This notebook processes DBpedia benchmark datasets and interacts with the OpenAI API to generate coherent text based on RDF triples.

#### Key Steps:
1. Load environment variables.
2. Process `.txt` files in the [`data/lmdb`](command: "/data/lmdb") directory. (A .txt file contains a number = Folder ID and a URL)
3. Read the txt file and parse it.
4. Make requests to the OpenAI API or Gemini and store the responses.
5. Save the results to JSON files at data/dbpedia/ESBM*/ESBM*_output*.json

