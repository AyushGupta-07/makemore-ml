
````markdown
# Character-Level Language Model — Makemore

A character-level language modeling project built with PyTorch to explore how Transformer-based language models learn to generate new names from a text dataset.

The project demonstrates the core concepts behind modern language models, including token embeddings, self-attention, Transformer blocks, feed-forward networks, optimization, training loss, model checkpointing, and text generation.

---

## Project Overview

This project uses a dataset of names to train a small character-level Transformer language model.

Instead of predicting complete words directly, the model learns to predict the next character based on the preceding characters. After training, the model can generate new name-like sequences that resemble patterns learned from the training data.

### Example Generated Outputs

Examples produced during training include:

```text
eshav
deicra
mabez
axzut
anasses
rozalena
barnon
zareeh
````

These outputs demonstrate the model's ability to generate previously unseen character sequences based on learned patterns.

---

## Key Concepts

* Character-level language modeling
* Token and positional embeddings
* Self-attention
* Transformer architecture
* Multi-layer perceptron / feed-forward networks
* Layer normalization
* Autoregressive next-token prediction
* Cross-entropy loss
* Gradient-based optimization
* Model checkpointing
* TensorBoard training logs
* Text generation

---

## Technology Stack

* **Python**
* **PyTorch**
* **NumPy**
* **TensorBoard**
* **Transformer architecture**
* **Git & GitHub**

---

## Model Architecture

The project implements a compact Transformer-based language model.

The overall flow is:

```text
Input Names
     ↓
Character Tokenization
     ↓
Character Embeddings
     ↓
Positional Information
     ↓
Self-Attention
     ↓
Feed-Forward / MLP
     ↓
Layer Normalization
     ↓
Next-Character Prediction
     ↓
Generated Text
```

The model is trained autoregressively, meaning that each predicted character becomes part of the context used to predict subsequent characters.

---

## Dataset

The model uses `names.txt`, where each line contains a name.

The dataset is used to create character sequences for next-character prediction.

The model learns statistical patterns such as:

* Which characters commonly follow one another
* Common character combinations
* Name-length patterns
* Character-level structure of names

---

## Training

The model was trained using PyTorch on a CPU environment.

Training progress is recorded using TensorBoard, allowing loss and training behavior to be inspected over time.

A trained model checkpoint is stored in:

```text
out/model.pt
```

TensorBoard event files are also stored in:

```text
out/
```

---

## Running the Project

### 1. Clone the repository

```bash
git clone https://github.com/AyushGupta-07/makemore-ml.git
cd makemore-ml
```

### 2. Install dependencies

```bash
python -m pip install torch tensorboard
```

### 3. Run the model

```bash
python makemore.py
```

The script trains the model and generates name-like sequences.

---

## TensorBoard

Training logs can be visualized using TensorBoard.

Run:

```bash
tensorboard --logdir out
```

Then open the local TensorBoard address displayed in the terminal.

---

## Project Structure

```text
makemore-ml/
│
├── makemore.py
├── names.txt
├── README.md
├── LICENSE
│
└── out/
    ├── model.pt
    └── events.out.tfevents.*
```

---

## Learning Outcomes

Through this project, I explored:

* How character-level language models represent text
* How Transformer architectures process sequential data
* How self-attention helps models learn contextual relationships
* How neural networks are trained using gradient descent
* How language models perform autoregressive generation
* How to monitor training using TensorBoard
* How trained model checkpoints can be saved and reused

---

## Portfolio Context

This project is part of my machine learning and AI engineering portfolio, with a focus on understanding the foundations behind modern NLP and generative AI systems.

It complements my other projects involving:

* End-to-end machine learning
* MLOps
* Customer churn prediction
* Fraud detection
* NLP and language modeling

---

## Attribution

This project is an **adapted learning implementation based on Andrej Karpathy's open-source `makemore` project**, used for educational and portfolio learning purposes.

Original project:

[https://github.com/karpathy/makemore](https://github.com/karpathy/makemore)

The original implementation and educational material are credited to Andrej Karpathy.

---

## Author

**Ayush Gupta**

GitHub:
[https://github.com/AyushGupta-07](https://github.com/AyushGupta-07)
