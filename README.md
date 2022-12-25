**Presentation**
This repository contains a report on the 3 papers present in the [papers](papers) folder.

---

## IS REINFORCEMENT LEARNING (NOT) FOR NATURAL LANGUAGE PROCESSING?: BENCHMARKS, BASELINES, AND BUILDING BLOCKS FOR NATURAL LANGUAGE POLICY OPTIMIZATION

#### Problem :
- Aligning pre-trained large language models with human preferences.
- RL training instability.
- Open source tools for RL in NLP.
  

#### Libraries and tools :
- [RL4LMs](https://github.com/allenai/RL4LMs) : Optimizing Encoder or Encoder/Decoder models with RL (HuggingFace compatible).
- [GRUE](https://rl4lms.apps.allenai.org/grue) : General Reinforced-language Understanding Evaluation, a benchmark based reward functions to capture automated measures of human preference. 
- [NLPO](https://rl4lms.apps.allenai.org/algorithms) : Natural Language Policy Optimization. RL algorithms that achieved better results in comparison to the [PPO](https://openai.com/blog/openai-baselines-ppo/) algorithm in the paper's experimentations.