# Semantic Search in articles

## Introduction
This task aims to implement a semantic search engine for English articles. Traditional word-matching (lexical search) often misses the context and meaning of words, while semantic search uses embeddings to capture word meaning. The objective is to enable contextual search and extract key information from English articles like the example I worked on [Cyshield's AI & Data Science services](https://cyshield.com/AIDS) article using embeddings.

## Data Description
The dataset is a single article about Cyshield's services, split into meaningful **paragraphs**. The paragraphs are embedded into numerical vectors for semantic search. No specific train-test split was required, as the task focuses on searching within a pre-existing document.

  - Data size: Multiple paragraphs from the article.
  - Features: Text chunk embeddings.

## Experiments
**Goal**: Improve search accuracy by using text embeddings.

**Approach**: The article was split into paragraphs and embedded using Cohere's `embed-multilingual-v3.0` model.
`Annoy` was used to create a fast vector search index for retrieving relevant chunks.

**Results**: Cohere's `command-r-plus` model effectively generated concise, relevant answers from the article in Arabic and English.

**Conclusion**: Integrating deep learning models enhanced the system’s ability to generate precise answers, improving the overall user experience.

## Tools and Resources
Tools Used: 
  - [Cohere](https://docs.cohere.com/) API (text [embeddings](https://dashboard.cohere.com/playground/embed) , answer [generation](https://dashboard.cohere.com/playground/generate))
  - [annoy](https://github.com/spotify/annoy) (vector search)
  - NumPy (embedding handling)
  - Python libraries.

External Resources: Cohere and Annoy documentation.


## Project Reflections
**Challenges**: choosing the best chunking method, embedding model, or text generation model.

**Key Learning**: Gained hands-on experience with semantic search, vector-based indexing, and integrating deep learning models for question-answering tasks.
