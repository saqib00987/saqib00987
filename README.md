# Saqib Ali Khan

**BSc Artificial Intelligence @ JKU Linz · Computer Vision · Applied ML**

I build and evaluate vision systems, and I'm most interested in the gap between
models that work on benchmarks and models that survive contact with real data.

`Computer Vision` · `Deep Learning` · `Sim-to-Real` · `Data Annotation` · `Applied ML`

---

## Selected Work

### 🔬 Born in Simulation
**How much visual diversity does sim-to-real transfer actually need?**

Six ResNet-18 classifiers trained entirely on synthetic PyBullet renders of YCB objects,
evaluated on 3,000 real photographs never seen in training.

* Reached 61.3% real-world accuracy with zero real training images
* Used Grad-CAM to show randomization shifts attention from background to object geometry
* Ablation without ImageNet pretraining locating the data-scale boundary
* Found and documented a seed-collision bug that had silently invalidated the first run
* Wrote the results up as a short research paper (ACM format, included in the repo)

**Stack:** Python · PyTorch · PyBullet · Grad-CAM

[View project →](https://github.com/saqib00987/sim2real-domain-randomization)

### 🛰️ EuroSAT Classifier
**Satellite land-use classification, built from scratch**

A VGG-style CNN trained without any pretrained weights, classifying satellite imagery
into 10 land-use classes, wrapped in a web app for live predictions.

* 96.7% validation accuracy, 96% on the held-out challenge set
* Full training pipeline: AdamW, LR scheduling, early stopping, best-model checkpointing
* Streaming per-channel normalisation computed without loading the dataset into memory
* Shiny web app: upload an image, see the prediction and full probability distribution

**Stack:** Python · PyTorch · torchvision · Shiny

[View project →](https://github.com/saqib00987/eurosat-classifier)

### 📈 US Macro Indicators
**Where do interest rate changes actually show up?**

Analysis and visualization of eight US macroeconomic series from the FRED API, built
around programmatic event detection rather than hand-marked dates.

* Automatic detection of rate peaks, yield-curve inversions and recession periods
* Lagged-correlation heatmaps across three macro regimes
* Significance-tested analysis of consumer sentiment response to economic shocks

**Stack:** Python · pandas · Matplotlib · Plotly · FRED API

[View project →](https://github.com/saqib00987/us-macro-indicators-viz)

---

## Focus

Computer Vision → CNNs, transfer learning, Grad-CAM, sim-to-real
Applied ML → experiment design, ablations, error analysis, evaluation
Data → annotation, inter-annotator agreement, dataset construction
Foundations → reinforcement learning, sequence models, algorithms


## Currently

* Practical project in Physical AI at JKU
* Reinforcement learning and formal methods coursework
* Looking for internships and working-student roles in AI/ML and Data science.

---

*Train it, break it, find out why.*

[LinkedIn](https://www.linkedin.com/in/saqib-ali-khan-07bb51279/)
