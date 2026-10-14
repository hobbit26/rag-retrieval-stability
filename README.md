# rag-retrieval-stability
Experiments for evaluating query-paraphrase retrieval stability as a lightweight signal for adversarial context detection in RAG.

# Query-Paraphrase Retrieval Stability for Adversarial Context Detection in RAG

This repository contains the experimental implementation for our COMPSCI 764 research project at the University of Auckland.

## Project

Our project investigates whether retrieval instability under semantically equivalent query paraphrases can serve as a lightweight signal for detecting adversarially retrieved contexts in Retrieval-Augmented Generation (RAG) systems.

The experiments compare:

- Vanilla RAG
- Keyword filtering
- Semantic instruction-likeness detection
- Retrieval-stability-based detection
- A stability-aware semantic detector

## Experimental Setup

The experiments use:

- HotpotQA
- `sentence-transformers/all-MiniLM-L6-v2` for retrieval
- `google/flan-t5-base` for generation
- Query paraphrases for retrieval stability analysis

The notebook contains the complete experimental pipeline and stored outputs reported in the final paper.

## Main Finding

In our experiments, query-paraphrase retrieval instability did not provide reliable additional detection value beyond semantic instruction-likeness.

The stability-only detector achieved a held-out ROC-AUC of 0.4567, while the semantic-only detector achieved 0.6978. Adding retrieval instability to the semantic detector did not improve overall performance and introduced substantial additional latency.

## Files

- `RAG_Retrieval_Stability_Experiments.ipynb` — complete experimental notebook with stored outputs.

## Authors

Lisha Zou  
Reena Liu

School of Computer Science  
The University of Auckland
