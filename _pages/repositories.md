---
layout: page
permalink: /repositories/
title: repositories
description: Code accompanying my papers.
nav: true
nav_order: 4
---

### KV Cache Compression Through the Lens of Transform Coding

Code for our paper [KV Cache Compression Through the Lens of Transform Coding](https://arxiv.org/abs/2608.14191).
It contains the implementation of Attention-Aware Transform Coding (AATC) together with the scripts to reproduce the experiments.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo.liquid repository="HannahLaus/aatc-kv-cache-transform-coding" %}
</div>

### Imaging with Confidence: Uncertainty Quantification for High-Dimensional Undersampled MR Images

Code for our paper [Imaging with Confidence](https://link.springer.com/chapter/10.1007/978-3-031-73229-4_25).
It implements the debiased total-variation estimator and the confidence-interval construction for undersampled MRI reconstruction.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo.liquid repository="HannahLaus/Project_UQ_TV" %}
</div>

### Non-Asymptotic Uncertainty Quantification in High-Dimensional Learning

Code for our NeurIPS 2024 paper [Non-Asymptotic Uncertainty Quantification in High-Dimensional Learning](https://arxiv.org/abs/2407.13666),
maintained by my coauthor Frederik Hoppe. It contains the MRI reconstruction experiments with U-Net and It-Net,
the debiased-estimator confidence intervals, and the model-based sparse regression experiments.

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  {% include repository/repo.liquid repository="frederikhoppe/UQ_high_dim_learning" %}
</div>
