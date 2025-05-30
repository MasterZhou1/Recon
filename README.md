# <img src="images/ai_economist.png" width="50"> Recon: Reasoning Like an Economist

**Post-Training on Economic Problems Induces Strategic Generalization in LLMs**  
Yufa Zhou*, Shaobo Wang*, Xingyu Dong*, et al. (*equal contribution)

<!-- [[📄 Paper]](https://arxiv.org/abs/placeholder)   -->

---

## 📖 Introduction

Recon is a 7B-parameter open-source large language model designed for economic and strategic reasoning. It is trained via a two-stage pipeline: Supervised Fine-Tuning (SFT) and Group Relative Policy Optimization (GRPO), using a curated dataset of 2,100 high-quality economic reasoning problems across 15 categories. Recon aims to bridge the gap between single-agent reasoning and multi-agent strategic behavior, enabling LLMs to generalize from textbook economic problems to complex multi-agent games. Our results show that domain-aligned post-training enhances both benchmark accuracy and emergent rational behavior in multi-agent settings.

---

## ✨ Overview

Recon follows a three-step pipeline for enabling economic and strategic reasoning in LLMs:

1. **Dataset Curation & Reasoning Trace Distillation:** High-quality economic problems and reasoning traces are curated from benchmarks and teacher models to form the Recon dataset.
2. **Post-Training via SFT & RL:** A base model is post-trained using Supervised Fine-Tuning (Recon-SFT) and Group Relative Policy Optimization (Recon-RL) on the curated dataset.
3. **Evaluation:** The resulting models are evaluated on economic reasoning benchmarks, self-play, and multi-agent games against opponent agents.

<p align="center">
  <img src="images/pipeline.png" width="600"/>
</p>

---

## 🏗️ Repo Structure

- `data/` — Datasets and benchmarks for economic reasoning and multi-agent games
- `images/` — Figures and diagrams for documentation and papers
- `SFT_Training.ipynb` — Supervised fine-tuning pipeline
- `GRPO_Training.ipynb` — GRPO training pipeline
- `data_curation.ipynb` — Dataset curation and reasoning trace distillation
- `vllm_evaluate.ipynb` — Model evaluation scripts

## 🔍 Insights & Takeaways

- **Domain-aligned post-training works:** Training LLMs on structured economic reasoning tasks leads to strong generalization, enabling models to perform well in both single-agent and multi-agent strategic settings.
- **Strategic behavior emerges:** Recon models not only solve textbook problems but also exhibit rational, game-theoretic behavior in unseen interactive games, demonstrating transferable equilibrium reasoning.
- **SFT + GRPO is effective:** The two-stage pipeline (SFT → GRPO) yields clear gains in both accuracy and strategic alignment, validating this approach for aligning LLMs with economic and multi-agent objectives.
- **Scalable and interpretable alignment:** Recon's approach provides a scalable route to agent alignment, with richer, self-correcting reasoning chains that enhance interpretability and facilitate auditing.

## 📚 Citation

If you find Recon helpful for your research, please cite our work (BibTeX coming soon):

```
TBD
```

## 📬 Contact

For questions or collaborations, feel free to reach out:

📧 yufa.zhou[at]duke.edu








