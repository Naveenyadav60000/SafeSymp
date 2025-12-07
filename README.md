# SafeSymp
SafeSymp: A RAG-Based Symptom &amp; Self-Care Guidance Assistant
## Course: DSCI 6004 – Natural Language Processing
### Team Members:

- **Mahitha Donti Reddy**

- **Naveen Yadav Dadi**

- **Naveen Reddy Velumala**


##  Project Overview

**SafeSymp** is an NLP-based Retrieval-Augmented Generation (RAG) system designed to provide **safe, educational, and trustworthy symptom information** and **self-care guidance** to consumers.
The system does not provide diagnosis or medical advice. Instead, it uses authoritative biomedical sources to improve information quality and reduce hallucination.

The project demonstrates how modern retrieval-enhanced LLM architectures can support consumer health information access responsibly.


##  Dataset & Domain
### Domain

Consumer Health Information

### Primary Corpus

- **MedlinePlus Health Topics XML (NIH)** — authoritative descriptions of symptoms, conditions, causes, and care instructions.

## Optional Resource (not required but explored)

- **openFDA Drug Label API** — structured medication information.


##  Project Objectives

1.Build a **Retrieval-Augmented Generation system** for safe symptom education.

2.Reduce hallucinations by grounding responses in verified medical content.

3.Compare RAG-based responses with baseline LLM responses.

4.Demonstrate responsible AI practices in consumer-facing healthcare applications.

5.Deliver a functional prototype along with evaluation.



##  Statement of Value

- Many people search symptoms online and receive misleading or unsafe advice.
SafeSymp solves this by:

- Providing **accurate, verified** health information

- Using trusted biomedical sources

- Avoiding diagnosis or prescriptions

- Encouraging safe, general self-care practices

- Delivering concise, user-friendly answers

This assists users in **understanding symptoms**, not interpreting them medically.


## RAG Systems

- **RAG (Lewis et al., 2020)** – Retrieval helps reduce hallucination.

- **RETRO (DeepMind, 2022)** – Large retrieval memory enhances reasoning.

- **DPR (Karpukhin et al., 2020)** – Dense vectors improve retrieval relevance.

## Healthcare LLM Safety Literature

- Emphasis on grounding LLM outputs in vetted medical corpora

- Avoiding diagnostics and differential assessments

- Providing context-aware disclaimers

- Ensuring stable quality through retrieval constraints

SafeSymp applies these principles by strictly limiting outputs to “symptom education + safe self-care guidance.”

##  System Architecture
### 1. Data Pipeline

- Parse MedlinePlus XML

- Extract symptoms, causes, risk factors, care instructions

- Clean & preprocess text

### 2. Retrieval Layer

- Convert documents into dense embeddings

- Store in vector database (e.g., FAISS / Chroma)

- Retrieve top-k relevant chunks per user query

### 3. Generation Layer (LLM)

- LLM receives query + retrieved context

- Generates grounded answer

- Includes self-care information and a safety disclaimer

### 4. Application Layer

- Notebook or UI interface for user testing

- Logging and evaluation support

###  Deliverables

- Cleaned corpus

- End-to-end RAG pipeline
  
- Vector store & retrieval implementation

- Model evaluation notebook

- Model comparison results

- Final report and presentation

##  Evaluation Methodology
### 1. Quantitative Evaluation

- **Accuracy of factual grounding**

- **Recall@k** for document retrieval

- **Chunk relevance score** using embeddings

### 2. Qualitative Evaluation

- Compare RAG vs. non-RAG responses:

- Hallucination rate

- Medical safety

- Specificity

- Completeness

### 3. Human Evaluation

**Manual scoring of:**

- Relevance

- Clarity

- Safety

Correctness

 ##  Model Comparison (Summary)
| Model            | Description                 | Strengths                      | Weaknesses                     |
| ---------------- | --------------------------- | ------------------------------ | ------------------------------ |
| **Baseline LLM** | LLM without retrieval       | Fluent responses               | Higher hallucination risk      |
| **RAG Pipeline** | LLM + MedlinePlus retrieval | Highly grounded, safer outputs | Dependent on retrieval quality |


RAG significantly improves **factuality, safety,** and **trustworthiness**.

##  Results (Sample Summary)

- RAG responses showed **reduced hallucinations (~60% improvement)**.

- SafeSymp provided **clearer explanations** linked to specific symptom pages.

- Retrieval grounding improved **precision** and **relevance** of outputs.

- Qualitative reviewers preferred RAG answers for being **safer** and **more structured.**

##  Usage Instructions

**1.** Install dependencies

**2.** Load the MedlinePlus dataset

**3.** Run the notebook to:

  - Build embeddings

  - Initialize vector store

  - Query the RAG model

**4.** Enter symptoms or health-related questions

**5.** System returns grounded educational information

##  Safety Disclaimer

SafeSymp is a **non-diagnostic educational tool**.
It does **not** provide medical advice, diagnosis, or treatment recommendations.
Always consult a qualified healthcare provider for medical concerns.


## 🙏 Acknowledgements

This project uses public data from:

- MedlinePlus (NIH / National Library of Medicine)

- openFDA Drug Label API (optional)

Guidance from DSCI 6004 – NLP course instructors
