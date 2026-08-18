# Code Switching NLP | Code Saviours SI-26 | Maryam Munawar

## Overview
This repository contains the Week 6 deliverables for Phase 1 of Project 2, completed during my Machine Learning Internship at Code Saviours (SMC-Private) Limited. The primary objective of this phase is to build an original dataset from scratch that captures natural code-switching between Roman Urdu and English.

## The Problem & Methodology
Currently, there is a lack of robust AI models capable of handling the informal, mixed-language communication style naturally used by online users in Pakistan[cite: 1]. To bridge this gap, I constructed a custom NLP dataset tailored for Token Classification.

*   **Data Sources:** Raw text was sourced directly from natural, real-world conversations via Twitter/X and anonymized WhatsApp messages[cite: 1].
*   **Volume:** 152 unique code-switched sentences[cite: 1].
*   **Processing:** Extracted text from screenshot data using a custom Python OCR pipeline (`pytesseract`), formatted the outputs into Python dictionaries, and manually annotated the dataset[cite: 1].

## Labeling Scheme
The dataset utilizes a strict word-by-word token classification structure. Every single word across all 152 sentences has been manually categorized into one of three labels[cite: 1]:
*   **`URD`**: Purely Roman Urdu words.
*   **`ENG`**: Purely English words.
*   **`MIX`**: Hybrid words, consisting of fused terms or English root words combined with Urdu grammatical suffixes.

## Repository Contents & Links
*   **Colab Notebook:** `SI26-Week6-maryam.ipynb` — Contains the automated OCR extraction script, data structuring loops, and CSV conversion pipeline[cite: 1].
*   **Published Dataset:** https://huggingface.co/datasets/Maryam657775/code-switching-codesaviours-si26-maryam[cite: 1]

---
*Built for the Code Saviours Cohort SI-26 Machine Learning Pipeline.*

## Overview
This repository contains the Week 7 deliverables for Project 2 of the Machine Learning Internship at Code Saviours (SMC-Private) Limited. Following the data collection and annotation phase, this week focused on fine-tuning a state-of-the-art transformer model to perform token classification on Roman Urdu and English code-switched text.

## Methodology & Training
The base model `xlm-roberta-base` was fine-tuned to classify individual words in mixed-language sentences into one of three distinct categories: `URD` (Roman Urdu), `ENG` (English), and `MIX` (Hybrid/Morphological blends). 

*   **Base Model:** `xlm-roberta-base`
*   **Dataset:** Custom dataset of 152 manually annotated code-switched sentences.
*   **Hardware:** NVIDIA T4 GPU 
*   **Training Hyperparameters:** 5 Epochs, Batch Size of 16, Learning Rate of 2e-5, Weight Decay of 0.01.
*   **Token Alignment:** Handled subword tokenization by mapping extra tokens to `-100` to properly calculate PyTorch loss for word-level predictions.

## Evaluation Metrics
The model was evaluated on a held-out 20% test split, achieving the following performance metrics:
*   **Accuracy:** 81.73%
*   **F1 Score:** 66.05%
*   **Precision:** 74.74%
*   **Recall:** 59.17%
*   **Validation Loss:** 0.5855

## Repository Contents & Deployment Links
*   **Notebook:** `SI26-Week7-maryam.ipynb` — Contains the complete pipeline for data loading, label mapping, subword token alignment, model training, and metric evaluation.
*   **Fine-Tuned Model:** [xlm-roberta-code-switching-si26 on Hugging Face](https://huggingface.co/Maryam657775/xlm-roberta-code-switching-si26)
*   **Source Dataset:** [code-switching-codesaviours-si26-maryam](https://huggingface.co/datasets/Maryam657775/code-switching-codesaviours-si26-maryam)

---
*Built for the Code Saviours Cohort SI-26 Machine Learning Pipeline.*
