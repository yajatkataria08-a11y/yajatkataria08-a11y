<div align="center">

<img src="./assets/banner.svg" alt="Yajat Kataria — Full-Stack AI/ML Developer" width="100%"/>

<br/>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/yajatkataria)
[![LeetCode](https://img.shields.io/badge/LeetCode-FFA116?style=for-the-badge&logo=leetcode&logoColor=black)](https://leetcode.com/yajatkataria)
[![HackerRank](https://img.shields.io/badge/HackerRank-00EA64?style=for-the-badge&logo=hackerrank&logoColor=black)](https://www.hackerrank.com/profile/yajatkataria08)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:yajatkataria08@gmail.com)

![Profile Views](https://komarev.com/ghpvc/?username=yajatkataria08-a11y&color=22d3ee&style=flat-square&label=Profile+Views)
![Followers](https://img.shields.io/github/followers/yajatkataria08-a11y?style=flat-square&color=22d3ee)

</div>

<img src="./assets/divider.svg" width="100%" alt=""/>

<img src="./assets/terminal.svg" alt="About me — terminal" width="100%"/>

<img src="./assets/numbers.svg" alt="By the numbers" width="100%"/>

<img src="./assets/divider.svg" width="100%" alt=""/>

## 🚀 Featured Projects

> Lunar AI habitat scoring · exoplanet vetting & habitability AI · turbofan digital twin · real-time orbital safety · satellite imagery AI · road-safety for 7 nations · smart-city command centers · multimodal IP defense.

<br/>

### 🌕 LUNARIS — Lunar Lava Tube Subsurface Habitat & Stability Mapper

<img src="./assets/card-lunaris.svg" alt="LUNARIS — Lunar Lava Tube Subsurface Habitat & Stability Mapper" width="100%"/>

A **peer-reviewed planetary AI system** that identifies, ranks, and architecturally models the best candidate lunar lava tube skylights for long-duration human habitation — focused on the **Marius Hills Hole** (Oceanus Procellarum, 14.08°N, 303.20°E).

Integrates ISRO Chandrayaan-2 multi-sensor data (OHRC, DFSAR, TMC-2, ChaSTE) through a 5-stage ML pipeline to produce a calibrated **Lunar Habitat Index (LHI)** score per candidate site.

<img src="./assets/arch-lunaris.svg" alt="LUNARIS architecture" width="100%"/>

- 🛰️ **Multi-Sensor Fusion:** OHRC 25cm orthophotos, DFSAR 24cm L-Band quad-pol SAR (m-chi decomposition, double-bounce), TMC-2 DTM terrain, ChaSTE subsurface thermal profiles
- 🧠 **Attention U-Net + Stacking Ensemble:** Semantic skylight segmentation → feature extraction → XGBoost / LightGBM / RandomForest Ridge meta-learner for final LHI scoring
- 🔬 **Physics Inversion:** DFSAR polarimetric scattering matrix inversion, ChaSTE thermal stability (–20°C target), Mohr–Coulomb geomechanical Factor of Safety, MMD domain adaptation
- 🎯 **SHAP Explainability:** Game-theoretic Shapley attribution per site — deconstructs every remote-sensing observation contributing to the habitat score
- 🌐 **Full-Stack Observatory UI:** Next.js 15 / React 19 mission control with live 3D Chandrayaan-2 orbit visualization (Three.js), interactive SHAP HUD, candidate leaderboard, subsurface cross-section viewer, 4 dynamic themes (URJA ☀️, DARK 🌑, LIGHT ☁️, JUNGO 🌿)
- ✅ **43/43 pytest passing** · TypeScript strict · Render-deployed FastAPI backend

```
Backend  : Python · FastAPI · uvicorn · SQLite
ML       : Attention U-Net · XGBoost · LightGBM · RandomForest · Ridge · TreeSHAP
Physics  : DFSAR m-chi · ChaSTE thermal · Mohr-Coulomb FoS · MMD Domain Adaptation
Data     : ISRO Chandrayaan-2 (OHRC / DFSAR / TMC-2 / ChaSTE) · NASA LROC/LOLA 2K albedo
Frontend : Next.js 15 · React 19 · TypeScript · TailwindCSS · Three.js · D3.js · Plotly.js
```

[![Repo](https://img.shields.io/badge/Repo-LUNARIS-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/LUNARIS)

<br/>

### 🔭 ASTRÆA — Citadel Observatory

<img src="./assets/card-astraea.svg" alt="ASTRÆA Citadel Observatory" width="100%"/>

A full-stack astrophysics and explainable-AI mission control platform for **exoplanet candidate vetting**, **habitability & composition modeling**, and **SPHEREx-style 102-channel sky-change anomaly detection** across **14,727 real NASA/TESS catalog targets**.

<img src="./assets/arch-astraea.svg" alt="ASTRÆA architecture" width="100%"/>

- 🪐 **AI Vetting (`B2`):** leak-free 8-feature **LightGBM** classifier (**0.977** KOI ROC-AUC · **0.952** TESS v4 fine-tuned ROC-AUC) with exact **TreeSHAP** per-target waterfall explanations
- 🌡️ **Habitability Physics (`B1`):** Monte Carlo uncertainty propagation through the **Chen–Kipping** mass–radius forecaster and **Kopparapu** habitable zone boundaries
- 🔭 **Sky Change Explorer (`Project A`):** 102-channel spectrophotometric SED synthesizer (`0.75–5.00 µm`), Mandel–Agol transit synthesis, centroid tripwire, and anomaly ranking
- ⚡ **Streaming & Auth:** FastAPI backend with 250-row async **SSE** batch scanning, SQLite triage persistence, `scrypt` + HMAC-SHA256 bearer tokens, and Google/GitHub/Microsoft **OAuth2 PKCE**
- 🎨 **Observatory Console:** **Next.js 15 / React 19** UI with interactive **D3.js** & **Plotly.js** charts, Aladin sky maps, custom WebGL/Canvas starfield, and 4 dynamic themes (`URJA`, `JUNGO`, `DARK`, `LIGHT`)

```
Backend  : Python · FastAPI · SSE Streaming · SQLite · OAuth2 PKCE
ML       : LightGBM · TreeSHAP · scikit-learn · Cross-Mission Fine-Tuning
Physics  : Monte Carlo HZ · Chen-Kipping Forecaster · Mandel-Agol Transits · SPHEREx 102-ch
Data     : NASA Exoplanet Archive (KOI, PS) · TESS (TOI) · Parquet (14,727 rows)
Frontend : Next.js 15 · React 19 · TypeScript · TailwindCSS · D3.js · Plotly.js
```

[![Repo](https://img.shields.io/badge/Repo-astraea--citadel--observatory-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/astraea-citadel-observatory)

<br/>

### ✈️ Turbozone (GENZONE)

<img src="./assets/card-turbozone.svg" alt="Turbozone" width="100%"/>

A physics-informed, **explainable digital twin** of a two-spool turbofan engine, built for **AI Manthan**. Trained on **NASA N-CMAPSS**, it predicts remaining useful life, tracks component health, and shows *why* behind every prediction.

<img src="./assets/arch-turbozone.svg" alt="Turbozone pipeline" width="100%"/>

- ⏳ **RUL:** stacking ensemble of Random Forest, XGBoost, LightGBM and CatBoost into a Ridge meta-learner, with empirical prediction intervals
- 🧪 **Physics layer:** healthy-condition baseline plus pressure-ratio and efficiency proxies derived from measured stations
- 📡 **Gas-path health:** Extended Kalman Filter with observability-based state selection, so only identifiable components are estimated
- 🔧 **Component forecasts:** per-component RUL and 10/25/50-flight health forecasts, shown only when they beat baselines
- 🔍 **Explainability:** SHAP, Ridge contributions, per-sensor occlusion and EKF diagnostics
- 🖥️ **Dashboard:** FastAPI backend with a live UI: fleet queue, RUL, gas-path health and maintenance log
- ☁️ **Reproducible:** Colab notebook shares its pipeline code with the backend, with a parity check between the two

```
Backend  : Python · FastAPI
ML       : XGBoost · LightGBM · CatBoost · Random Forest · Ridge · SHAP
Physics  : Extended Kalman Filter · Gas-path modelling
Data     : NASA N-CMAPSS · HDF5 · Google Colab
Frontend : HTML5 · JavaScript · CSS3
```

[![Repo](https://img.shields.io/badge/Repo-Turbozone-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/Turbozone)

<br/>

### 🛰️ Orbital Insight

<img src="./assets/card-orbital.svg" alt="Orbital Insight" width="100%"/>

Autonomous collision management for **55 satellites** dodging **~15,000 debris objects**: predict the risk, plan the burn, fire the thrusters. Built by Team BroCODE for **NSH 2026 at IIT Delhi**.

<img src="./assets/arch-orbital.svg" alt="Orbital Insight system flow" width="100%"/>

- 🪐 **Physics:** RK4 propagation with J2 oblateness; two-burn Hohmann transfers to a graveyard orbit when fuel runs low
- 🤖 **ML:** calibrated XGBoost collision probability (Chan formula as baseline/fallback), Thompson Sampling for burn direction, Isolation Forest for anomalous debris, quadratic RLS fuel forecasting, Kalman conjunction tracking
- ♻️ **Self-improving:** missed predictions are logged and retrained on; a new model only replaces the old one if it scores better
- 🌍 **UI:** live 3D globe, ground tracks, fuel heatmap, maneuver timeline + Streamlit analytics with SHAP explanations
- 🐳 **Infra:** single Docker container (Supervisord → Nginx + FastAPI + Streamlit), deployed on Railway

[![Repo](https://img.shields.io/badge/Repo-orbital--insight-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/orbital-insight)
[![Live Demo](https://img.shields.io/badge/Live_Demo-Railway-0B0D0E?style=for-the-badge&logo=railway)](https://orbital-insight-production.up.railway.app)

<br/>

### 🌍 GEOSEG

<img src="./assets/card-geoseg.svg" alt="GEOSEG" width="100%"/>

A full-stack Earth-observation platform that tackles mixed-pixel blur and coarse 10–20 m ground sampling in **Sentinel-2 L2A** imagery: it super-resolves up to **8×** and then segments land cover.

<img src="./assets/arch-geoseg.svg" alt="GEOSEG pipeline" width="100%"/>

<img src="./assets/geoseg-chart.svg" alt="PSISR vs baselines" width="100%"/>

- 🔬 **PSISR:** 3-stage progressive cascade (2× → 4× → 8×) with UBCF blocks, a learnable Pearson correlation filter and PixelShuffle upscaling; adaptive MSE + SSIM loss
- 🗺️ **Segmentation:** ResNet-34 U-Net on a 16-channel input (13 bands + NDVI/NDWI/NDBI) with distance-weighted overlap blending
- ⚡ **Native core:** C++20 engine with AVX2 tiling and normalization, reported up to 4.8× faster than NumPy
- 🖥️ **Viewer:** React + Vite split-view (low-res vs 8×), coordinate HUD, Google/ISRO Bhuvan/Esri/OSM basemaps, preset AOIs including Bhopal

[![Repo](https://img.shields.io/badge/Repo-GEOSEG-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/GEOSEG)

<br/>

### 🛣️ Road Safety AI

<img src="./assets/card-roadsafety.svg" alt="Road Safety AI" width="100%"/>

One offline-first PWA for crash response, traffic-law compliance, civic issue reporting and authority accountability across all **7 BIMSTEC nations**.

<img src="./assets/arch-roadsafety.svg" alt="Road Safety AI cascade" width="100%"/>

- 🚑 **RoadSoS CrashMode:** one-tap 60-minute "Golden Hour" countdown, offline first-aid, 112/108/100 dialing, trauma-centre navigation, multi-channel alerts (SMS, WhatsApp, email, webhooks)
- ⚖️ **DriveLegal AI:** 154 verified violations, fines by vehicle type, repeat-offence penalties, Motor Vehicles Act citations, Hinglish support
- 🔥 **RoadWatch:** severity-weighted Leaflet heatmap, GPS-tagged reports, upvoting, SLA breach alerts
- 📄 **Challan OCR:** client-side Tesseract.js + server-side pytesseract
- 🧠 **Cascade:** keyword classifier → BiLSTM NER → FAISS RAG work offline; below a 0.65 confidence threshold it escalates to Gemini Flash, with Groq Llama-3.1-70B as fallback

[![Repo](https://img.shields.io/badge/Repo-Roadsafety--AI-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/Roadsafety-AI)

<br/>

### 🏙️ NagarSetu V2.0

<img src="./assets/card-nagarsetu.svg" alt="NagarSetu V2.0" width="100%"/>

A smart-city civic intelligence platform for Bhopal and Indore: citizens get a multi-module Android super-app, and responders get a live **command center** with an SOS queue, tactical map and incident triage.

<img src="./assets/arch-nagarsetu.svg" alt="NagarSetu system map" width="100%"/>

- 📱 **Android:** Kotlin + Jetpack Compose, 12+ feature modules, plus the Raksha safety module
- 🖥️ **Command Center:** Next.js 15 + TypeScript + Tailwind, three-panel layout (SOS queue · map · triage), runs on mock data without a backend
- 🔌 **Realtime:** Node.js / Express / Socket.IO event stream
- 🧠 **ai_engine:** Python FastAPI + scikit-learn service, built in phases on a 15-phase roadmap

[![Repo](https://img.shields.io/badge/Repo-NagarsetuV2.0-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/NagarsetuV2.0)

<br/>

### 🛡️ Trinetra V5.0

<img src="./assets/card-trinetra.svg" alt="Trinetra V5.0" width="100%"/>

A multimodal intellectual-property defense registry for the **AI for Bharat** hackathon: register an asset once, then catch duplicates and infringements across images, audio and text.

<img src="./assets/arch-trinetra.svg" alt="Trinetra architecture" width="100%"/>

- 🖼️ CLIP image similarity and CLAP audio embeddings behind a FAISS HNSW index
- 📝 Amazon Titan Embeddings V2 for text, AWS Rekognition for faces and objects, reverse image "Web Peek"
- 🌐 Sarvam AI for 10+ Indic languages
- 🏗️ Refactored from a 3,800-line monolith into a 10-module architecture

[![Repo](https://img.shields.io/badge/Repo-Trinetra__AI-181717?style=for-the-badge&logo=github)](https://github.com/yajatkataria08-a11y/Trinetra_AI)
[![Live Demo](https://img.shields.io/badge/Live_Demo-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://trinetra-ai-team-human.streamlit.app)

<img src="./assets/divider.svg" width="100%" alt=""/>

## 🧰 More Builds

| Project | What it is | Stack |
|---|---|---|
| 🏜️ **DINOv2 Terrain Segmentation** | 10-class offroad segmentation, Startathon 2026 (E-Cell VIT Bhopal) | PyTorch · DINOv2 · CutMix/MixUp · Focal Loss · EMA |
| 🚖 **RideFlex** | Corporate/SEZ employee ride-hailing with C++ matching engine, ladies-only matching and SOS | FastAPI · Next.js · React Native · C++ (pybind11) |
| 🎓 **ElevateAI** | AI-powered student OS: Student DNA, TrustScore Network, CampusOS | Flutter · Supabase |
| 🧮 **SciCalc** | Scientific calculator with C++/WASM core and Material You dark theme | Next.js 15 · TypeScript · C++/WASM |
| 🎙️ [**Friday_ai**](https://github.com/yajatkataria08-a11y/Friday_ai) | Python voice assistant inspired by Marvel's FRIDAY | Python |

<img src="./assets/divider.svg" width="100%" alt=""/>

## ⚙️ How I Ship

<img src="./assets/pipeline.svg" alt="24–48 hour build loop" width="100%"/>

## 🌌 Tech Constellation

<img src="./assets/tech-orbit.svg" alt="Tech stack orbit" width="100%"/>

### 🛠️ Skills & Stack

| Domain | Technologies |
|---|---|
| **Planetary & Space AI** | `Attention U-Net` · `SAR Polarimetry (DFSAR m-chi)` · `Thermal Inversion (ChaSTE)` · `MMD Domain Adaptation` · `Lunar Photometry (Lommel-Seeliger)` · `Three.js 3D Orbit` |
| **AI / ML & Explainability** | `LightGBM` · `XGBoost` · `CatBoost` · `PyTorch` · `scikit-learn` · `TreeSHAP` · `FAISS` · `CLIP` · `Isolation Forest` · `BiLSTM` · `DINOv2` |
| **Scientific & Physics Computing** | `NumPy` · `SciPy` · `OpenCV` · `Monte Carlo Simulation` · `Extended Kalman Filter` · `RK4 + J2` · `Mohr-Coulomb FoS` · `Parquet` |
| **Backend & Auth** | `Python` · `FastAPI` · `SSE Streaming` · `Node.js` · `Express` · `Socket.IO` · `SQLite` · `Supabase` · `OAuth2 PKCE` · `scrypt + HMAC-SHA256` |
| **Frontend & Data Viz** | `Next.js 15` · `React 19` · `TypeScript` · `TailwindCSS` · `Three.js` · `D3.js` · `Plotly.js` · `Streamlit` · `Leaflet` |
| **Systems, Mobile & Infra** | `C++20 (AVX2 / pybind11 / WASM)` · `Kotlin (Jetpack Compose)` · `Flutter` · `Docker` · `AWS` · `Render` · `Railway` |

<img src="./assets/divider.svg" width="100%" alt=""/>

## 📊 GitHub Activity

<div align="center">

<img height="180" src="https://github-readme-stats.vercel.app/api?username=yajatkataria08-a11y&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" alt="GitHub stats"/>
<img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=yajatkataria08-a11y&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top languages"/>

<img src="https://streak-stats.demolab.com?user=yajatkataria08-a11y&theme=tokyonight&hide_border=true&date_format=M%20j%5B%2C%20Y%5D" alt="Streak"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=yajatkataria08-a11y&theme=tokyo-night&hide_border=true&area=true" alt="Activity graph" width="100%"/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/yajatkataria08-a11y/yajatkataria08-a11y/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/yajatkataria08-a11y/yajatkataria08-a11y/output/github-snake.svg"/>
  <img alt="Contribution snake" src="https://raw.githubusercontent.com/yajatkataria08-a11y/yajatkataria08-a11y/output/github-snake.svg" width="100%"/>
</picture>

<img src="https://github-profile-trophy.vercel.app/?username=yajatkataria08-a11y&theme=tokyonight&no-frame=true&row=1&column=7" alt="Trophies"/>

</div>

## 💻 Competitive Programming

<div align="center">

[![LeetCode Stats](https://leetcode-badge-showcase.vercel.app/api?username=yajatkataria&theme=dark&border=no_border)](https://leetcode.com/yajatkataria)

</div>

`Binary search on answer` · `Greedy` · `Trees & graphs (BFS/DFS)` · `Dynamic programming` · `Two pointers / sliding window` · `Stack & queue`

## 📚 Currently Learning

| | Focus | Topics |
|---|---|---|
| 🌕 | **Planetary AI & Remote Sensing** | SAR polarimetry, lunar photometry, geomechanical FoS |
| 🧠 | **Advanced Deep Learning** | Transformers, ViT, Diffusion Models, Attention U-Net |
| ⚙️ | **System Design** | Scalable ML pipelines & microservices |
| 🔐 | **Cloud Security** | AWS IAM, VPCs, Security Groups |
| 🏎️ | **Competitive Programming** | Codeforces Div 2/3 |
| 🌐 | **Web3 Fundamentals** | Smart contracts & dApps |

## 🤝 Open To

🤝 **Hackathon collabs** (AI/ML, systems, space-tech) · 💼 **Internships** (AI/ML, full-stack, backend) · 🔬 **Research** (computer vision, NLP, multimodal, planetary AI) · 🌟 **Open source** (Python, ML tooling, FastAPI)

## 📫 Let's Connect

| Platform | Link |
|---|---|
| 📧 Email | [yajatkataria08@gmail.com](mailto:yajatkataria08@gmail.com) |
| 💼 LinkedIn | [linkedin.com/in/yajatkataria](https://linkedin.com/in/yajatkataria) |
| 🧩 LeetCode | [leetcode.com/yajatkataria](https://leetcode.com/yajatkataria) |
| 🟢 HackerRank | [hackerrank.com/profile/yajatkataria08](https://www.hackerrank.com/profile/yajatkataria08) |
| 📍 Location | Indore, India |

<img src="./assets/footer.svg" alt="Ship fast, iterate faster." width="100%"/>
