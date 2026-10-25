 ## ﻿Legal Document RAG System

An end-to-end Retrieval-Augmented Generation (RAG) pipeline designed to apply semantic search and question-answering over unstructured legal corpora. This system automates information retrieval from massive volumes of complex legal contracts and policies, providing legal professionals with precise, contextualised insights to reduce document review time and enhance research accuracy.

📌 Project Overview

• Domain: Legal Tech / Generative AI
• Objective: Implement document loading, text preprocessing, text chunking, vector embeddings, storage management, and dynamic retrieval combined with Language Generation Models (LLMs).
• Framework: Powered by GenAI abstraction frameworks (LangChain or LlamaIndex).

'' Repository Structure

text
├── RAG_Legal_Docs_[YourName].ipynb   # Core Jupyter Notebook containing the entire implementation
├── requirements.txt                  # Python dependencies
├── README.md                         # Project documentation
└── .gitignore                        # Standard exclusions (ignores local datasets and cache files)
Use code with caution.
(Note: Per security and academic integrity guidelines, the raw datasets (corpus/ and benchmark/) are kept locally and are excluded from version control via .gitignore.)

📊 Dataset Specifications

The pipeline processes a diverse corpus of text files (.txt) divided into four specific subfolders:
• contractnli: Non-disclosure and confidentiality agreements.
• cuad: Contracts annotated with specific legal clauses.
• maud: Merger and acquisition contracts/agreements.
• privacy_qa: Question-answering evaluation pairs covering privacy policies.
Evaluation benchmarks are mapped across matching JSON arrays (contractnli.json, cuad.json, maud.json, privacy_qa.json) specifying text spans and ground-truth answers.

🛠️ System Architecture & Workflow


1. Data Preparation & EDA

• Text Preprocessing: Automated pipeline to ingest .txt sources, strip architectural noise, and clean formatting anomalies.
• Exploratory Data Analysis (EDA): Mathematical evaluation of corpus metrics tracking maximum, minimum, and average document lengths. Includes vocabulary occurrence charts and inter-document structural similarity matrices calculated via TF-IDF vectors.
• Chunking Strategy: Text chunking using token or character split thresholds tailored to extract contextual passages without splitting critical legal clauses.

2. Knowledge Base & Vector Storage

• Embedding Layer: Vector representation generation using advanced semantic embedding models.
• Vector Database: Local database setup with a dedicated persistence storage directory to store chunk embeddings securely.

3. RAG Execution & Evaluation Pipeline

• Contextual Retrieval: Context-matching function that pulls top-k relevant snippets matching legal queries.
• Generation Engine: Generation prompt layer routing structured contexts directly into the LLM to output accurate answers.
• Benchmark Evaluation: Metrics assessment parsing validation elements from the benchmark/ files to evaluate accuracy thresholds for both retrieval and language generation.

🚀 Getting Started


Prerequisites

• Python 3.9+
• Jupyter Notebook or JupyterLab

Installation

1. Clone this repository to your local directory:bash
git clone https://github.com
cd YOUR_REPO_NAME
Use code with caution.
2. Install the necessary dependencies:bash
pip install -r requirements.txt
Use code with caution.
3. Place your assignment data folders (corpus/ and benchmark/) inside your local root workspace directory.
4. Open the starter notebook environment:bash
jupyter notebook RAG_Legal_Docs_[YourName].ipynb
Use code with caution.

⚖️ Academic Disclaimer

This repository is submitted as part of an individual academic assessment. Replicating, copying, or distributing this codebase directly for coursework submissions violates plagiarism guidelines and is strictly prohibited.
