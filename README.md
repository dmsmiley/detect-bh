# Intertextual Parallel Detection in Biblical Hebrew: A Transformer-Based Benchmark

A benchmark study evaluating transformer-based language models for detecting parallel passages in the Hebrew Bible, focusing on textual relationships between Chronicles and Samuel/Kings.

## Overview

This repository contains code and data for evaluating pre-trained transformer models (E5, AlephBERT, MPNet, and LaBSE) on the task of identifying intertextual parallels in Biblical Hebrew texts. The study addresses limitations of traditional manual comparison methods by leveraging modern NLP techniques to detect semantic similarities between ancient texts.

## Key Features

- **Embeddings-based approach**: Uses verse-level embeddings to capture semantic relationships beyond surface-level matching
- **Multiple model evaluation**: Compares performance across 4 state-of-the-art transformer models
- **Comprehensive metrics**: Employs cosine similarity, Wasserstein Distance, and classification metrics
- **Known parallels dataset**: 558 verified parallel verses between Chronicles and Samuel/Kings

## Results Summary

| Model | Mean Cosine (Parallel) | Mean Cosine (Non-Parallel) | F1-Score | Wasserstein Distance |
|-------|------------------------|----------------------------|----------|---------------------|
| **E5** | 0.966 | 0.882 | 0.88 | 0.081 |
| **AlephBERT** | 0.914 | 0.638 | 0.87 | 0.276 |
| **MPNet** | 0.903 | 0.649 | 0.78 | 0.254 |
| **LaBSE** | 0.828 | 0.375 | 0.78 | 0.453 |

**Key Findings**:
- E5 excels at detecting explicit parallels (highest cosine similarity).
- AlephBERT shows better separation between parallel and non-parallel texts, probably the preferred model.
- Combined use of E5 and AlephBERT recommended for optimal results.
