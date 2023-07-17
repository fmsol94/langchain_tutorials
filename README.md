# Langchain Tutorials

## Chat with your data

Based on [Langchain - Chat with your data](https://learn.deeplearning.ai/langchain-chat-with-your-data) course. 

## Table of Contents

1. [Document Loading](#document-loading)
2. [Document Splitting](#document-splitting)
3. [Vectorstores and Embeddings](#vectorstores-and-embeddings)
4. [Retrieval](#retrieval)
5. [Question Answering](#question-answering)
6. [Chat](#chat)


## Document Loading

This section introduces methods to load documents from different sources, including PDFs, YouTube, URLs, and Notion.

### PDFs
The `PyPDFLoader` from Langchain is used to load PDFs, specifically [transcripts](https://see.stanford.edu/materials/aimlcs229/transcripts/MachineLearning-Lecture01.pdf) from Andrew Ng's CS229 course.

### YouTube
The process of loading and processing data from YouTube using the `YoutubeAudioLoader` is covered.

### URLs
This part discusses the `WebBaseLoader`, which is utilized to load and process documents from URLs.

### Notion
The `NotionDirectoryLoader` is used to load content from Notion. The process of duplicating a Notion page, exporting it as `Markdown / CSV`, unzipping it, and saving it as a folder containing the markdown file for the Notion page is detailed.

## Document Splitting

This section focuses on how to split documents into smaller chunks for processing. Techniques include splitting by character count, token count, and context.

### Recursive and Character Splitting
The usage of the `RecursiveCharacterTextSplitter` and `CharacterTextSplitter` to split a document into chunks of a specific character size, with or without overlap, is explained.

### Token Splitting
This part describes the use of the `TokenTextSplitter` to split a document into tokens. This technique is useful for language models with context windows designated in tokens.

### Context Aware Splitting
Context aware splitting is introduced using the `MarkdownHeaderTextSplitter`, which preserves header metadata in chunks. This technique is particularly beneficial for structured documents like Markdown files.

## Vectorstores and Embeddings

This section explains how to store and retrieve vectors for text retrieval. It covers how to use OpenAIEmbeddings to generate embeddings for sentences and discusses the concepts of similarity search and maximum marginal relevance. The use of Vectorstores like Chroma is demonstrated for efficient storage and retrieval of vectors. The section also identifies potential challenges in retrieval and presents solutions to ensure diversity and specificity in the retrieved results.

## Retrieval

The retrieval section delves into the use of different types of retrievers for document retrieval. Apart from vectorstore retrieval, other methods like SVM and TF-IDF retrievers are also introduced. The section presents ways to enhance retrieval results, including the use of metadata for context-specific retrieval and contextual compression for more concise responses.

## Question Answering

This section shows how to build a question answering system and the different ways of condensating the information to fit the LLM limit number of tokens input.

## Chat

This section implements a full chat with memory of previous messages. The script `chat.py` implements a GUI to run the full chatbot with all the concepts explained in the previous sections. To run the GUI, we can just execute `python chat.py`, and this will launch the panel application in port `8080`.