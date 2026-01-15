### 1. The Core Biological Problem: AMR

You don't need to be a biologist, but you must understand *what* we are trying to solve.

* **Antimicrobial Resistance (AMR):** Learn why bacteria stop responding to medicines and why identifying the specific genes responsible is so critical for public health.


* **The "False Positive" Problem:** Understand that current tools often give false alarms (false positives) when a sequence is "borderline" or ambiguous. Our entire project exists to fix this specific issue using AI reasoning.



### 2. Bioinformatics Tools & Data Formats

Our system acts as a wrapper around existing industry standards, so you need to know how they work.

* **Sequence Alignment (BLAST & DIAMOND):** We use these tools to find the initial list of candidate genes. You should learn how to run them from the command line and how to interpret their output scores (like "Bit Score" and "E-Value").


* **FASTA Files:** This is the input data format. You need to know how to parse these text files to extract DNA sequences.



### 3. The Dataset: CARD (Comprehensive Antibiotic Resistance Database)

This is the single most important data source for our project.

* **The Ontology (ARO):** CARD organizes data using the "Antibiotic Resistance Ontology" (ARO). You need to learn how to query this database to find the relationship between a gene and the drug it resists.


* **Why we need it:** We use this data to feed "context" into the AI. If you don't understand how CARD works, you can't build the RAG system.



### 4. The AI Architecture: LLMs & RAG

This is the "brain" of our framework.

* **Retrieval-Augmented Generation (RAG):** This is the specific technique we use. You must learn how to combine external data (from CARD) with a prompt to stop the AI from hallucinating (making things up).


* **Prompt Engineering:** We have to write very specific instructions (prompts) to get the LLM to act as a validator. You need to know how to structure a prompt that includes biological statistics and asks for a "True/False" verdict.



### 5. The Tech Stack

* **Python:** The backend logic, including running the alignment tools and connecting to APIs, is built in Python.


* **JSON Handling:** Our system outputs data in JSON for developers. You need to be comfortable parsing complex JSON structures from the CARD database and the LLM API responses.


* **API Integration:** You need to know how to send requests to LLM providers (like OpenAI) and handle the responses.



### Summary Checklist for Day 1

If I were you, I would start in this order:

1. **Read Chapter 1 & 2** of the thesis to understand the "Gap Analysis" (why current tools fail).


2. **Download CARD:** Get the `card.json` file and try to find a specific gene description inside it.
3. **Run DIAMOND:** Try to align a sample FASTA file against a database locally.


4. **Experiment with RAG:** Write a simple Python script that sends a biological description to ChatGPT and asks it to summarize it.