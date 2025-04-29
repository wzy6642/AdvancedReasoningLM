<!--
 * @Author: Zhenyu Wu
 * @Date: 2025-04-29 08:41:02
 * @LastEditTime: 2025-04-29 17:17:37
-->
# AdvancedReasoningLM
A curated collection of research papers on complex reasoning with language models.

## Benchmark
 - **[OlymMATH]:** Challenging the Boundaries of Reasoning: An Olympiad-Level Math Benchmark for Large Language Models. [Paper](http://arxiv.org/abs/2503.21380), [Code](https://github.com/RUCAIBox/Slow_Thinking_with_LLMs)<br>
    <span style="color:#90EE90;">**TLDR:**</span> <br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` 


## Methodology
 - **[Tina]:** Tina: Tiny Reasoning Models via LoRA. [Paper](http://arxiv.org/abs/2504.15777), [Code](https://github.com/shangshang-wang/Tina)<br>
    <span style="color:#FFC0CB;">**TLDR:**</span> LoRA excels at quickly learning the structural/format requirements of multi-step reasoning (e.g., step-by-step chains) while largely preserving the base model’s world knowledge—enabling “less compute, more performance”. <br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `LoRA` `Reinforcement Learning` `DeepSeek-R1-Distill-Qwen-1.5B` `Mathematical Reasoning` `Scientific Reasoning` `GRPO`

 - **[SRPO]:** SRPO: A Cross-Domain Implementation of Large-Scale Reinforcement Learning on LLM. [Paper](http://arxiv.org/abs/2504.14286), [Code](https://huggingface.co/Kwaipilot/SRPO-Qwen-32B)<br>
    <span style="color:#90EE90;">**TLDR:**</span> The approach includes a two-stage training paradigm, where the first stage focuses on mathematical data to develop reasoning skills, and the second integrates coding data to build proficiency in procedural thinking. Key innovations include the introduction of History Resampling (HR), which improves training efficiency by filtering out “easy” samples and maintaining meaningful gradients. <br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `Qwen-2.5-32B-Base` `Mathematical Reasoning` `Code Generation` `Reinforcement Learning` `GRPO`


## Analysis
 - **[Open-RS]:** Reinforcement Learning for Reasoning in Small LLMs: What Works and What Doesn't. [Paper](https://arxiv.org/pdf/2503.16219), [Code](https://github.com/knoveleng/open-rs)<br>
    <span style="color:#90EE90;">**TLDR:**</span> Small language models can efficiently improve their reasoning skills through reinforcement learning using minimal data and computational resources, with training stabilized by a mix of easy and hard problems and output length managed by cosine rewards, though complex tasks may require longer context limits.<br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `Reinforcement Learning` `DeepSeek-R1-Distill-Qwen-1.5B` `Mathematical Reasoning` `GRPO`

 - **[Limit-of-RLVR]:** Does Reinforcement Learning Really Incentivize Reasoning Capacity in LLMs Beyond the Base Model? [Paper](http://arxiv.org/abs/2504.13837), [Code](https://limit-of-rlvr.github.io/)<br>
    <span style="color:#FFC0CB;">**TLDR:**</span> The study questions whether Reinforcement Learning with Verifiable Rewards (RLVR) enhances LLM reasoning beyond base models. It finds RLVR boosts initial performance but restricts exploration, limiting its ability to surpass base models at larger sampling sizes. Distillation from stronger models proves more effective in expanding reasoning boundaries. Thus, RLVR falls short in significantly advancing LLM reasoning capabilities compared to alternative training approaches.<br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `Reinforcement Learning` `Qwen2.5-7B` `Mathematical Reasoning` `GRPO` `Code Generation` `Visual Reasoning`


## Foundation Models
 - **[Qwen3]:** Qwen3: Think Deeper, Act Faster. [Blog](https://qwenlm.github.io/blog/qwen3/), [Code](https://github.com/QwenLM/Qwen3)<br>
    <span style="color:#FFC0CB;">**TLDR:**</span> To develop a hybrid model adept at both detailed reasoning and quick responses, the team executed a four-stage training pipeline: (1) they initiated training via a long chain-of-thought (CoT) cold-start phase, fine-tuning the model with diverse reasoning data across math, coding, and logic; (2) next, they conducted reasoning-based reinforcement learning (RL) to refine the model's exploration and problem-solving abilities; (3) subsequently, they fused rapid-response capabilities into the model by fine-tuning it with combined CoT and standard instruction-tuning data; and (4) finally, general RL was applied across a wide range of real-world tasks to enhance the model’s overall performance, ensuring reliability and mitigating undesirable behaviors.<br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `Reinforcement Learning` `Qwen3` `Thinking Mode`
 


## Metrics
 - **pass@k:** Given a problem, we sample k outputs from the model. The pass@k value for this question is 1 if at least one of the k samples passes verification; otherwise, it is 0.
  - **perplexity:** Given a model $m$, a problem $x$, and a response $\mathbf{Y}=(y_1,\ldots,y_T)$, the perplexity is defined as the exponentiated average negative log-likelihood of a sequence: <br>
$\mathrm{PPL}\_m(\mathbf{Y}|x)=\exp\left(-\frac{1}{T}\sum_{t=1}^T\log P(y_t|x,y_1,\ldots,y_{t-1})\right)$ <br>
  which reflects the model’s ability to predict the given response $\mathbf{Y}$ conditioned on the prompt $x$. Lower perplexity indicates that the model has a higher likelihood of generating this response.
