# Gabriel Dias Moreira

**Data Scientist & ML Engineer** — rigorous modeling, production ML and LLM systems.

I build models that are evaluated the way they will be used: temporal and spatial
hold-outs instead of random splits, honest baselines, calibrated probabilities and
results reported even when the model only ties the baseline. Then I ship them —
infrastructure as code, CI with type checks and coverage gates, monitored endpoints
and evaluated LLM agents.

📫 gabriel.dias09@icloud.com · [LinkedIn](https://www.linkedin.com/in/gabrieldiasmoreira/)

---

## Featured projects

### [Chuva_bh](https://github.com/Dias0202/Chuva_bh) — hourly rain nowcasting for Belo Horizonte
Probability of ≥ 0.5 mm of rain in the next 1, 3 and 6 hours from INMET stations,
METAR and Open-Meteo. A single XGBoost model with the horizon as a feature, a strict
temporal split (train ≤ 2023, validation 2024, test 2025) and persistence and NWP
baselines, scored with Brier, PR-AUC, CSI/POD/FAR and reliability tables.
Deployed with AWS CDK (SageMaker pipeline, model registry with manual approval, PSI
drift monitoring and retraining alarms). Includes a LangGraph agent on Bedrock with
guardrails, evaluated against a 36-question golden set. 281 tests, 80% coverage gate.
`Python` `XGBoost` `AWS CDK` `SageMaker` `LangGraph` `Bedrock` `mypy --strict`

### [yellow-fever-risk-brazil](https://github.com/Dias0202/yellow-fever-risk-brazil) — sylvatic yellow fever risk, 5,570 municipalities
Season-level (July–June) forecasting of yellow fever spillover, modelled as a wave
that propagates rather than as static habitat suitability. Prospective and
spatio-temporal block validation, decision curves and decile calibration; the final
model is a 12-variable logistic regression with one representative per mechanism.
Climate scenarios from a 5-GCM × 4-SSP CMIP6 ensemble with resampling-based
uncertainty, plus an [interactive dashboard](https://dias0202.github.io/yellow-fever-risk-brazil/).
`Python` `scikit-learn` `SHAP / ALE` `CMIP6` `GitHub Actions`

### [Transito_bh](https://github.com/Dias0202/Transito_bh) — road-crash risk and interventions in Belo Horizonte
LightGBM Poisson on H3 cells × day × hour compared against simple baselines, Poisson
GLM with clustered standard errors, fixed effects for speed cameras and a
before/after design with placebo tests for speed bumps, plus a Monte Carlo simulator
and a bilingual Quarto paper. [Live dashboard](https://dias0202.github.io/transito-bh/).
`Python` `LightGBM` `statsmodels` `H3` `Quarto`

### [VavaPPRT](https://github.com/Dias0202/VavaPPRT) — analytics platform and LLM Discord bot
FastAPI + PostgreSQL + React. The bot uses a provider-agnostic LLM client
(Gemini/Groq) with fallback, streaming, `Retry-After` handling and a bounded tool
loop, plus speech-to-text with faster-whisper. CI runs the test suite against SQLite
and PostgreSQL 17.
`FastAPI` `PostgreSQL` `React` `LLM tool use` `faster-whisper`

### [BirdCLEF-2026_GDM](https://github.com/Dias0202/BirdCLEF-2026_GDM) — bird-call classification from audio
EfficientNet-B0 on log-Mel spectrograms with attention pooling, MixUp, SpecAugment,
mixed precision, MLflow tracking and Grad-CAM, validated with the competition metric on
recordist-grouped folds so that no recordist appears on both sides of a split.
`PyTorch` `audio` `MLflow`

### [HairPainter](https://github.com/Dias0202/HairPainter) — fibril measurement in electron microscopy
Segmentation and measurement of Mimivirus fibrils in TEM images (CLAHE, optional
U-Net, OCR of the scale bar) with a desktop GUI.
`OpenCV` `PyTorch` `computer vision`

---

## Toolbox

- **Modeling:** scikit-learn, XGBoost, LightGBM, PyTorch, statsmodels; time-series and
  spatial validation, calibration, decision curves, SHAP/ALE, count models, quasi-experimental designs
- **ML engineering:** AWS CDK, SageMaker, MLflow, Docker, GitHub Actions, pytest, mypy, ruff, uv
- **LLM systems:** LangGraph, Amazon Bedrock, Gemini/Groq APIs, tool calling, guardrails, golden-set evaluation
- **Data & backend:** Python, SQL, PostgreSQL, FastAPI, pandas, geospatial (H3, rasters, Earth Engine)

Also: bioinformatics tools from my research background —
[SAMANTHEX_2.0](https://github.com/Dias0202/SAMANTHEX_2.0) (Sanger consensus GUI) and
[viral-ngs-pipeline](https://github.com/Dias0202/viral-ngs-pipeline).
