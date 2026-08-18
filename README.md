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
