# 🧠 The Illusion of Certainty: Uncertainty Quantification for LLMs Fails under Ambiguity

[![Paper Status](https://img.shields.io/badge/arXiv-2502.01234-red.svg)](https://arxiv.org/abs/2502.01234)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![HuggingFace Datasets](https://img.shields.io/badge/Datasets-on%20🤗%20Hugging%20Face-yellow.svg)](https://hf.co/collections/ttomov/llm-uncertainty-under-ambiguity)

This repository accompanies the paper:

> **Tim Tomov, Dominik Fuchsgruber, Tom Wollschläger, Stephan Günnemann**  
> *The Illusion of Certainty: Uncertainty Quantification for LLMs Fails under Ambiguity*  

---

## 📖 Overview

Accurate **uncertainty quantification (UQ)** in large language models (LLMs) is essential for reliable and trustworthy deployment. However, most existing UQ methods are evaluated under the restrictive assumption that every question has a **single correct answer** — that is, *zero aleatoric uncertainty*.

In this work, we show that:

- When **ambiguity** is present (multiple valid answers), current uncertainty estimators degrade to *close-to-random performance*.
- This failure is consistent across three major UQ paradigms:
  1. **Predictive-distribution–based estimators** (entropy, MSP, semantic uncertainty)
  2. **Hidden-state–based estimators** (linear and MLP probes)
  3. **Ensemble-based estimators** (Bayesian mutual information)
- We provide **theoretical proofs** explaining why these estimators are fundamentally limited under ambiguity.

To rigorously evaluate this phenomenon, we introduce two new **ambiguous QA datasets** with **explicit ground-truth answer distributions**.

---

## 🧩 Datasets

| Dataset | Description |  Link |
|:--------|:-------------|:------|
| **MAQA\*** | Ambiguous QA with factual co-occurrence–based ground-truth distributions | [🤗 `ttomov/maqa_star`](https://huggingface.co/datasets/ttomov/maqa_star) |
| **AmbigQA\*** | Extension of AmbigQA with estimated answer probabilities and verified entailment | [🤗 `ttomov/ambigqa_star`](https://huggingface.co/datasets/ttomov/ambigqa_star) |

Both datasets provide **ground-truth distributions \(p^*(y|x)\)** estimated from factual **co-occurrence statistics** in large corpora (Wikipedia, RedPajama-V1, The Pile) and validated via entailment models.  
They enable, for the first time, *quantitative* evaluation of epistemic vs. aleatoric uncertainty in LLMs.

---

## 🧮 Repository Status

> ⚠️ **Code coming soon.**  
> The repository currently contains the paper text and dataset links.  
> Full experimental code and analysis scripts will be released upon acceptance.

---

## 📚 Citation

If you use our datasets or results, please cite:


