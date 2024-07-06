---
author: ["Weilun Chen"]
title: "From RLHF to DPO and IPO"
date: "2024-07-04"
description: "How does RLHF works under the hood, and how can we get rid of it? (Or can we?)"
tags: ["machine learning", "LLM", "Reinforcement Learning"]
math: true
ShowToc: true
---

I think by now every one should already understand that the state-of-the-art LLM models are trained with massive human quality feedback. This feedback is either coming from a massive rater pool, or can come from the end users implicitly (sometimes explicitly as well.. remember when ChatGPT presents you 2 responses to choose from?). This [video](https://youtu.be/zjkBMFhNj_g?si=LaoFxRBqdKuKRdJD&t=1262) talks about RLHF very briefly and you can checkout for a refresher. The content below requires you to have a rough understanding of this algorithm.

## RLHF: a recap

We try to optimize for the following objective in RLHF

$$
\begin{aligned}
x + y &= z \\
a + b &= c
\end{aligned}
$$
