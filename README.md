# Cognitive Chain-of-Thought (CoCoT): Structured Multimodal Reasoning about Social Situation.
This is the official repository for "Cognitive Chain-of-Thought (CoCoT): Structured Multimodal Reasoning about Social Situations" (COLM 2026).

<p align="center"> <img src="cocot_fi1.png" width="90%"> </p> <p align="center"> <em>CoCoT reasoning on multimodal intent disambiguation. Given a subtle utterance and an image, the task is to infer the speaker's intent in the visual context.</em> </p>

## About

Chain-of-Thought prompting helps models think step by step, but naive CoT breaks down on visually grounded social tasks, where models must perceive, understand, and judge all at once. CoCoT structures vision-language model reasoning through three cognitively motivated stages:

| Stage | Question | Constraint |
|---|---|---|
| `Perception` | What is directly observable? | Concrete visual evidence only; no mental-state language |
| `Situation` | What social script explains it? | Must build on entities established in `Perception` |
| `Norm` | Which interpretation is socially plausible? | Selects against the situation model, not raw perception |

Across multimodal intent disambiguation, theory of mind, social commonsense, and safety instruction following, CoCoT improves consistently over both direct prompting and standard CoT. Supervised fine-tuning on CoCoT-structured traces yields further gains without CoCoT prompting at inference, indicating that models internalize the reasoning structure rather than merely following formatting instructions.
