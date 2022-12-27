**Presentation**
This repository contains a report on the 3 papers present in the [papers](papers) folder.

---

## IS REINFORCEMENT LEARNING (NOT) FOR NATURAL LANGUAGE PROCESSING?: BENCHMARKS, BASELINES, AND BUILDING BLOCKS FOR NATURAL LANGUAGE POLICY OPTIMIZATION

#### Problem :
- Aligning pre-trained large language models with human preferences (and Naturalness).
- RL training instability.
- Open source tools for RL in NLP.
  

#### Libraries and tools :
- [RL4LMs](https://github.com/allenai/RL4LMs) : A modular RL library to fine-tune language models to human preferences.
- [GRUE](https://rl4lms.apps.allenai.org/grue) : General Reinforced-language Understanding Evaluation, a benchmark based reward functions to capture automated measures of human preference. 
- [NLPO](https://rl4lms.apps.allenai.org/algorithms) : Natural Language Policy Optimization. RL algorithms that achieved better results in comparison to the [PPO](https://openai.com/blog/openai-baselines-ppo/) algorithm in the paper's experimentations.


#### Methods :
###### Overview

<!-- ![GRUE](assets/grue.gif) -->

![GRUE](assets/grue.jpg)

###### Action space
Masking poilicy $\pi_\psi$ :
$$\begin{equation*}
\pi_\psi\left(\cdot \mid s, \pi_\theta\right)= \begin{cases}\pi_\theta(\cdot \mid s) / Z^p\left(\pi_\theta\right) & \text { if } a \in  \mathcal V_{\pi_\theta}^p \text { and } Z\left(\pi_\theta\right) \\
0 & \text { otherwise. }\end{cases}
\end{equation*}$$

$\mathcal V^p_{\pi_\theta} \subset \mathcal V$ : Top vocabulary ($p\in(0, 1]$ portion of highest proba tokens)

$Z(\pi_\theta) = \sum_{a\in\mathcal V} \pi_{\theta_0}(a|s)$

$Z^p(\pi_\theta) = \sum_{a\in\mathcal V^p_{\pi_\theta}} \pi_{\theta_0}(a|s)$

###### Evaluations

![GRUE taks](assets/grue_tasks.jpg)

#### Results :

![Results](assets/results_nlpo.jpg)


---

## Aligning Generative Language Models with Human Values

#### Problem :
- Aligning pre-trained large language models with human values and ethics.
- Dealing with Out-of-domain human values.

![gpt2_poor](assets/GPT2_poor.jpg)

#### Libraries and tools :
- [BLUE](https://fr.wikipedia.org/wiki/BLEU_(algorithme)) : Used to approximate the human evaluation of the generated text.
- [GPT-2](https://openai.com/blog/tags/gpt-2/) : Pre-trained generative LM.

#### Methods :

###### SENSEI

![SENSEI](assets/sensei.jpg)


#### Results :

![Sensei results](assets/sensei_results.jpg)


---

## Scaling Laws for Reward Model Overoptimization

#### Problem :
- To which extent the reward model can be optimized (no overoptimization) ?
- Scaling laws for reward models.