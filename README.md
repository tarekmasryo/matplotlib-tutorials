# 📈 Matplotlib — Beginner-to-Pro 🎯

[![Python](https://img.shields.io/badge/Python-3.10–3.12-blue.svg)](#requirements)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-%E2%89%A53.8-11557c.svg)](#requirements)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](#license)
[![Open in Colab](https://img.shields.io/badge/Colab-Open-brightgreen.svg)](https://colab.research.google.com/github/<YOUR_USERNAME>/<REPO>/blob/main/matplotlib-beginner-to-pro.ipynb)
[![Kaggle](https://img.shields.io/badge/Kaggle-Notebook-20beff.svg)](https://kaggle.com/code/<YOUR_KAGGLE_USERNAME>/<KAGGLE_NOTEBOOK_SLUG>)

A practical, opinionated reference for **data visualization with Matplotlib** — from **beginner basics** → **intermediate customization** → **advanced patterns**, ending with a **mini Kaggle-ready EDA pipeline**.


---

## 🚀 Why this notebook?
- Clean, modular, **ready-to-paste** examples for real projects/Kaggle.  
- Consistent visuals with a tiny helper: **`use_style()`**.  
- Performance-minded patterns: **hexbin**, **rasterized scatter**, **LineCollection**.  
- True **reproducibility** via `rng = np.random.default_rng(42)`.

---

## 📂 Datasets
- **Toy data** generated reproducibly with `rng`.  
- **Iris** from `scikit-learn` for a compact, clean EDA pipeline.

---

## 📖 Notebook Outline
1. **Reproducibility** — silence warnings, print versions, set RNG.  
2. **Setup & Style** — `use_style()` + **Quick Gallery**.  
3. **Beginner Plots** — line, scatter, bar/barh, hist (linear vs log), KDE, ECDF, box/violin, stacked area.  
4. **Intermediate Customization** — subplots, annotations, legends, time-series formatting, tick formatters.  
5. **Advanced Patterns** — grouped/stacked bars, twin axes, broken axis, inset, 3D surface, dense clouds, LineCollection.  
6. **Integration Tricks** — Pandas → Matplotlib: line/rolling/area + quick data check.  
7. **Mini EDA (Iris)** — class balance, histograms, species scatter, correlation heatmap, box/violin, scatter matrix.  
8. **Best Practices & Saving Figures**.  
9. **Cheat Sheet** — minimal examples + common gotchas.

> Naming clarity: `df_area` (stacked area), `df_monthly` (Pandas interop), `df` (Iris).

---

## 🖼️ Gallery Preview
<p align="center">
  <img src="figures/01_gallery.png" width="24%" alt="Quick Gallery"/>
  <img src="figures/02_time_series.png" width="24%" alt="Time Series formatting"/>
  <img src="figures/03_twin_axes.png" width="24%" alt="Twin Axes combined legend"/>
  <img src="figures/04_hexbin.png" width="24%" alt="Hexbin for dense clouds"/>
</p>

> Generate with `dpi=200` for crisp README visuals.

---

## ⚡ Quick Start
```bash
# clone
git clone https://github.com/<YOUR_USERNAME>/<REPO>
cd <REPO>

# option A: pip
python -m venv .venv && source .venv/bin/activate   # (Windows: .venv\Scripts\activate)
pip install -r requirements.txt

# option B: conda
conda env create -f environment.yml && conda activate mpl-pro

# launch
jupyter notebook matplotlib-beginner-to-pro.ipynb
```
Or open on **Colab/Kaggle** via badges above.

---

## 📦 Requirements
- Python **3.10–3.12**  
- `numpy`, `pandas`, `matplotlib (>=3.8)`, `scipy` (for `gaussian_kde`), `scikit-learn` (Iris)

_Optional (sharper inline plots):_
```python
# %config InlineBackend.figure_format = "retina"
```

---

## ✅ Reproducibility
All randomness flows through one generator:
```python
rng = np.random.default_rng(42)
# rng.normal / rng.lognormal / rng.integers / ...
```
This guarantees the same outputs across runs/machines.

---


## 🧾 Cheat Sheet (Snapshot)
- **Grouped Bars:** `ax.bar(x - w/2, a, w); ax.bar(x + w/2, b, w)`  
- **Twin Axes:** `ax2 = ax1.twinx()`; combine legends, label units clearly; fix y-limits.  
- **Broken Axis:** two subplots sharing x with different y-limits — call out the visual cut.  
- **Inset:** `inset_axes(ax, ...)` with ticks removed.  
- **Dense Scatter:** `ax.hexbin(...)` or `plt.scatter(..., rasterized=True)`.

---

## 🗂️ Repo Structure
```
<REPO>/
├─ matplotlib-beginner-to-pro.ipynb
├─ figures/                 # exported previews used in README
├─ requirements.txt         # pip install -r requirements.txt
├─ environment.yml          # conda env (optional)
├─ helpers/                 # optional: style/pattern helpers
│  └─ style.py
└─ README.md
```

---

## 📜 License
MIT

