# Architecture

The RAG system follows this sequence:

1. **PDF ingestion** — accepts a pharmaceutical PDF package.
2. **Text extraction** — uses PyMuPDF for normal PDFs.
3. **OCR fallback** — uses Tesseract when a page has no extractable text.
4. **Document analysis** — classifies pages and detects logical document boundaries.
5. **Chunking** — creates overlapping chunks while preserving document/page metadata.
6. **Embedding** — encodes chunks with `all-MiniLM-L6-v2`.
7. **Indexing** — stores dense vectors in FAISS.
8. **Query routing** — uses the LLM to predict the most relevant document type.
9. **Retrieval** — searches the appropriate vector index and returns relevant chunks.
10. **Generation** — passes retrieved context to Mistral 7B Instruct.
11. **Attribution** — returns answer text together with source information and a retrieval-based confidence estimate.

The public repository intentionally excludes company-specific documents and evaluation ground truth.
