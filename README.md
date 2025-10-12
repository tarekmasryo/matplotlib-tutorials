# 📈 Matplotlib — Beginner-to-Pro 🎯

[![Python](https://img.shields.io/badge/Python-3.10–3.12-blue.svg)](#-requirements)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%E2%89%A53.8-11557c.svg)](#-requirements)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#-license)
[![Open in Colab](https://img.shields.io/badge/Colab-Open-brightgreen.svg)](https://colab.research.google.com/github/tarekmasryo/Matplotlib-Beginner-to-Pro/blob/main/matplotlib-beginner-to-pro.ipynb)
[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20beff.svg)](https://kaggle.com/code/tarekmasryo/matplotlib-beginner-to-pro)

A practical, opinionated reference for **Exploratory Data Analysis (EDA) with Matplotlib**.  
We start from **beginner basics** → **intermediate customization** → **advanced patterns**, and finish with a **compact, Kaggle-ready EDA pipeline**.

---

## 🚀 Why this notebook?
- Clean, modular examples you can drop into real projects.  
- Short cells + clear plots = easy to follow.  
- Covers both *when to use what* and hands-on code.  
- Ends with a reusable **Mini EDA pipeline** (Iris).  
- Performance-minded tips: **hexbin**, **rasterized scatter**, **LineCollection**.  
- Consistent visuals via a tiny helper: **`use_style()`**.

---

## 📂 Datasets Used
- **Toy data** generated reproducibly with `numpy.random.default_rng(42)`.  
- **Iris** (from `scikit-learn`) for a clean, compact EDA workflow.  
> No external downloads needed.

---

## 📖 Notebook Outline
- **Setup & Style Helpers** – reproducibility, unified theme, quick gallery.  
- **Beginner Plots** – line, scatter, bar/barh, histogram (linear vs log), KDE, ECDF, box/violin, stacked area.  
- **Intermediate Customization** – subplots, annotations, legends, time-series formatting, tick formatters.  
- **Advanced Patterns** – grouped/stacked bars, twin axes, broken axis, inset, 3D surface, dense clouds (hexbin/rasterized), fast multi-lines (LineCollection).  
- **Pandas × Matplotlib Interop** – quick wins: line/rolling/area + sanity checks.  
- **EDA Mini-Pipeline (Iris)** – class balance, histograms, species scatter, correlation heatmap, box/violin, scatter matrix.  
- **Best Practices & Pitfalls** – what to avoid + export tips.  
- **Cheat Sheet** – minimal examples with common gotchas.

---

## ⚡ Quick Start
```bash
# clone
git clone https://github.com/tarekmasryo/matplotlib-tutorials
cd matplotlib-tutorials

# option A: pip
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# option B: conda
conda env create -f environment.yml && conda activate mpl-pro

# launch
jupyter notebook matplotlib-beginner-to-pro.ipynb
```
Or open directly on **Colab** / **Kaggle** via the badges above.

---

## 📦 Requirements
- Python **3.10–3.12**  
- `numpy`, `pandas`, `matplotlib (>=3.8)`, `scipy` (for `gaussian_kde`), `scikit-learn` (Iris)

_Optional (sharper inline plots in notebooks):_
```python
# %config InlineBackend.figure_format = "retina"
```

---

## ✅ Reproducibility
All randomness flows through one generator for stable results across runs/machines:
```python
rng = np.random.default_rng(42)
# rng.normal / rng.lognormal / rng.integers / ...
```



## 📜 License
MIT © [Tarek Masryo](https://github.com/tarekmasryo)

---
