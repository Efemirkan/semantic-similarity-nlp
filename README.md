# Semantic Similarity with NLP

## Overview

How similar are two sentences in meaning?

This project compares three NLP approaches to answer that question, moving from simple word counting to transformer-based models:

- **TF-IDF** — sparse, count-based 
- **GloVe** — pre-trained static word embeddings
- **BERT** — contextual embeddings via HuggingFace Transformers

## Motivation

When I search for something online or ask a chatbot a question, how does it actually understand what I mean, not just the exact words I typed?

That question is what this project is about.

Semantic similarity powers a lot of tools we use every day, such as search engines, chatbots, recommendation systems. But a simple
keyword match breaks the moment someone uses a synonym or rephrases a question.

In this project, I will implement all three approaches myself to see that performance gap in practice, not just read about it.

## Plan

1. TF-IDF + Cosine Similarity
    - Convert sentences into TF-IDF vectors and compute similarity scores
2. GloVe Embeddings
    - Represent sentences by averaging pre-trained word embeddings
3. BERT Embeddings
    - Extract contextual sentence embeddings using a pre-trained BERT model

The performance of each method will be compared on sentence pairs and evaluated on a benchmark dataset.

## Tech Stack
- Python 3.x
- scikit-learn
- GloVe pre-trained vectors
- HuggingFace Transformers

## Dataset

Planned: Semantic Textual Similarity Benchmark (STS-B)

## Hypothesis

Before running any experiments, I expect the different approaches to perform at different levels.

1. TF-IDF will likely perform the worst because it relies on exact word overlap and cannot handle paraphrases well.

2. GloVe embeddings should perform better, as they capture semantic similarity between words. However, they still ignore context, so their performance will be limited.

3. BERT is expected to perform the best, since it represents words based on their context within the sentence and can better capture overall meaning.