# RNN and LSTM-Based Next-Word Prediction for a Domain-Specific Medical Text Corpus

This project implements and compares **Simple Recurrent Neural Network (RNN)** and **Long Short-Term Memory (LSTM)** models for next-word prediction using a domain-specific medical text corpus.

Given the previous 20 words of a medical text sequence, the models predict the most likely next word from a vocabulary of 20,000 words.

---

## Project Objective

The main objectives of this project are to:

- Preprocess a domain-specific medical text corpus
- Convert text into numerical sequences using tokenization
- Generate fixed-length input sequences for next-word prediction
- Train a Simple RNN as a baseline model
- Train an LSTM model using the same dataset and settings
- Compare RNN and LSTM performance
- Generate Top-1 and Top-5 next-word predictions
- Build a simple next-word prediction system

---

## Dataset

The project uses a **medical text corpus** obtained from Kaggle.

The dataset contains medical documents belonging to multiple medical categories.

The original dataset contains:

- `train.dat`
- `test.dat`

The class labels are removed because this project performs **language modeling / next-word prediction**, not text classification.

The raw dataset is not included in this repository because of its size.

---

## Project Workflow

```text
Medical Text Dataset
        |
        v
Text Cleaning
        |
        v
Remove Category Labels
        |
        v
Tokenizer
        |
        v
Vocabulary Creation
        |
        v
Word-to-Integer Conversion
        |
        v
Sliding Window Sequence Generation
        |
        v
20 Previous Words ---> Next Word
        |
        +---------------------+
        |                     |
        v                     v
   Simple RNN               LSTM
        |                     |
        v                     v
   Evaluation             Evaluation
        \                     /
         \                   /
          ------ Compare -----
                 |
                 v
        Next-Word Prediction
