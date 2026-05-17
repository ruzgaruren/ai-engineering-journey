# Day 02 — LLMs, Embeddings, Attention & Transformer Architecture

## Objective

The goal of Day 2 was to deeply understand how modern Large Language Models work internally.

---

# 1. Large Language Models (LLMs)

LLMs are probabilistic systems trained on massive text datasets.

Core idea:
Predict the next token based on context.

Important insight:
LLMs do not truly think.
They generate statistically probable outputs.

---

# 2. Tokens

LLMs process tokens instead of words.

Tokens are fragmented numerical representations of text.

Important insight:
Turkish consumes more tokens because it is an agglutinative language.

---

# 3. Context Window

Context window defines how many tokens the model can process simultaneously.

Larger context:
- more memory
- more relationships
- harder attention computation

---

# 4. Hallucination

Hallucination occurs when the model generates plausible but incorrect information.

Reason:
LLMs optimize probability, not truth.

---

# 5. Embeddings

Embeddings convert meaning into numerical vector coordinates.

Example:

Cat:
[0.82, -0.11, 0.45, ...]

Important insight:
Embeddings represent semantic meaning mathematically.

---

# 6. Vector Space

All embeddings exist inside a high-dimensional semantic vector space.

Semantically similar concepts cluster together:
- cat
- dog
- tiger

may exist near each other.

---

# 7. Semantic Search

Traditional search:
keyword matching.

Semantic search:
meaning similarity.

---

# 8. Vector Databases

Vector databases store embeddings and retrieve semantically similar information.

---

# 9. Retrieval-Augmented Generation (RAG)

RAG combines:
- information retrieval
- LLM generation

Pipeline:
Query → Embedding → Vector Search → Retrieved Context → LLM Response

---

# 10. Attention Mechanism

Attention calculates which tokens are important relative to others.

Example:
"Ali went to the bank and withdrew money."

The phrase "withdrew money" increases the probability that "bank" refers to a financial institution.

---

# 11. Transformers

Transformers revolutionized AI by allowing models to analyze relationships between all tokens simultaneously.

Key innovation:
Parallel attention computation.

---

# Key Insight of Day 2

Modern AI systems are built on:
- probability
- semantic geometry
- relationship networks
- attention mechanisms

AI does not understand reality directly.
It learns the statistical traces of reality encoded in language.
