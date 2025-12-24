# NanoGPT-Math: DPO Fine-Tuning for Mathematical Reasoning

## Overview

This repository is based on the official **NanoGPT-Math** assignment framework.  
The project focuses on **Direct Preference Optimization (DPO)** to fine-tune a pretrained NanoGPT model for improved mathematical reasoning.

Only the components related to **DPO training and preference data** are modified.  
All pretrained models and core architecture files are kept unchanged, as required.

---

## Base Repository

The original base code is provided at:  
https://github.com/zhouyuan888888/NanoGPT-Math

The following files are part of the provided framework:

- `sft/gpt.pt` — Pretrained NanoGPT model  
- `sft/meta.pkl` — Codebook used during pretraining  
- `configurator.py` — Default configuration script (unchanged)  
- `model.py` — NanoGPT model definition (unchanged)

> ⚠️ **Note**: `configurator.py` and `model.py` are from the official NanoGPT repository and are **not modified**, as instructed.

---

## Modified Components

### 1. DPO Training Script (`dpo/dpo.ipynb`)

This Jupyter notebook is the **main implementation file** for this assignment.  
Modifications include:

- Completing the DPO fine-tuning pipeline
- Loading pretrained NanoGPT weights
- Training with preference-based optimization
- Evaluating model behavior after DPO fine-tuning

The notebook is designed to be run sequentially.

---

### 2. Preference Data (`dpo/pos_neg_pairs.json`)

This JSON file contains **positive–negative response pairs** used for DPO training.

- The original file includes only toy examples
- Additional preference pairs are collected and appended
- Each data item represents:
  - A prompt
  - A preferred (positive) response
  - A less preferred (negative) response

This dataset directly determines the optimization signal in DPO.

---

## Methodology

- Start from a **supervised fine-tuned (SFT) NanoGPT model**
- Apply **Direct Preference Optimization (DPO)** using human-curated preference pairs
- Optimize the model to prefer mathematically correct and well-reasoned outputs
- Evaluate improvements qualitatively through test prompts

---

## Key Learning Outcomes

- Understanding preference-based learning in language models
- Practical implementation of Direct Preference Optimization (DPO)
- Data collection and structuring for preference learning
- Fine-tuning small language models for reasoning tasks

---

## Author

**Yichen Qu**

This project is completed as part of an academic assignment and follows the provided NanoGPT-Math framework.
