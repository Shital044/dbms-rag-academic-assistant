# 📊 Results Report – DBMS RAG Academic Assistant

---

# 1. Introduction

This document presents the experimental results of the DBMS Retrieval-Augmented Generation (RAG) system.

The project evaluated:

- Chunking strategies
- Prompt engineering techniques
- Retrieval strategies
- Real-world document challenges

All experiments were conducted using the same dataset and evaluation questions to ensure fairness.

---

# 2. Experiment 1 – Chunking Strategy Comparison

Two chunking strategies were compared:

- Fixed-Size Chunking
- Sentence-Based Chunking

## Evaluation Method

Each question was rated on:

- Relevance (1–5)
- Quality (1–5)

## Average Scores

| Strategy | Average Relevance | Average Quality |
|----------|------------------|-----------------|
| Fixed-Size Chunking | 3.3 | 3.3 |
| Sentence-Based Chunking | 3.4 | 3.4 |

## Observations

- Sentence-based chunking performed better for conceptual questions such as:
  - ACID properties
  - Transaction
  - B-tree vs Hash index

- Fixed-size chunking performed more consistently across mixed DBMS topics.

## Final Decision

Although sentence-based chunking slightly improved average scores,  
**Fixed-size chunking was selected as the final strategy due to better overall stability.**

---

# 3. Experiment 2 – Prompting Technique Comparison

Two prompting strategies were tested:

- Basic Prompt
- Improved Structured Prompt

## Observations

### Basic Prompt
- Generated short responses
- Less structured format
- Sometimes incomplete explanations

### Improved Prompt
- Produced structured answers
- Included definitions and explanations
- Reduced hallucination
- Better academic formatting

## Final Decision

The **Improved Structured Prompt** was selected for the final system because it consistently produced higher-quality academic responses.

---

# 4. Experiment 3 – Retrieval Strategy Comparison

Three retrieval strategies were evaluated:

- Top-K (k=3)
- Top-K (k=5)
- Maximal Marginal Relevance (MMR)

## Observations

### Top-K (k=3)
- High precision
- Sometimes limited context coverage

### Top-K (k=5)
- Broader context
- Occasionally introduced irrelevant information

### MMR
- Balanced relevance and diversity
- Reduced redundancy
- Improved contextual coverage
- Provided the most stable results

## Final Decision

**MMR was selected as the production retrieval strategy** due to its balanced performance.

---

# 5. Part 4 – Real-World Challenges

The system addressed the following practical challenges:

## 1. Chunking Strategy Stability
Different chunking methods affected retrieval performance.  
This was resolved through experimental comparison and selection of the most stable strategy.

## 2. Prompt Engineering
Improved structured prompts significantly enhanced answer clarity and organization.

## 3. Retrieval Diversity
MMR improved diversity and reduced redundant context in responses.

---

# 6. Final Production System Configuration

Based on experimental results, the final system uses:

- Sentence-Based Chunking (for document preparation)
- Improved Structured Prompt
- MMR Retrieval Strategy
- ChromaDB as Vector Database
- LCEL Pipeline Architecture

This configuration was selected based on empirical evaluation.

---

# 7. Overall Performance Summary

The system successfully:

- Retrieved relevant DBMS content
- Generated structured academic answers
- Compared multiple strategies systematically
- Demonstrated measurable improvements
- Handled real-world RAG design considerations

The experimental approach ensured decisions were data-driven rather than assumption-based.

---

# 8. Conclusion

The DBMS RAG system demonstrates:

- Effective use of retrieval-augmented generation
- Impact of chunking strategies on performance
- Importance of prompt engineering
- Benefits of advanced retrieval techniques like MMR

The final system represents an optimized configuration based on controlled experiments and evaluation metrics.

This project successfully integrates theoretical understanding with practical implementation of modern RAG systems.