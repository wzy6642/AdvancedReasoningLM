<!--
 * @Author: Zhenyu Wu
 * @Date: 2025-04-29 08:41:02
 * @LastEditTime: 2025-04-29 15:39:46
-->
# AdvancedReasoningLM
A curated collection of research papers on complex reasoning with language models.

## Benchmark

## Methodology
 - **[Tina]:** Tina: Tiny Reasoning Models via LoRA. [Paper](http://arxiv.org/abs/2504.15777), [Code](https://github.com/shangshang-wang/Tina)<br>
    <span style="color:#FFC0CB;">**TLDR:**</span> LoRA excels at quickly learning the structural/format requirements of multi-step reasoning (e.g., step-by-step chains) while largely preserving the base model’s world knowledge—enabling “less compute, more performance”. <br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `LoRA` `Reinforcement Learning` `DeepSeek-R1-Distill-Qwen-1.5B` `Mathematical Reasoning` `Scientific Reasoning` `GRPO`

## Analysis
 - **[Open-RS]:** Reinforcement Learning for Reasoning in Small LLMs: What Works and What Doesn't. [Paper](https://arxiv.org/pdf/2503.16219), [Code](https://github.com/knoveleng/open-rs)<br>
    <span style="color:#90EE90;">**TLDR:**</span> Small language models can efficiently improve their reasoning skills through reinforcement learning using minimal data and computational resources, with training stabilized by a mix of easy and hard problems and output length managed by cosine rewards, though complex tasks may require longer context limits.<br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `Reinforcement Learning` `DeepSeek-R1-Distill-Qwen-1.5B` `Mathematical Reasoning` `GRPO`

 - **[Limit-of-RLVR]:** Does Reinforcement Learning Really Incentivize Reasoning Capacity in LLMs Beyond the Base Model? [Paper](http://arxiv.org/abs/2504.13837), [Code](https://limit-of-rlvr.github.io/)<br>
    <span style="color:#FFC0CB;">**TLDR:**</span> <br>
    <span style="color:#90EE90;">**Keywords:**</span> `2025` `arXiv` `Reinforcement Learning` `Qwen2.5-7B` `Mathematical Reasoning` `GRPO` `Code Generation` `Visual Reasoning`

## Foundation Models

## Metrics
 - **pass@k:** Given a problem, we sample k outputs from the model. The pass@k value for this question is 1 if at least one of the k samples passes verification; otherwise, it is 0.
  - **perplexity:** Given a model $m$, a problem $x$, and a response $\mathbf{Y}=(y_1,\ldots,y_T)$, the perplexity is defined as the exponentiated average negative log-likelihood of a sequence: <br>
$\mathrm{PPL}\_m(\mathbf{Y}|x)=\exp\left(-\frac{1}{T}\sum_{t=1}^T\log P(y_t|x,y_1,\ldots,y_{t-1})\right)$ <br>
  which reflects the model’s ability to predict the given response $\mathbf{Y}$ conditioned on the prompt $x$. Lower perplexity indicates that the model has a higher likelihood of generating this response.
