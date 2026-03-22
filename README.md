# Awesome Generalized Additive Models (GAMs) [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of papers, libraries, tutorials, and resources for Generalized Additive Models (GAMs) — from classical statistics to neural network-based interpretable ML.

GAMs model a response variable as the sum of smooth functions of individual features:
**g(E[y]) = β₀ + f₁(x₁) + f₂(x₂) + ... + fₚ(xₚ)**
This additive structure makes each feature's effect independently interpretable, bridging the gap between accuracy and explainability.

---

## Contents

- [Foundational Works](#foundational-works)
- [Modern Neural GAM Variants](#modern-neural-gam-variants)
  - [EBM / InterpretML](#ebm--interpretml)
  - [Neural Additive Models (NAM)](#neural-additive-models-nam)
  - [NODE-GAM](#node-gam)
  - [GAMI-Net](#gami-net)
  - [ExNN](#exnn--explainable-neural-networks)
  - [NBM & SPAM](#nbm--spam)
  - [IGANN](#igann)
  - [Other Neural GAM Variants](#other-neural-gam-variants)
- [Interaction Detection & Editing](#interaction-detection--editing)
- [Software Libraries](#software-libraries)
  - [Python](#python)
  - [R](#r)
- [Surveys & Benchmarks](#surveys--benchmarks)
- [Tutorials & Courses](#tutorials--courses)
- [Applications](#applications)
  - [Healthcare](#healthcare)
  - [Environmental Science & Ecology](#environmental-science--ecology)
  - [Finance & Credit Scoring](#finance--credit-scoring)
- [Interpretability & XAI](#interpretability--xai)

---

## Foundational Works

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 1986 | **Generalized Additive Models** | Trevor Hastie, Robert Tibshirani | *Statistical Science*, 1(3), 297–318 | [Paper](https://projecteuclid.org/journals/statistical-science/volume-1/issue-3/Generalized-Additive-Models/10.1214/ss/1177013604.full) · [PDF](https://hastie.su.domains/Papers/gam.pdf) |
| 1990 | **Generalized Additive Models** (Book) | T.J. Hastie, R.J. Tibshirani | Chapman & Hall/CRC | [Book](https://www.routledge.com/Generalized-Additive-Models/Hastie-Tibshirani/p/book/9780412343902) |
| 2009 | **The Elements of Statistical Learning** (2nd ed.) — Ch. 9: Additive Models | Trevor Hastie, Robert Tibshirani, Jerome Friedman | Springer | [Book](https://link.springer.com/book/10.1007/978-0-387-84858-7) · [Free PDF](https://hastie.su.domains/ElemStatLearn/) |
| 2017 | **Generalized Additive Models: An Introduction with R** (2nd ed.) | Simon N. Wood | Chapman & Hall/CRC | [Book](https://www.routledge.com/Generalized-Additive-Models-An-Introduction-with-R-Second-Edition/Wood/p/book/9781498728331) |

---

## Modern Neural GAM Variants

### EBM / InterpretML

The **Explainable Boosting Machine (EBM)** is a GA²M (GAM with pairwise interactions) trained via cyclic gradient boosting. Developed at Microsoft Research, it is widely regarded as the state-of-the-art glass-box model.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2012 | **Intelligible Models for Classification and Regression** | Yin Lou, Rich Caruana, Johannes Gehrke | KDD 2012 | [ACM](https://dl.acm.org/doi/10.1145/2339530.2339556) · [PDF](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd12.pdf) |
| 2013 | **Accurate Intelligible Models with Pairwise Interactions** | Yin Lou, Rich Caruana, Johannes Gehrke, Giles Hooker | KDD 2013 | [ACM](https://dl.acm.org/doi/10.1145/2487575.2487579) · [PDF](https://www.cs.cornell.edu/~yinlou/papers/lou-kdd13.pdf) |
| 2015 | **Intelligible Models for HealthCare: Predicting Pneumonia Risk and Hospital 30-day Readmission** | Rich Caruana, Yin Lou, Johannes Gehrke, Paul Koch, Marc Sturm, Noemie Elhadad | KDD 2015 | [ACM](https://dl.acm.org/doi/10.1145/2783258.2788613) |
| 2019 | **InterpretML: A Unified Framework for Machine Learning Interpretability** | Harsha Nori, Samuel Jenkins, Paul Koch, Rich Caruana | arXiv | [arXiv:1909.09223](https://arxiv.org/abs/1909.09223) · [GitHub](https://github.com/interpretml/interpret) |

### Neural Additive Models (NAM)

**NAM** uses individual neural networks per feature, trained jointly, to learn each shape function. Proposed by Google Brain with Geoffrey Hinton as co-author.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2021 | **Neural Additive Models: Interpretable Machine Learning with Neural Nets** | Rishabh Agarwal, Levi Melnick, Nicholas Frosst, Xuezhou Zhang, Ben Lengerich, Rich Caruana, Geoffrey E. Hinton | NeurIPS 2021 | [arXiv:2004.13912](https://arxiv.org/abs/2004.13912) · [GitHub](https://github.com/AmrMKayid/nam) |

### NODE-GAM

**NODE-GAM** combines Neural Oblivious Decision Ensembles (NODE) with the GAM framework for better tabular data performance.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2022 | **NODE-GAM: Neural Generalized Additive Model for Interpretable Deep Learning** | Chun-Hao Chang, Rich Caruana, Anna Goldenberg | ICLR 2022 | [arXiv:2106.01613](https://arxiv.org/abs/2106.01613) · [OpenReview](https://openreview.net/forum?id=g8NJR6fCCl8) |

### GAMI-Net

**GAMI-Net** extends neural GAMs with structured pairwise interaction detection using heredity constraints.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2021 | **GAMI-Net: An Explainable Neural Network based on Generalized Additive Models with Structured Interactions** | Zebin Yang, Aijun Zhang, Agus Sudjianto | *Pattern Recognition*, 120, 108192 | [arXiv:2003.07132](https://arxiv.org/abs/2003.07132) · [GitHub](https://github.com/SelfExplainML/GamiNet) |

### ExNN — Explainable Neural Networks

**ExNN** bridges neural networks and additive index models for interpretability.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2018 | **Explainable Neural Networks based on Additive Index Models** | Joel Vaughan, Agus Sudjianto, Erind Brahimi, Jie Chen, Vijayan N. Nair | arXiv | [arXiv:1806.01933](https://arxiv.org/abs/1806.01933) · [GitHub](https://github.com/SelfExplainML/ExNN) |

### NBM & SPAM

**Neural Basis Models (NBM)** learn shared basis functions across features. **SPAM** uses polynomial splines for scalable interpretable models. Both from Meta AI.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2022 | **Neural Basis Models for Interpretability** | Filip Radenovic, Abhimanyu Dubey, Dhruv Mahajan | NeurIPS 2022 | [arXiv:2205.14120](https://arxiv.org/abs/2205.14120) · [GitHub](https://github.com/facebookresearch/nbm-spam) |
| 2022 | **Scalable Interpretability via Polynomials** (SPAM) | Abhimanyu Dubey, Filip Radenovic, Dhruv Mahajan | NeurIPS 2022 | [arXiv:2205.14108](https://arxiv.org/abs/2205.14108) · [GitHub](https://github.com/facebookresearch/nbm-spam) |

### IGANN

**IGANN** uses small neural networks with weight constraints for interpretable additive models.

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2024 | **Interpretable Generalized Additive Neural Networks** | Mathias Kraus, Daniel Tschernutter, Sven Weinzierl, Patrick Zschech | *European Journal of Operational Research*, 317(2), 303–316 | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0377221723005027) |

### Other Neural GAM Variants

| Year | Title | Venue | Links |
|------|-------|-------|-------|
| 2020 | **Adaptive Explainable Neural Networks (AxNN)** | arXiv | [arXiv:2004.02353](https://arxiv.org/abs/2004.02353) |
| 2022 | **Sparse Neural Additive Model (SNAM): Interpretable Deep Learning with Feature Selection via Group Sparsity** | arXiv / ICLR 2022 Workshop | [arXiv:2202.12482](https://arxiv.org/abs/2202.12482) |
| 2022 | **Sparse Interaction Additive Networks (SIAN) via Feature Interaction Detection and Sparse Selection** | NeurIPS 2022 | [arXiv:2209.09326](https://arxiv.org/abs/2209.09326) · [GitHub](https://github.com/EnouenJ/sparse-interaction-additive-networks) |
| 2022 | **Higher-Order Neural Additive Models (HONAM): An Interpretable Machine Learning Model with Feature Interactions** | arXiv | [arXiv:2209.15409](https://arxiv.org/abs/2209.15409) · [GitHub](https://github.com/gim4855744/HONAM) |
| 2022 | **Monotonic Neural Additive Models: Pursuing Regulated Machine Learning Models for Credit Scoring** | ICAIF 2022 | [arXiv:2209.10070](https://arxiv.org/abs/2209.10070) |
| 2024 | **Improving Neural Additive Models with Bayesian Principles** (LA-NAM) | ICML 2024 | [arXiv:2305.16905](https://arxiv.org/abs/2305.16905) |
| 2024 | **Gaussian Process Neural Additive Models** (GP-NAM) | AAAI 2024 | [arXiv:2402.12518](https://arxiv.org/abs/2402.12518) · [GitHub](https://github.com/Wei2624/GPNAM) |
| 2024 | **GAMformer: In-Context Learning for Generalized Additive Models** | arXiv | [arXiv:2410.04560](https://arxiv.org/abs/2410.04560) |

---

## Interaction Detection & Editing

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2013 | **Accurate Intelligible Models with Pairwise Interactions** (GA²M) | Yin Lou et al. | KDD 2013 | [ACM](https://dl.acm.org/doi/10.1145/2487575.2487579) |
| 2022 | **Interpretability, Then What? Editing Machine Learning Models to Reflect Human Knowledge and Values** (GAM Changer) | Zijie J. Wang, Alex Kale, Harsha Nori et al. | KDD 2022 | [arXiv:2112.03245](https://arxiv.org/abs/2112.03245) · [Demo](https://interpret.ml/gam-changer) |

---

## Software Libraries

### Python

| Library | Description | Links |
|---------|-------------|-------|
| **InterpretML** | Microsoft's EBM (Explainable Boosting Machine) — state-of-the-art GA²M. Glass-box and black-box explainability. | [GitHub](https://github.com/interpretml/interpret) · [Docs](https://interpret.ml/) |
| **pyGAM** | Penalized B-spline GAMs with scikit-learn-compatible API. Supports LogisticGAM, LinearGAM, PoissonGAM, etc. | [GitHub](https://github.com/dswah/pyGAM) · [Docs](https://pygam.readthedocs.io/) |
| **statsmodels** | `GLMGam` class with penalized B-splines, inheriting from GLM. | [Docs](https://www.statsmodels.org/stable/gam.html) |
| **PiML Toolbox** | Interpretable ML toolbox supporting GAM, GAMI-Net, EBM, XGB1/XGB2 and more. | [GitHub](https://github.com/SelfExplainML/PiML-Toolbox) · [Paper](https://arxiv.org/abs/2305.04214) |
| **gaminet** | Python implementation of GAMI-Net with pairwise interactions. | [GitHub](https://github.com/ZebinYang/gaminet) |
| **gammy** | Bayesian GAMs in Python. | [GitHub](https://github.com/malmgrek/gammy) |
| **generalized-additive-models** | Pure Python GAM implementation emphasizing interpretability. | [GitHub](https://github.com/tommyod/generalized-additive-models) |

### R

| Package | Description | Links |
|---------|-------------|-------|
| **mgcv** | The de facto standard for GAMs in R. Mixed GAM Computation Vehicle with automatic smoothness estimation via REML/GCV. | [CRAN](https://cran.r-project.org/web/packages/mgcv/index.html) |
| **gam** | Original implementation following Hastie & Tibshirani (1990), using local scoring and backfitting. | [CRAN](https://cran.r-project.org/web/packages/gam/) |
| **gamm4** | Generalized Additive Mixed Models combining mgcv with lme4. More numerically robust than `gamm()`. | [CRAN](https://cran.r-project.org/web/packages/gamm4/index.html) |
| **gratia** | ggplot2-based visualization and tidy helper functions for mgcv GAMs. Named after Grace Wahba. | [CRAN](https://cran.r-project.org/web/packages/gratia/) · [Website](https://gavinsimpson.github.io/gratia/) |
| **mvgam** | Dynamic Bayesian GAMs for multivariate time series forecasting. | [GitHub](https://github.com/nicholasjclark/mvgam) |
| **neuralGAM** | Neural Additive Models (NAM-style) in R with backfitting algorithm. | [CRAN](https://cran.r-project.org/package=neuralGAM) · [Paper](https://arxiv.org/abs/2505.08610) |

---

## Surveys & Benchmarks

| Year | Title | Authors | Venue | Links |
|------|-------|---------|-------|-------|
| 2023 | **Interpretable and Explainable Machine Learning: A Methods-Centric Overview** | Raphael Marcinkevics, Julia E. Vogt | *WIREs Data Mining and Knowledge Discovery* | [Wiley](https://wires.onlinelibrary.wiley.com/doi/full/10.1002/widm.1493) |
| 2025 | **Challenging the Performance-Interpretability Trade-Off: An Evaluation of Interpretable Machine Learning Models** | Sven Kruschel, Nico Hambauer et al. | *Business & Information Systems Engineering* | [Springer](https://link.springer.com/article/10.1007/s12599-024-00922-2) · [arXiv:2409.14429](https://arxiv.org/abs/2409.14429) |

> **Key finding (Kruschel et al. 2025):** Compared 7 GAM variants (P-Splines, TP-Splines, EBM, NAM, GAMI-Net, ExNN, IGANN) against 7 black-box baselines across 20 datasets. GAMs achieved comparable accuracy, challenging the traditional performance-interpretability trade-off.

---

## Tutorials & Courses

| Resource | Author(s) | Links |
|----------|-----------|-------|
| **Generalized Additive Models in R** (Free Interactive Course) | Noam Ross, David Miller, Gavin Simpson, Eric Pedersen | [Course](https://noamross.github.io/gams-in-r-course/) |
| **GAM Resources** (Curated List) | Noam Ross | [GitHub](https://github.com/noamross/gam-resources) |
| **Physalia GAM Course** | Gavin L. Simpson | [GitHub](https://github.com/gavinsimpson/physalia-gam-course) |
| **Generalized Additive Models** (Online Guide) | Michael Clark | [Website](https://m-clark.github.io/generalized-additive-models/) |
| **Hierarchical GAMs in Ecology: An Introduction with mgcv** | Eric Pedersen, David Miller, Gavin Simpson, Noam Ross | [PeerJ (2019)](https://peerj.com/articles/6876/) · [GitHub](https://github.com/eric-pedersen/mixed-effect-gams) |
| **gratia: An R Package for Exploring GAMs** | Gavin L. Simpson | [JOSS (2024)](https://doi.org/10.21105/joss.06962) |

---

## Applications

### Healthcare

| Year | Title | Links |
|------|-------|-------|
| 1995 | **Generalized Additive Models for Medical Research** | [PubMed](https://pubmed.ncbi.nlm.nih.gov/8548102/) |
| 2015 | **Intelligible Models for HealthCare: Predicting Pneumonia Risk and Hospital 30-day Readmission** (Caruana et al.) | [ACM](https://dl.acm.org/doi/10.1145/2783258.2788613) |
| 2020 | **A Factored Generalized Additive Model for Clinical Decision Support in the Operating Room** | [arXiv:1907.12596](https://arxiv.org/abs/1907.12596) · [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC7153157/) |
| 2022 | **Interpretable Generalized Neural Additive Models for COVID-19 Mortality Prediction** | [PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9803600/) |

### Environmental Science & Ecology

| Year | Title | Venue | Links |
|------|-------|-------|-------|
| 2002 | **On the Use of Generalized Additive Models in Time-Series Studies of Air Pollution and Health** | *American Journal of Epidemiology*, 156(3) | [Oxford](https://academic.oup.com/aje/article-abstract/156/3/193/71628) |
| 2009 | **Application of a GAM to Reveal Relationships Between Environmental Factors and Distributions of Pelagic Fish and Krill** | *ICES Journal of Marine Science*, 66(6) | [Oxford](https://academic.oup.com/icesjms/article/66/6/1417/695432) |
| 2013 | **GAMs Used to Predict Species Abundance in the Gulf of Mexico** | *PLOS ONE* | [Paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0064458) |
| 2019 | **Hierarchical GAMs in Ecology: An Introduction with mgcv** | *PeerJ* | [Paper](https://peerj.com/articles/6876/) |
| 2019 | **Generalized Additive Models to Investigate Air Pollution, Climate Change, and Human Health** | *Environment International* | [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S0160412019309341) |

### Finance & Credit Scoring

| Year | Title | Links |
|------|-------|-------|
| 2018 | **Transparent GAM Trees (TGAMT) for Credit Scorecards** (FICO) | [PDF](https://www.philadelphiafed.org/-/media/frbp/assets/events/2018/consumer-finance/fintech-2018/day-1/session_3_paper_3_fico_paper_gerald_fahner.pdf) |
| 2022 | **Monotonic Neural Additive Models: Pursuing Regulated ML Models for Credit Scoring** | [arXiv:2209.10070](https://arxiv.org/abs/2209.10070) |

---

## Interpretability & XAI

GAMs occupy a unique position in the interpretable ML landscape — they are inherently glass-box models where each feature's contribution is a visualizable shape function, yet modern variants achieve accuracy competitive with black-box models.

**Key connections:**

- **Glass-box vs. post-hoc:** Unlike LIME or SHAP which explain black-box models after the fact, GAMs are inherently interpretable — the shape functions *are* the model.
- **Human-in-the-loop:** GAM Changer (Wang et al., 2022) demonstrates that GAM interpretability enables direct model editing by domain experts.
- **Regulatory compliance:** Monotonic NAMs and FICO's TGAMT show how GAMs meet financial regulatory requirements for model transparency.
- **Healthcare safety:** Caruana et al. (2015) showed that an EBM revealed a dangerous learned pattern (asthma → lower pneumonia risk) that black-box models silently exploited — a landmark case for interpretable ML.

**Related frameworks:**

| Tool | Description | Links |
|------|-------------|-------|
| **InterpretML** | Unifies glass-box models (EBM) with post-hoc explainers (SHAP, LIME, PDP) | [GitHub](https://github.com/interpretml/interpret) |
| **PiML** | End-to-end interpretable ML pipeline with multiple GAM variants | [GitHub](https://github.com/SelfExplainML/PiML-Toolbox) |
| **GAM Changer** | Interactive visualization tool for editing GAM shape functions | [Demo](https://interpret.ml/gam-changer) |

---

## Model Taxonomy

```
GAM Family
├── Classical / Statistical
│   ├── Spline-based (mgcv, pyGAM)
│   ├── Local regression (LOESS-based, original gam package)
│   └── Bayesian (gammy, mvgam)
│
├── Boosted
│   ├── EBM / GA²M (InterpretML)
│   └── NODE-GAM (oblivious decision ensembles)
│
├── Neural Network-based
│   ├── NAM (one network per feature)
│   ├── GAMI-Net (with structured interactions)
│   ├── ExNN (additive index models)
│   ├── NBM (shared basis functions)
│   ├── IGANN (weight-constrained networks)
│   ├── SNAM (sparse feature selection)
│   ├── HONAM (higher-order interactions)
│   ├── LA-NAM (Bayesian / Laplace approximation)
│   ├── GP-NAM (Gaussian process-based)
│   └── GAMformer (in-context learning)
│
├── Polynomial
│   └── SPAM (scalable polynomial features)
│
└── Hybrid / Specialized
    ├── AxNN (adaptive explainable)
    ├── Monotonic NAM (with monotonicity constraints)
    ├── SIAN (sparse interaction detection)
    └── F-GAM (factored for clinical use)
```

---

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to suggest additions.

---

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

This list is released into the public domain under CC0 1.0.
