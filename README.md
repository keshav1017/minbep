# Tokenization Notebook: Byte Pair Encoding (BPE) for LLMs

## Overview

This repository contains a Jupyter Notebook that replicates the tokenizer-building process demonstrated by Andrej Karpathy in his video ["Let's build the GPT Tokenizer"](https://www.youtube.com/watch?v=zduSFxRajkE). The notebook is intended for **educational purposes only** and walks through the fundamentals of tokenization in Large Language Models (LLMs), specifically focusing on Byte Pair Encoding (BPE).

## Purpose

- **Learning**: This notebook is a step-by-step, hands-on guide to understanding how tokenizers work in modern LLMs, such as GPT-2 and GPT-4.
- **Replication**: The code and explanations closely follow Karpathy's tutorial, providing practical exercises and detailed commentary.
- **Experimentation**: Users can modify the notebook to experiment with different datasets, vocabulary sizes, and tokenization strategies.

## Contents

### 1. Introduction to Tokenization

- Explains the importance of tokenization in LLMs.
- Discusses why tokenization is a separate preprocessing stage from the neural network itself.
- Outlines typical issues caused by tokenization, such as inefficiencies with non-English text and code formatting.

### 2. Unicode and Text Encoding

- Describes how text is represented in computers using Unicode code points.
- Compares UTF-8, UTF-16, and UTF-32 encodings, highlighting why UTF-8 is preferred for tokenizer input.

### 3. Byte Pair Encoding (BPE) Algorithm

- Provides a clear walkthrough of the BPE algorithm:
  - Starts with a sequence of bytes (from UTF-8 encoding).
  - Iteratively merges the most frequent pairs of bytes/tokens.
  - Builds up a vocabulary of merged tokens to achieve better compression and efficiency.
- Includes code cells for:
  - Counting consecutive pairs.
  - Merging the most frequent pair.
  - Iteratively building the vocabulary.

### 4. Training the Tokenizer

- Demonstrates how to train a tokenizer on a sample text dataset.
- Shows how vocabulary size is a tunable hyperparameter.
- Tracks compression ratio and vocabulary growth as merges are performed.

### 5. Encoding and Decoding

- Implements functions to:
  - Encode raw text into token sequences using the trained vocabulary.
  - Decode token sequences back into human-readable text.
- Explains the mapping between tokens and their corresponding byte sequences.

### 6. Practical Examples and Quirks

- Explores real-world quirks of tokenization, such as:
  - How different tokenizers split words, numbers, and whitespace.
  - The impact of tokenization on code and non-English text[1].
  - Case sensitivity and special cases in token splitting.

### 7. References and Further Reading

- The notebook references Karpathy's video and associated resources, including:
  - The [minBPE GitHub repository](https://github.com/karpathy/minbpe)
  - The [tiktoken](https://github.com/openai/tiktoken) and [sentencepiece](https://github.com/google/sentencepiece) libraries.

## Attribution

> **This notebook is a direct replication of Andrej Karpathy's video ["Let's build the GPT Tokenizer"](https://www.youtube.com/watch?v=zduSFxRajkE). It is provided strictly for learning and educational purposes. All credit for the instructional content and original ideas goes to Andrej Karpathy.**

## Disclaimer

- **Do not use this code or notebook for production or commercial purposes.**
- The implementation is simplified for educational clarity and may not reflect all optimizations or edge cases found in production tokenizers.

## Getting Started

1. **Clone or download** this repository.
2. **Open** the `tokenization.ipynb` notebook in Jupyter or Google Colab.
3. **Follow the cells** sequentially, reading the explanations and running the code.
4. **Experiment** with your own text samples and vocabulary sizes to deepen your understanding.
