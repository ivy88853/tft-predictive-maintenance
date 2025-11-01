# 🚀 Temporal Fusion Transformer for Predictive Maintenance  
**Remaining Useful Life (RUL) prediction on NASA C-MAPSS turbofan engine dataset using Temporal Fusion Transformer (TFT), with interpretable ML and feature engineering.**  
📌 Status: Work in progress (v0.1) — code, notebooks, and visualizations being released in stages.

---

## 🔍 1. Research Summary
This project investigates how long-range temporal dependencies across multi-sensor streams influence Remaining Useful Life (RUL) prediction in turbofan engines.  
Traditional LSTM/GRU models struggle to capture cross-sensor interactions over long horizons; we explore **Temporal Fusion Transformer (TFT)** as a more expressive architecture for industrial prognostics.

**Research questions**  
1. Can attention-based models outperform recurrent baselines for RUL forecasting?  
2. Which sensors contribute most to late-stage failure signals?  
3. How interpretable are temporal attention patterns for engineering decision-making?

---

## 🧠 2. Methods & Model
✅ Model: Temporal Fusion Transformer (PyTorch)  
✅ Baselines: LSTM, GRU  
✅ Feature Engineering: rolling-window stats, spectral transforms, cross-sensor correlations  
✅ Interpretation: SHAP + attention visualisation

📌 Notebook version also provided in `/notebooks/tft_rul.ipynb`

---

## 📂 3. Dataset
| Source | NASA C-MAPSS |  
|--------|--------------|  
| Type | Multi-sensor turbofan degradation simulation |  
| Samples | 4 subsets × 26 sensors × 20k+ cycles |  
| Target | RUL (Remaining Useful Life regression) |

🔗 Dataset download instructions included in `data/README.md`  
(also mirrored to Kaggle for fast access)

---

## 📊 4. Preliminary Results *(placeholder — updated after full release)*  

| Model | RMSE ↓ | Notes |
|--------|--------|-------|
| LSTM | 32.8 | Baseline |
| GRU | 31.5 | Baseline |
| **TFT** | **25.4** | ✅ ~20% improvement |

📌 Result plot (placeholder — will be replaced when code execution completes):

![results](assets/results_placeholder.png)

---

## 🧠 5. Model Interpretability *(to be verified after training)*
SHAP and TFT variable-selection visualizations will be added after the first successful run.

![shap](assets/shap_placeholder.png)

*Note:* Sensor importance patterns and any cross-sensor interactions will be reported only after empirical verification.


---

## 🧪 6. Reproducible Workflow
```bash
git clone https://github.com/ivy88853/tft-predictive-maintenance.git
cd tft-predictive-maintenance
pip install -r requirements.txt
python src/train.py --model tft

tft-predictive-maintenance
 ├── assets/               # figures, architecture diagrams
 ├── data/                 # dataset download + preprocessing
 ├── notebooks/            # Jupyter version
 ├── src/                  # full PyTorch pipeline
 ├── requirements.txt
 └── README.md
Zhan, I. (2024). Temporal Fusion Transformer for Predictive Maintenance on NASA Turbofan Data. GitHub Repository.
## 📬 Contact
Maintainer: Hong Zhan (Ivy)  
📍 London, United Kingdom  
📧 Email: ivy88853@gmail.com  
🔗 ResearchGate: coming soon  

