# RAG (Retrieval Augmented Generation) with Re-Ranking

## Overview

In the world of GenAI, RAG (Retrieval Augmented Generation) enhances large language models (LLMs) by providing additional context along with a query to generate better responses.

## Problem with Basic RAG

A basic RAG setup often delivers suboptimal accuracy because it may not provide the most precise context to the LLM. Only the top_k results from vector search are passed to the LLM, potentially missing out on other relevant information.

### Key Issues

1. **Context Loss:** Important context may be lost as we only consider top_k results.
2. **LLM Context Limitation:** LLMs have a limited context window, restricting how much information can be processed.
3. **LLM Recall Performance:** Too many tokens can degrade LLM recall performance, affecting response quality.

## Solution: Re-Ranking

To refine RAG implementation, re-ranking is crucial. A re-ranking model assigns a matching score to query-document pairs, rearranging vector search results to prioritize the most relevant ones.

### Implementation Steps

1. **Vector Search:** Quickly retrieve relevant documents from a large dataset.
2. **Re-Ranking:** Apply re-ranking to prioritize the most relevant documents.
3. **Enhanced Context:** Pass top-ranked documents to the LLM for more accurate responses.

## Conclusion

Re-ranking addresses the limitations of basic RAG setups by ensuring the LLM receives the most relevant context, thus enhancing the accuracy and precision of generated responses.
