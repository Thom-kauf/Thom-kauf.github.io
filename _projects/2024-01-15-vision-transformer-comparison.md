---
title: "I-JEPA vs. Supervised ViT: Self-Supervised Transfer Learning"
layout: single-project
collection: projects
type: "Deep Learning"
date: "2024-05-01"
github: "https://github.com/Thom-kauf/ViT_Classification"
---

This project presents a comparative analysis of self-supervised vs. supervised representations in computer vision. I evaluated Meta's **I-JEPA (Image Joint-Embedding Predictive Architecture)** against a fine-tuned **Google Vision Transformer (ViT)** on CIFAR-10.

**Key Technical Challenges:**
* **Codebase Adaptation:** As no official API existed for I-JEPA at the time, I performed a deep dive into the Meta research codebase to extract the target encoder and adapt it for downstream classification tasks.
* **Architecture Engineering:** Modified the I-JEPA target encoder by adding custom Layer Normalization and an MLP head, and fine-tuned the supervised ViT output layer for a controlled performance comparison.

**Findings:**
* **Quantitative:** The Supervised ViT achieved **98.28%** accuracy, while the adapted I-JEPA reached **86.04%** within a single epoch.
* **Qualitative:** Despite lower accuracy, semantic visualization analysis suggests that I-JEPA captures more robust structural and semantic meaning in its latent representations than supervised models, which can over-rely on specific pixel features.

**Skills Demonstrated:**
* **PyTorch** architecture modification.
* Evaluation of Self-Supervised Learning (SSL) objectives.
* Qualitative analysis of semantic embeddings.