# **DocuInsight: AI-Powered Document Interaction and Querying**

**DocuInsight** is an advanced AI-powered chatbot designed to help you interact with your documents. By leveraging **Retrieval-Augmented Generation (RAG)** techniques powered by the **Llama 3** model, DocuInsight allows you to upload PDF documents, parse their contents, and ask contextually relevant questions to extract insights. Whether you're working with business reports, research papers, or any other type of document, DocuInsight turns it into an interactive knowledge hub.

The chatbot uses sophisticated document embeddings for efficient retrieval, providing precise answers and offering an intuitive conversational experience.

## **Features**

![Architecture](/images/chatbot_screenshot1.JPG)

- **PDF Upload and Parsing**: Upload PDF documents, which are then parsed and transformed into a structured, searchable format.
- **Document Embedding**: Documents are broken into embeddings that allow for efficient search and retrieval of specific information.
- **Conversational Querying**: Ask the chatbot questions about the document, and get context-aware, relevant answers.
- **Memory Management**: Retains conversation history for more natural and coherent interactions.
- **Intuitive Interface**: A clean, user-friendly interface for easy interaction and document querying.

## **How It Works**

1. **Upload Your PDF**: Upload your document, and DocuInsight will parse it into a structured format that’s ready for querying.
2. **Ask Your Questions**: Interact with the chatbot by asking questions about the document's content. DocuInsight uses AI to understand the document and provide accurate responses.
3. **Explore the Content**: Continue your conversation, with DocuInsight keeping track of context and answering follow-up questions based on your previous queries.

## **Architecture Overview**

![Architecture](/images/Architecture_design.JPG)

DocuInsight utilizes the following key components:

- **Llama 3**: A powerful language model for deep understanding of the document's content.
- **Chainlit**: A framework to facilitate the chatbot's conversational capabilities.
- **LangChain**: A toolkit to manage document processing and language model interactions.
- **Qdrant**: A high-performance vector database to store and efficiently retrieve document embeddings.
- **LlamaParse**: A parsing tool that converts complex PDF files, including those with tables, into structured, query-friendly formats.


# Chat with your documents

![Architecture](/images/chatbot_screenshot2.JPG)

Chat anything about the documents that you provided. This is using open source LLM models by Meta: Llama 3

## Install dependencies

Install the required dependencies in the requirements.txt

## Get Groq API Key

Get your groq API Key. [Obtain API KEY here](https://console.groq.com/keys)

Set environment variable GROQ_API_KEY:

```
export GROQ_API_KEY="your_api_key"
```


## Upload files to the data directory

Go to the /data directory and upload your documents.

run the populate_database script:

```
python populate_database.py
```

## Run the streamlit app

```
streamlit run queryprompt.py
```
