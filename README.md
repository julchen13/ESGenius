# ESGenius
Prototype for LLM document Chat his tool is an LLM-based assistant for answering questions from PDF documents. The assistant allows users to upload PDF documents, process them, and then ask questions that are answered based on the content of those documents. Main Features PDF Processing

Upload one or multiple PDF documents Splitting documents into smaller chunks for more efficient processing Configurable document splitting parameters:

Split method (word, sentence, passage) Split length (100-1000) Split overlap (0-500)

Template Management

Customizable prompt templates for LLM queries Template validation with protection for important placeholders Reset function to restore the original template

Questions and Answers

Selection of various LLM models:

Anthropic Claude models (3 Opus, 3 Sonnet, 3 Haiku, 3.7 Sonnet) OpenAI GPT models (3.5 Turbo, 4, 4 Turbo Preview) HuggingFace models (Zephyr, Meta-Llama 3.1)

Predefined questions or manual input Multilingual support (automatically detects the language of the question)

PDF Report Generation

Creation of PDF reports containing all questions and answers Customizable output directories Integration of company branding (FMA logo)

Technical Details Frameworks and Libraries Used

Haystack: Framework for document retrieval and question answering Gradio: For the user interface SentenceTransformers: For embedding generation ReportLab: For PDF generation LangDetect: For language detection

API Integration

Support for various LLM APIs:

Anthropic (Claude models) OpenAI (GPT models) HuggingFace Inference API

Embedding and Retrieval

Batch processing for efficient handling of large documents Vector-based retrieval of relevant document sections Optimized memory usage through chunking and batching

Example Template The default template is focused on insurance SFCRs (Solvency and Financial Condition Reports) and instructs the LLM to take on the role of an analyst from a regulatory authority. However, it can be customized for other use cases. Usage

Upload PDF documents Set processing parameters and click "Process PDFs" Optional: Customize the template Select an LLM model Ask a question (predefined or manual) Generate a PDF report, if desired

Requirements

Python environment with installed dependencies API keys for the LLM providers used (in separate text files):

/content/anthropic_api_key.txt /content/openai_api_key.txt /content/huggingface_api_key.txt

Access to an FMA logo for PDF reports (optional)
