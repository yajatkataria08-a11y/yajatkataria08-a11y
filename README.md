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

> Real-time orbital safety · satellite imagery AI · road-safety for 7 nations · smart-city command centers · multimodal IP defense.

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

<img src="./assets/divider.svg" width="100%" alt=""/>

## 🏅 Hackathon Trail

<img src="./assets/timeline.svg" alt="Hackathon timeline" width="100%"/>

| 🏆 Event | 💡 Project | 🛠️ Stack | 📌 Status |
|---|---|---|---|
| NSH 2026 · IIT Delhi | Orbital Insight | FastAPI · XGBoost · Docker | 🔥 In progress |
| AI for Bharat | Trinetra V5.0 | CLIP · FAISS · AWS | ✅ Shipped & live |
| Startathon 2026 · E-Cell VIT Bhopal | DINOv2 Terrain Segmentation | PyTorch · Streamlit | ✅ Shipped |

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
| 🧠 | **Advanced Deep Learning** | Transformers, ViT, Diffusion Models |
| ⚙️ | **System Design** | Scalable ML pipelines & microservices |
| 🔐 | **Cloud Security** | AWS IAM, VPCs, Security Groups |
| 🏎️ | **Competitive Programming** | Codeforces Div 2/3 |
| 🌐 | **Web3 Fundamentals** | Smart contracts & dApps |

## 🤝 Open To

🤝 **Hackathon collabs** (AI/ML, systems) · 💼 **Internships** (AI/ML, full-stack, backend) · 🔬 **Research** (computer vision, NLP, multimodal) · 🌟 **Open source** (Python, ML tooling, FastAPI)

## 📫 Let's Connect

| Platform | Link |
|---|---|
| 📧 Email | [yajatkataria08@gmail.com](mailto:yajatkataria08@gmail.com) |
| 💼 LinkedIn | [linkedin.com/in/yajatkataria](https://linkedin.com/in/yajatkataria) |
| 🧩 LeetCode | [leetcode.com/yajatkataria](https://leetcode.com/yajatkataria) |
| 🟢 HackerRank | [hackerrank.com/profile/yajatkataria08](https://www.hackerrank.com/profile/yajatkataria08) |
| 📍 Location | Indore, India |

<img src="./assets/footer.svg" alt="Ship fast, iterate faster." width="100%"/>
