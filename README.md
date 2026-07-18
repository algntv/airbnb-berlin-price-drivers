# Airbnb Berlin — Price Drivers

> An exploratory data analysis of **14,274 Airbnb listings in Berlin** that identifies the factors most associated with nightly price.

**[View the interactive project page](https://YOUR_GITHUB_USERNAME.github.io/airbnb-berlin-price-drivers/)** · **[Open the notebook](./airbnb_berlin_eda.ipynb)** · **[See the presentation](./airbnb_berlin_eda_presentation.pptx)**

![Room type price comparison](assets/room_type_prices.png)

## Why this project

Pricing in short-term rentals is shaped by more than just location. This project turns a university coursework into a reproducible portfolio analysis: it cleans the raw dataset, visualises pricing patterns, and translates the evidence into practical conclusions.

## Main findings

| Finding | Evidence |
| --- | --- |
| **Room type is the strongest categorical signal.** | Hotel rooms average **€197** per night; entire homes **€141**; private rooms **€81**; shared rooms **€48**. |
| **Location matters.** | The average price in Mitte is **€146.6**, versus **€87.4** in Reinickendorf. |
| **Capacity drives price.** | Price and guest capacity have a correlation of **0.59**. |
| **Longer minimum stays are cheaper per night.** | Correlation between price and minimum nights: **−0.20**. |
| **Reputation alone is weak.** | Rating and price correlate at only **0.03**. |

## Visual evidence

<p align="center">
  <img src="assets/district_prices.png" width="48%" alt="Mean price by district" />
  <img src="assets/capacity_price.png" width="48%" alt="Price vs capacity" />
</p>

<p align="center">
  <img src="assets/correlation_matrix.png" width="54%" alt="Correlation matrix" />
</p>

## Dataset

- **Source:** [Inside Airbnb — Berlin](https://insideairbnb.com/get-the-data/)
- **Snapshot:** 23 September 2025
- **Raw data:** 14,274 listings × 79 variables
- **Outlier treatment:** prices above the 99th percentile (€617.37) removed
- **Analytical sample:** 9,171 listings

The raw file is deliberately excluded from this repository. The notebook downloads the exact source extract automatically if it is not present locally.

## Tech stack

`Python` · `pandas` · `NumPy` · `matplotlib` · `seaborn` · `Jupyter`

## Reproduce locally

```bash
git clone https://github.com/YOUR_GITHUB_USERNAME/airbnb-berlin-price-drivers.git
cd airbnb-berlin-price-drivers
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook airbnb_berlin_eda.ipynb
```

## What I would add next

1. Build a train/test price-prediction baseline with regularised regression.
2. Add listing text, geospatial features, and host-level effects.
3. Compare pricing across multiple snapshots to capture seasonality.

---

Created by Alexander Ignatiev as a data analytics portfolio project.
