# Where to Apply LoRA for Reasoning: SFT or RL?

**Author:**  Yiming Luo  
**Supervisor:**  Li Li  
**Institution:** Faculty of Science and Technology, University of Macau  
**Date:** August 21, 2025

---

# Abstract

This project addresses the problem of enhancing the reasoning capabilities of Large Language Models (LLMs) under parameter-efficient fine-tuning (PEFT) constraints. Leveraging Low-Rank Adaptation (LoRA) technology and both Supervised Fine-Tuning (SFT) and Reinforcement Learning (RL) algorithms, we developed a hybrid fine-tuning framework that assigns tasks based on data characteristics and merges LoRA modules accordingly. The system was evaluated using reasoning-centric metrics on benchmarks such as GSM8K, MATH, and MBPP, achieving superior performance compared to single-method fine-tuning approaches. This work demonstrates the feasibility of orchestrating SFT and RL under PEFT for reasoning enhancement, and provides a foundation for future research on hybrid adaptation strategies in high-stakes, domain-specific tasks.

---

## Table of Contents
#
1.  [Introduction](#-1-introduction)
2.  [key Contribution](#-2-objectives-and-key-contributions)
3.  [Required Skills](#-3-required-skills)
4.  [Number of Students](#-4-number-of-students)

## 🧠 1. Introduction
LLMs have achieved unprecedented success across a broad range of natural language processing tasks. However, while early models handled routine tasks well, their limitations in complex, high-stakes reasoning—such as mathematical problem-solving and program synthesis—have prompted the development of specialized reasoning-centric LLMs. These newer models are trained on datasets that explicitly target deductive, abductive, and multi-hop reasoning skills, resulting in improved capabilities like structured deliberation and extended inferential chains.

<img src="Final_Year_Project/image_1.png" height="270" width="500">
<img src="Final_Year_Project/image_2.png" width="500">

To further strengthen domain-specific reasoning, fine-tuning procedures are commonly applied to pre-trained LLMs. Two dominant paradigms are SFT and RL. While SFT leverages teacher-model demonstrations to guide learning, RL refines model behavior through iterative reward-based feedback. Despite their effectiveness, most prior research has focused on full-parameter fine-tuning, leaving open questions about their performance and interplay under PEFT settings—such as with LoRA. How to apply an efficient Fine-tuning among two stages, and how to apply the two stages for different training datasets, that are the problems highlighted.



## 🎯 2. Objective(s) and Key Contributions
We conduct a systematic empirical study of SFT and RL under the PEFT regime, focusing on reasoning-centric tasks. Our contributions include:
-   A comparative analysis of SFT and RL in PEFT settings across varying task types and difficulties.
-   Evidence that SFT benefits significantly from larger datasets, while RL is more influenced by reward structure than data scale.
-   A novel Hybrid Fine-Tuning Strategy that partitions training data by task characteristics, applies SFT and RL accordingly, and merges LoRA modules to yield improved reasoning performance.

This work provides actionable insights for researchers and practitioners seeking to maximize reasoning capabilities of LLMs through efficient and scalable fine-tuning pipelines.

## 🔧 3. Required Skills
-   Proficient in using Hugging Face transformers, datasets, and peft libraries for LoRA-based fine-tuning and model deployment.
-   Experienced with both SFT and RL strategies, including GRPO-based techniques.
-   Strong understanding of PEFT techniques, especially LoRA, including module merging and hybrid tuning.
-   Capable of designing reasoning-oriented experiments and evaluating models using benchmarks such as GSM8K, MATH, and MBPP.
-   Skilled in training automation, multi-GPU deployment, and performance monitoring using tools like shell scripting, wandb, or TensorBoard.
-   Experienced in evaluating LLMs using metrics like accuracy, chain-of-thought consistency, reward alignment, and step-level correctness.


## 👥 4. Number of Students
1

## 📚 5. References
[1] Hu, E. J.; Shen, Y.; Wallis, P.; Allen-Zhu, Z.; Li, Y.; Wang, S.; Wang, L.; and Chen, W. 2021. LoRA: Low-Rank Adap-tation of Large Language Models. arXiv:2106.09685.

[2] Li, X.; Zou, H.; and Liu, P. 2025. LIMR: Less is More for RL Scaling. arXiv:2502.11886.

[3] Luong, T. Q.; Zhang, X.; Jie, Z.; Sun, P.; Jin, X.; and Li, H. 2024. ReFT: Reasoning with Reinforced Fine-Tuning. arXiv:2401.08967.

[4] Ma, L.; Liang, H.; Qiang, M.; Tang, L.; Ma, X.; Wong,
Z. H.; Niu, J.; Shen, C.; He, R.; Cui, B.; and Zhang,
W. 2025. Learning What Reinforcement Learning Can’t:
Interleaved Online Fine-Tuning for Hardest Questions.
arXiv:2506.07527.

[5] Muennighoff, N.; Yang, Z.; Shi, W.; Li, X. L.; Fei-Fei,
L.; Hajishirzi, H.; Zettlemoyer, L.; Liang, P.; Cand`es, E.; and Hashimoto, T. 2025. s1: Simple test-time scaling. arXiv:2501.19393.
