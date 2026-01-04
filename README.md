# LSTM-Based-Next-Word-Text-Generation-from-Wikipedia-Biographies
# Overview

This project implements a next-word text generation system using a Long Short-Term Memory (LSTM) neural network. The model is trained on Wikipedia biography text to learn sequential word patterns and generate text one word at a time.
The goal of this project is hands-on practice with sequence modeling and NLP fundamentals, not to build a production-grade language model.

# Dataset

Source: Wikipedia biographies
Data type: Plain text (.txt)
Content includes multiple biographies concatenated into a single corpus
Basic cleaning performed (removed references, tables, and non-text elements)

# Approach

Text Preprocessing

Tokenized text using Keras Tokenizer
Converted text into integer sequences
Applied padding to ensure uniform input length
Built vocabulary from the corpus (~2000 unique tokens)

# Model Architecture

Embedding Layer for word representation
LSTM Layer for sequence learning
Dense + Softmax Layer for next-word probability prediction

# Training

Optimized using categorical cross-entropy loss
Trained with validation split to observe generalization behavior
Observed training instability due to random initialization and small dataset size

# Text Generation

Implemented temperature-based sampling to control randomness in predictions
Compared greedy decoding (argmax) vs probabilistic sampling
Temperature sampling helped reduce repetitive word generation

# Results & Observations

Training accuracy varied across runs due to stochastic optimization
Validation accuracy fluctuated and degraded over epochs, indicating overfitting
High accuracy did not correlate with high-quality text generation
The project demonstrates why LSTMs struggle with long-term dependencies and motivates modern transformer-based models

# Limitations

Small dataset size leads to high variance and overfitting
Accuracy is not a reliable metric for text generation tasks
LSTM architecture has limited context retention compared to transformers
Not intended for deployment or production use

# Key Learnings

Sequence modeling using LSTM networks
Practical challenges in NLP evaluation
Importance of sampling strategies in text generation
Understanding model limitations and failure modes

# Technologies Used

Python
TensorFlow / Keras
NumPy
Google Colab

# Future Improvements

Train on a larger and more diverse corpus
Experiment with stacked or bidirectional LSTMs
Replace LSTM with transformer-based architectures
Use perplexity as an evaluation metric
