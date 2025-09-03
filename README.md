# AI-Based-Medical-Chatbot
This project is an AI-powered **medical chatbot** built with **Retrieval-Augmented Generation (RAG)**.
It allows users to upload medical PDFs (e.g., medical reports), and then ask questions. The chatbot answers **only** from the uploaded content, ensuring **evidence-based, context-grounded** responses with **citations**.

⚠️ **Disclaimer**: This tool is for **educational purposes only**. It is **not** a substitute for professional medical advice. Always consult a healthcare professional for medical concerns.

## Features
*  **PDF Upload & Analysis** – Extracts text using PyPDF2 or OCR (Tesseract) for scanned PDFs.
*  **Hybrid Search (Dense + Sparse)** – Combines **HuggingFace embeddings** with **BM25** for precise retrieval.
*  **Chat Interface** – Built with **Streamlit**, featuring a clean, modern UI.
*  **Context-Aware Answers** – Answers are generated **strictly** from uploaded documents.
*  **Metrics Dashboard** – Real-time monitoring of RAG quality:

  * Faithfulness
  * Answer relevancy
  * Context relevancy
  * Response latency
  * User feedback
* **Safe Medical Guidance** – Provides structured answers with:

  * Summary / Overview
  * Usage & Indications
  * Dosage & Administration
  * Safety Precautions
  * Next Steps & Disclaimer
*  **Data Export** – Save evaluation logs as CSV.

##  Tech Stack

* **Frontend / App**: [Streamlit](https://streamlit.io/)
* **Retrieval**: [Pinecone](https://www.pinecone.io/) + Hybrid (BM25 + HuggingFace Embeddings)
* **Embeddings**: `all-MiniLM-L6-v2` (HuggingFace)
* **LLM Backend**: [Groq API](https://groq.com/) (OpenAI-compatible client)
* **PDF Processing**: PyPDF2, pdf2image, pytesseract (OCR)
* **Evaluation**: LLM-as-a-Judge for real-time scoring
* **Data Handling**: Pandas

## Evaluation Metrics

The **Metrics Dashboard** provides insights into:

* **Faithfulness**: Is the answer supported by retrieved context?
* **Answer Relevancy**: Does the answer fully address the user’s query?
* **Context Relevancy**: Were the retrieved documents relevant?
* **Latency**: Response time per query.
* **User Feedback**: 👍 / 👎 tracking.

## Limitations

* Depends on quality of uploaded PDFs.
* Does not provide **real-time clinical advice**.
* OCR accuracy may vary on poor scans.
* Requires valid Pinecone & Groq API keys.

## Future Improvements

* Support for multiple LLM backends (OpenAI, Anthropic, etc.)
* Multi-language medical document support.
* Fine-tuned evaluation metrics dashboard.
* Integration with external structured medical databases (e.g., PubMed APIs).

