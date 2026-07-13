# Explainable Music Genre Classification Using Attention-Based CNN-LSTM

> Published at NGNDAI-2026 | Springer Lecture Notes in Networks and Systems (Scopus-indexed)

## Overview
A deep learning system for music genre classification that combines CNN spatial 
feature extraction, Bidirectional LSTM temporal modeling, and Bahdanau attention 
with Grad-CAM explainability and cross-dataset generalization analysis.

## Key Results
| Experiment | Accuracy |
|---|---|
| Baseline CNN (GTZAN) | 91.46% |
| CNN-LSTM (GTZAN) | 71.83% |
| CNN-LSTM + Attention — Proposed (GTZAN) | 74.83% |
| Pure Cross-Dataset (GTZAN → FMA) | 39.18% |
| Mixed-Source Training (GTZAN + 20% FMA → FMA) | 62.43% |

## Architecture
- **CNN Stage** — 3 convolutional blocks (32, 64, 128 filters) with Batch Normalization, MaxPooling, Dropout
- **Bidirectional LSTM** — 128 units per direction (256 total)
- **Bahdanau Attention** — weighted context vector over LSTM time steps
- **Explainability** — Grad-CAM heatmaps + attention weight visualization

## Datasets
- **GTZAN** — 1,000 audio clips, 10 genres, 30s each
- **FMA Small** — 8,000 tracks, 8 genres, 30s each

## How to Run
1. Open `music_genre_classification.ipynb` in Google Colab
2. Set runtime to GPU (T4)
3. Run cells top to bottom
4. For FMA cross-dataset evaluation, continue from Cell 18 onwards

## Requirements
See `requirements.txt`

## Tech Stack
Python | TensorFlow | Keras | Librosa | NumPy | Matplotlib | Scikit-learn | OpenCV | Google Colab

## Publication
Accepted at **NGNDAI-2026** (September 2026) — In Press
Springer Lecture Notes in Networks and Systems (LNNS)
Indexed by: Scopus, INSPEC, SCImago
