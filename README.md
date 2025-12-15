#Assignment 5 – Simple Retrieval-Augmented Generation (RAG)

#Written by Edgar 
#Embedding Model: sentence-transformers/all-MiniLM-L6-v2  
#LLM: google/flan-t5-small  

#Overview
This project implements a simple Retrieval-Augmented Generation (RAG) pipeline
to answer questions using a custom knowledge base describing AcmeTech company policies.

#Retrieval Summary

| Test Case | Retrieved Chunks | Outcome |
|---------|------------------|--------|
| Factual | Remote Work Policy | Correct, grounded answer |
| Foil | Irrelevant policy chunks | Model correctly stated lack of information |
| Synthesis | Remote Work + Security | Combined multiple policies accurately |

#Analysis
Compared to a raw LLM, the RAG system significantly reduced hallucination by grounding
responses in retrieved context. When information was missing from the knowledge base,
the model appropriately declined to answer rather than guessing.