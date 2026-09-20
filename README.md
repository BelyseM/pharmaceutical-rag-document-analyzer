# Pharmaceutical Document RAG System

An AI-powered Retrieval-Augmented Generation (RAG) system for
intelligent analysis and data retrieval over pharmaceutical
documents.

## Overview

This project develops an end-to-end pipeline that transforms complex
pharmaceutical PDF documents into a searchable knowledge base and
generates source-attributed answers to natural-language questions.

The system combines document classification, OCR, semantic chunking,
vector retrieval, query routing, and large language models to improve
information retrieval across heterogeneous pharmaceutical documents.

## Pipeline

PDF Documents
↓
Text Extraction / OCR
↓
Document Classification
↓
Logical Document Segmentation
↓
Metadata-Aware Chunking
↓
Sentence Transformer Embeddings
↓
FAISS Vector Index
↓
LLM Query Routing
↓
Context Retrieval
↓
Mistral 7B Answer Generation
↓
Source Attribution + Confidence

## Key Features

- PDF text extraction with PyMuPDF
- OCR fallback for scanned documents
- LLM-based document classification
- Logical document boundary detection
- Metadata-preserving document chunking
- Semantic embeddings with Sentence Transformers
- FAISS vector similarity search
- Automatic query routing by document type
- Source-attributed answer generation
- Confidence scoring
- Gradio interactive interface
- Retrieval and end-to-end evaluation

## Evaluation

The project includes evaluation methods for:

- Recall@K
- Mean Reciprocal Rank (MRR)
- Precision@K
- Hit Rate
- Answer Accuracy
- Citation Accuracy
- Response Time

## Technologies

Python · PyMuPDF · Tesseract OCR ·
Sentence Transformers · FAISS · LlamaIndex ·
Mistral 7B · Gradio · NumPy

## Project Context

Developed as part of an AI-powered document extraction externship.

> Note: This public repository contains only code and
> non-confidential/sanitized materials. Proprietary documents and
> confidential company information are not included.
