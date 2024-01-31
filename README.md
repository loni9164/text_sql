# Translate text into SQL queries, querying the database with the generated queries and converting the SQL output into a human-interpretable answer
This section details the implementation of different LLM to translate text into SQL queries. It includes querying the database with these generated queries and converting the SQL output into a human-interpretable answer.


## Repository Contents

### CSV Files
- Directory `csv_files/` contains CSV files used to create the database for the credit card system.

### Notebooks

#### sqlcoder2.ipynb
- **Model:** sqlcoder2-GPTQ (15B parameters)
- **Database:** PostgreSQL
- **Features:**
  - Generates SQL queries, query the database and final answer generation.
  - Includes a simple Gradio UI, enabling users to ask questions about their credit cards/accounts.
- **TODO:**
  - Develop metrics to evaluate model accuracy for both query and final answer generation.
  - Experiment with separate models for query and final answer generation.

#### code_llama.ipynb
- **Model:** CodeLlama (7B parameters)
- **Observation:** Performance currently lower than sqlcoder2-15B.
- **TODO:**
  - Redo experiments with an updated database and recent few-shot learning examples.
  - Compare performance with sqlcoder2-15B.
  - Experiment with the CodeLlama 15B model and compare its performance against sqlcoder2-15B.

#### sqlcoder_34b.ipynb
- **Attempt:** Tried loading sqlcoder 34B parameter model.
- **Issue:** Inability to load the model in the free tier of Google Colab.
