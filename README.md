# Saqib Ali Khan

**BSc Artificial Intelligence @ JKU Linz**

I work on computer vision and applied machine learning. The thread running through
most of what I build is checking whether a result means what it appears to mean:
whether a model generalises or memorises, whether a correlation is real or an
artefact of two series trending together, whether a finding survives the noise in
its own experiment.

---

## Selected Work

### 🔬 Born in Simulation
**How much visual diversity does sim-to-real transfer actually need?**

Six ResNet-18 classifiers trained entirely on synthetic PyBullet renders of YCB
objects, evaluated on 3,000 real photographs never seen during training.

* Reached 61.3% real-world accuracy with zero real training images, up from a
  below-chance baseline that had learned a background shortcut
* Grad-CAM showed the mechanism: randomization moves the model's attention off the
  background and onto object geometry
* Ablation without ImageNet pretraining located the data-scale boundary where
  diversity alone stops being enough
* Found and documented a seed-collision bug that had silently produced identical
  training data across three conditions in the first run
* A control comparison afterwards showed the curve's shape is not separable from
  run-to-run variance, which is reported openly rather than quietly dropped
* Written up as a short research paper (ACM format, included in the repo)

**Stack:** Python · PyTorch · PyBullet · Grad-CAM

[View project →](https://github.com/saqib00987/sim2real-domain-randomization)

### 🛰️ EuroSAT Classifier
**Satellite land-use classification, built from scratch**

A VGG-style CNN trained with no pretrained weights, classifying Sentinel-2 tiles into
10 land-use classes, deployed as a web app for live predictions.

* 96.7% validation accuracy and 96% on the held-out test set, with a train-validation
  gap of ~1.4%, so the model generalises rather than memorises
* Full pipeline: stratified reproducible splits, augmentation, LR scheduling, early
  stopping, best-model checkpointing
* Per-channel normalisation computed by streaming over the training set, and reused
  at inference so uploads are normalised identically to training
* Errors cluster where overhead imagery is genuinely ambiguous: the vegetation classes
  trade misclassifications, while Forest is near-perfect
* Shiny app: upload a tile, get the predicted class and full probability distribution

**Stack:** Python · PyTorch · torchvision · scikit-learn · Shiny

[View project →](https://github.com/saqib00987/eurosat-classifier)

### 📈 US Macro Indicators
**How Fed rate changes transmit through the economy, and how long it takes**

Eight US macroeconomic series from FRED, 2000 to 2026, analysed with programmatic
event detection rather than hand-marked dates.

* Rate peaks lead unemployment peaks by 32 to 35 months, confirmed across both
  completed cycles; transmission is far faster post-COVID (+0.44 at lag 6, against
  +0.24 only at lag 36 pre-2008)
* Every economic-cycle recession in the window was preceded by a yield-curve
  inversion, with COVID the sole exception as an external shock
* Correlations computed on month-over-month changes rather than levels, so two
  trending series don't correlate for no reason
* Missing data hatched as unavailable rather than backfilled, and the one marginal
  sentiment result (p = 0.045) reported as suggestive rather than firm

**Stack:** Python · pandas · Matplotlib · Plotly · SciPy · FRED API

[View project →](https://github.com/saqib00987/us-macro-indicators-viz)

---

## Currently

* Practical project in Physical AI at JKU
* Reinforcement learning and formal methods coursework
* Looking for internships and working-student roles in AI, ML and data science

[LinkedIn](https://www.linkedin.com/in/saqib-ali-khan-07bb51279/) · saaqikhan00987@gmail.com
