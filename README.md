
# 🧠 Names-Generator Project

This project demonstrates the evolution of name generation using progressively more powerful neural network models. The goal is to generate realistic-looking names from scratch by training models on a dataset of real names.

---

## 📦 Overview

We explore the following setups:

1. **Without Training** – Names are generated from random noise.
2. **Small Neural Network** – Basic architecture with minimal training.
3. **Deep Neural Network** – Advanced architecture using embeddings, linear layers, normalization, and non-linearities.

---

## 🧪 Results

### 🔹 1. Without Training

Names generated purely from noise (no training or learning involved):

```
bhrnrekvrcfhyjrenlf.
lumyuovtqjyotnhgxuul.
udrltrsroghvx.
qttygzsdskyuilbcsqfhznsrsnsxtwuwovgmiqhvhbmbsvfyg.
sxanod.
szkdw.
yzljuqahljmgmzivsztfck.
nskmnr.
gmzymbcck.
lobwavbmwnvnujwmwamdejaynpgikaztmkdcxslunhxulzpqrjurfphmmfagmigvfngmkrpskkkyjpctebsyioqchegfu.
```

_(Note: Names appear as gibberish due to lack of learned patterns.)_

---

### 🔹 2. Small Neural Network

A basic neural network trained on the dataset begins to pick up on name-like patterns:

```
bhriretorco.
maren.
f.
lemauovieiynana.
sa.
l.
merlershonine.
stty.
zade.
drilyarlll.
```

_(More structure and shorter name-like tokens begin to emerge.)_

---

### 🔹 3. Deep Neural Network

A deeper, well-trained network with multiple layers and batch normalization produces highly realistic names:

```
kylie.
kaelyn.
arios.
bowin.
avija.
jaelyne.
kinger.
leona.
maelynn.
alecia.
```

> ✨ The model learns patterns in syllables, prefixes, suffixes, and structure of real names.

---

## 🧠 Deep Neural Network Architecture

The architecture used in the deep model is:

```
Embedding          : (32, 8, 24)
FlattenConsecutive : (32, 4, 48)
Linear             : (32, 4, 128)
BatchNorm1d        : (32, 4, 128)
Tanh               : (32, 4, 128)
FlattenConsecutive : (32, 2, 256)
Linear             : (32, 2, 128)
BatchNorm1d        : (32, 2, 128)
Tanh               : (32, 2, 128)
FlattenConsecutive : (32, 256)
Linear             : (32, 128)
BatchNorm1d        : (32, 128)
Tanh               : (32, 128)
Linear             : (32, 27)
```

- Batch size: 32
- Embedding dim: 24
- Vocabulary size: 27 (characters)
- Output: Probabilities over next character

---

## 🚀 Getting Started

1. Install Python and PyTorch.
2. Clone the repo.
3. Prepare your dataset of names (one per line).
4. Train using the small or deep model.
5. Generate new names using the trained model.

---

## 📚 Inspirations

- [makemore (Andrej Karpathy)](https://github.com/karpathy/makemore)
- NLP and character-level modeling techniques

---

## 🧑‍💻 Author

This project was built as an experiment in character-level language modeling using deep learning.

