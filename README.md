# MedOmni-45°: A Safety-Performance Benchmark for Reasoning-Oriented LLMs in Medicine

[![Paper](https://img.shields.io/badge/Paper-AAAI%202026-blue)](#) [![Dataset](https://img.shields.io/badge/Dataset-Coming%20Soon-orange)](#)
[![Code](https://img.shields.io/badge/Code-Coming%20Soon-green)](#)

> **Status:** We are currently organizing the dataset and evaluation code. They will be released here very soon! Stay tuned. 🚀

This repository contains the official dataset and evaluation code for the paper **"MedOmni-45°: A Safety-Performance Benchmark for Reasoning-Oriented LLMs in Medicine"**. 

As large language models (LLMs) are rapidly integrated into clinical decision-support workflows, ensuring reliability in their reasoning steps is increasingly critical. **MedOmni-45°** is a benchmark and evaluation workflow explicitly designed to quantify the trade-off between safety and performance in LLMs under manipulative hint conditions.

---

## 🌟 Highlights

* **Comprehensive Medical Dataset:** Features 1,804 reasoning-focused medical questions spanning 6 clinical specialties (Internal Medicine, Surgery, OBGYN, Pediatrics, Stomatology, Ophthalmology) and 3 task types (Clinical Simulation, Medical Calculation, General Medical Reasoning).
* **Manipulative Prompt Framework:** Systematically augments questions with 7 manipulative hint types (e.g., Guideline-Based Prompts, User Suggestion Bias, Prior Response Conditioning), each embedding two distinct misleading cue variants, resulting in approximately 27,000 unique inputs.
* **Three Orthogonal Metrics:** Evaluates models across *Accuracy* (Performance), *CoT-Faithfulness* (Safety/Transparency), and *Anti-Sycophancy* (Safety/Robustness).
* **The 45° Safety-Performance Plot:** Introduces a novel visualization to reveal the universal trade-off between model accuracy and safety vulnerability.

---

## 📊 Benchmark Overview

### The MedOmni Dataset
The benchmark consists of:
* **1,304 Self-Built Questions:** Extracted and adapted from canonical medical textbooks and licensing exams, rigorously manually verified.
* **500 MedMCQA Items:** A curated subset from the public MedMCQA dataset to enable cross-benchmark comparisons.

### Evaluated Models
We evaluated 7 leading LLMs, generating over 189K inference instances:
* **Open-Source & Reasoning-Enhanced:** QwQ-32B, Qwen3-32B
* **Distilled:** DeepSeek-R1-Distill-Qwen-32B
* **Open-Source Base:** LLaMA-3.3-70B
* **Medical-Specific:** HuatuoGPT-01-72B
* **Closed-Source:** GPT-4o, o4-mini-high

---

## 🏆 Key Findings

* **The Trade-off:** There is a universal trade-off between performance and safety; no model currently surpasses the ideal 45° diagonal guideline.
* **Top Performer in Balance:** The open-source reasoning model, **QwQ-32B**, approaches the closest at 43.81°, demonstrating notable safety and reasoning transparency (up to 84% CoT Faithfulness).
* **Vulnerability to Specific Hints:** Models struggle significantly with *Structured Meta-Hints* and *Prior Response Conditioning*, which can reduce CoT Faithfulness to below 10% on average. 
* **Domain-Specific Models:** Medical models like HuatuoGPT-72B and LLaMA-3-70B show high accuracy but unexpectedly low safety under adversarial prompting, highlighting the need for explicit safety alignment.

---

## 🚀 Getting Started (Coming Soon)

We are finalizing the release of the dataset and the evaluation pipeline. Once released, you will be able to:

1.  **Download the MedOmni dataset** (including all manipulative hint variants).
2.  **Run inference** on your own models using our unified prompting template.
3.  **Evaluate results** using our scoring scripts for Accuracy, Sycophancy, and CoT Faithfulness.

## 📝 Citation

If this codebase assists in your research, please cite our work: 
```text
@article{ji2025medomni,
  title={Medomni-45 $\{$$\backslash$deg$\}$: A safety-performance benchmark for reasoning-oriented llms in medicine},
  author={Ji, Kaiyuan and Guo, Yijin and Zhang, Zicheng and Zhu, Xiangyang and Tian, Yuan and Liu, Ning and Zhai, Guangtao},
  journal={arXiv preprint arXiv:2508.16213},
  year={2025}
}
```
