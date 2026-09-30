# Italy MedVQA — Visual Grounding in Medical Images

Evaluation results and data for the paper **"Are Large Vision Language Models Truly Grounded in Medical Images? Evidence from Italian Clinical Visual Question Answering"**, accepted at the **NeurIPS 2025 MMRL4H Workshop** (Best Presentation).

> **Fork notice:** This repository is a fork of [Federico Felizzi's original](https://github.com/felizzi/eurips2025-mmrl4h-italian-medvqa-visual-grounding). Federico Felizzi is the lead and corresponding author of the underlying work.

## Overview

This repository contains the evaluation results and data from a study investigating whether frontier large vision-language models (VLMs) genuinely ground their answers in medical images when responding to Italian clinical visual-question-answering (VQA) questions.

The benchmark consists of **60 curated Italian clinical VQA questions** drawn from the **EuropeMedQA SSM subset**, each explicitly requiring image interpretation. The questions span multiple medical specialties, approximately:

| Specialty | Share |
|-----------|-------|
| Cardiology | 27% |
| Dermatology | 13% |
| Orthopedics | 12% |
| Neurology | 10% |

## Evaluation Setup

Four state-of-the-art VLMs were evaluated, each run with **10 repetitions** to ensure statistical reliability:

- **Claude Sonnet 4.5**
- **GPT-4o**
- **GPT-5-mini**
- **Gemini 2.0**

To test whether models truly integrate visual and textual information, correct medical images were substituted with blank placeholders and accuracy was compared against the full-image setting. The results reveal striking variability in visual dependency across models, along with confident explanations for fabricated visual interpretations — highlighting critical differences in model robustness and the need for rigorous evaluation before clinical deployment.

## Repository Structure

- **`data/`** — Images used for evaluation
- **`revision_11_25/`** — Claude Sonnet 4.5 evaluation results (reasoning + aggregated results for 10 repetitions)
- **`revision_11_25_OpenAI/`** — OpenAI model evaluation results (GPT-4o and GPT-5-mini)
- **`revision_11_25_Gemini/`** — Gemini model evaluation results
- **`original_submission/`** — Results from the original workshop submission
- **`overall_results/`** — Aggregated results across all models

## Paper

- **Title:** Are Large Vision Language Models Truly Grounded in Medical Images? Evidence from Italian Clinical Visual Question Answering
- **arXiv:** [arxiv.org/abs/2511.19220](https://arxiv.org/abs/2511.19220)
- **Workshop:** [NeurIPS 2025 MMRL4H — Best Presentation](https://multimodal-rep-learning-for-health.github.io)

### Authors

Federico Felizzi, Olivia Riccomi, Michele Ferramola, Francesco Andrea Causio, Manuel Del Medico, Vittorio De Vita, Lorenzo De Mori, Alessandra Piscitelli, Pietro Eric Risuleo, Bianca Destro Castaniti, Antonio Cristiano, Alessia Longo, Luigi De Angelis, Mariapia Vassalli, Marcello Di Pumpo

### BibTeX

```bibtex
@misc{felizzi2025large,
  title        = {Are Large Vision Language Models Truly Grounded in Medical Images? Evidence from Italian Clinical Visual Question Answering},
  author       = {Felizzi, Federico and Riccomi, Olivia and Ferramola, Michele and Causio, Francesco Andrea and Del Medico, Manuel and De Vita, Vittorio and De Mori, Lorenzo and Piscitelli, Alessandra and Risuleo, Pietro Eric and Destro Castaniti, Bianca and Cristiano, Antonio and Longo, Alessia and De Angelis, Luigi and Vassalli, Mariapia and Di Pumpo, Marcello},
  year         = {2025},
  eprint       = {2511.19220},
  archiveprefix= {arXiv},
  primaryclass = {cs.CV},
  note         = {Accepted at the NeurIPS 2025 MMRL4H Workshop (Best Presentation)}
}
```

## License

See the `LICENSE` file for details.
