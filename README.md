# ⚖️ AI Meets Law: Legal vs Illegal Activity Detection and Justification

## Overview

This project bridges the gap between artificial intelligence and legal reasoning by using a Retrieval-Augmented Generation (RAG) framework to classify real-world scenarios as legal or illegal under the **Penal Code of 1860 (Bangladesh)**. It not only classifies but also provides **contextual justifications**, making legal knowledge more accessible to both professionals and the public.

## ✨ Key Features

- **Scenario-based Classification**: Determines if an activity is legal or illegal based on user input.
- **Legal Justification Generator**: Outputs explanations grounded in relevant legal sections.
- **RAG Framework**: Combines the **Gemma2B** model for retrieval and **LLaMA 3.2B** for generation.
- **PDF Legal Text Parsing**: Parses and chunks the Penal Code of 1860 using NLP techniques.
- **Vector Store with ChromaDB**: Stores and retrieves semantically relevant legal segments.
- **Multilingual-Ready Pipeline**: Designed for future support of multiple languages.

## 🧠 Models & Technologies

| Component | Description |
|----------|-------------|
| **Gemma2B** | Fine-tuned for retrieving legal text chunks from the Penal Code. |
| **LLaMA 3.2B** | Generates coherent, context-aware legal justifications. |
| **SentenceTransformers** | Embeddings via `all-mpnet-base-v2` for semantic similarity. |
| **ChromaDB** | Vector store for fast top-k retrieval. |
| **LangChain** | Framework to connect components of the RAG pipeline. |
| **PyMuPDF, PyPDF2** | Legal text extraction from PDFs. |
| **spaCy** | Tokenization, sentence segmentation. |

## 🛠️ System Architecture

+--------------------+ +------------------------+
| User Legal Query | ----> | Embed & Retrieve Top |
| | | Chunks from ChromaDB |
+--------------------+ +------------------------+
|
v
+---------------------+
| LLaMA 3.2B Model |
| Generates Answer |
+---------------------+
|
v
+----------------------------+
| Legal Status & Justification|
+----------------------------+

## 📊 Sample Queries & Output

**Query:** *Is carrying a firearm for self-defense legal?*  
**Output:** *Section 99 of the Penal Code permits private defense but not to the extent of causing death unless specific threats are present...*

**Query:** *Can a police officer arrest without a warrant based on suspicion alone?*  
**Output:** *Illegal under Section 43 unless the officer has valid cause...*

## 🧪 Evaluation

- Tested with real-world scenarios such as **self-defense**, **intoxication**, and **wrongful arrest**.
- Top-k retrieval precision remained strong across varying complexity.
- Legal accuracy benchmarked using official Penal Code references.

## 🔍 Use Cases

- **Lawyers & Legal Interns**: Quick access to relevant penal code provisions.
- **Students**: Learn legal reasoning through AI-generated explanations.
- **Public Users**: Understand rights and legal status in common situations.

