# TOPSIS-BASED SELECTION OF PRETRAINED TEXT SENTENCE SIMILARITY MODELS

---

## 1. OVERVIEW

This project applies **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** to identify the best pretrained **text sentence similarity** model from **Hugging Face**.

The selection is performed using multiple evaluation criteria such as **semantic similarity performance, inference efficiency, model size, and embedding dimension**.

The main objective of this work is to demonstrate how **multi-criteria decision-making (MCDM)** techniques like TOPSIS can be practically used for **systematic model selection in Natural Language Processing (NLP)** tasks.

---

## 2. METHODOLOGY

In this assignment, the **TOPSIS method** is used to rank pretrained **sentence similarity models** based on multiple performance-related criteria.

TOPSIS works by comparing different alternatives and selecting the model that is **closest to the ideal solution** and **farthest from the worst solution**.

---

### 2.1 MODEL SELECTION

The following pretrained **sentence similarity models** were selected from **Hugging Face**:

- all-MiniLM-L6-v2  
- all-mpnet-base-v2  
- paraphrase-distilroberta-base-v1  
- bert-base-nli-mean-tokens  

Only **general-purpose pretrained models** were considered.  
Fine-tuned or domain-specific models were avoided to ensure a **fair and unbiased comparison**.

---

### 2.2 EVALUATION CRITERIA

Each model was evaluated using the following criteria:

**AVERAGE COSINE SIMILARITY SCORE**  
Measures how effectively the model captures semantic similarity between sentence pairs. Higher values indicate better performance.

**INFERENCE TIME (SECONDS)**  
Represents the average time taken by the model to generate sentence embeddings. Lower values are preferred.

**MODEL SIZE (MB)**  
Indicates the memory footprint of the model. Smaller models are easier to deploy.

**EMBEDDING DIMENSION**  
Represents the richness of sentence representations. Higher values are preferred.

Similarity score and embedding dimension are treated as **benefit criteria**, while inference time and model size are treated as **cost criteria**.

---

### 2.3 DECISION MATRIX AND WEIGHT ASSIGNMENT

The measured values for all criteria were arranged in the form of a **decision matrix**, where:

- Rows represent the models  
- Columns represent the evaluation criteria  

Since the criteria have different units, **normalization** was applied.

The following weights were assigned based on relative importance:

- Similarity Score: 0.4  
- Inference Time: 0.2  
- Model Size: 0.2  
- Embedding Dimension: 0.2  

---

### 2.4 TOPSIS COMPUTATION

After normalization and weighting:

- Ideal best and ideal worst solutions were calculated  
- The distance of each model from these solutions was computed  
- A **TOPSIS score** was obtained for each model  

The model with the **highest TOPSIS score** was ranked as the best-performing model.

---

## 3. RESULTS AND ANALYSIS

The TOPSIS scores obtained for each model were used to rank the pretrained sentence similarity models.

The ranking results indicate that **all-MiniLM-L6-v2** achieved the highest TOPSIS score, followed by **all-mpnet-base-v2**, **paraphrase-distilroberta-base-v1**, and **bert-base-nli-mean-tokens**.

Although some models provide richer embeddings, their higher inference time and model size negatively affected their overall TOPSIS ranking.

---

## 4. RESULT VISUALIZATION

A bar graph was used to visualize the **TOPSIS scores** of all evaluated models.

<img width="688" height="555" alt="Screenshot 2026-01-27 145646" src="https://github.com/user-attachments/assets/f13d6a91-6872-4f6d-a2bb-53b6cfe0c40b" />

The graph clearly supports the ranking obtained through the TOPSIS method and provides an intuitive comparison of model performance across multiple criteria.

---

## 5. FINAL CONCLUSION

Based on the TOPSIS analysis, **all-MiniLM-L6-v2** is identified as the best pretrained **Text Sentence Similarity** model among the evaluated alternatives.

It offers the most balanced trade-off between semantic accuracy, computational efficiency, and model size, making it the **optimal choice** according to the TOPSIS method.

---
