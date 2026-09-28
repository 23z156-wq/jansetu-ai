# JanSetu AI (जनसेतु)
### Multilingual Digital Public Good for Citizen-Driven National Infrastructure Planning

[![Built with Google AI](https://img.shields.io/badge/Google%20Cloud-Gemini%201.5%20%7C%20BigQuery-4285F4?logo=google-cloud&logoColor=white)](https://cloud.google.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Hackathon](https://img.shields.io/badge/Build%20with%20AI-Code%20for%20Communities%202026-green)](#)

## 📌 Executive Summary
Governments across India struggle to consolidate citizen feedback and align it with central infrastructure priorities. Development requests live in fragmented regional systems, leading to misaligned public spending under flagship schemes like PMGSY and Jal Jeevan Mission.

**JanSetu AI** bridges this gap as an open-source **Digital Public Good (DPG)**. It aggregates citizen grievances across regional Indian languages via voice notes and text, clusters demand using **BigQuery GIS**, and applies predictive prioritization (**Infrastructure Priority Index - IPI**) to recommend actionable project sanctions to national policymakers.

---

## 🏛️ System Architecture
[ Citizen Ingestion ] ──────> [ Multilingual NLU ] ──────> [ Geospatial Fusion ] ──────> [ Policy Dashboard ]
• Regional Voice Notes         • Cloud Speech-to-Text        • BigQuery GIS Clustering     • Spatial Heatmaps
• WhatsApp / PWA Intake        • Gemini 1.5 Multimodal NLU   • data.gov.in Scheme Gaps     • Auto Sanction Briefs
• Dialect Parsing (Tamil/Hi)   • Entity & Geo Extraction     • IPI Scoring Algorithm       • District Collector View

---

## 🚀 Key Features

1. **Multilingual & Voice-First Intake:** Ingests citizen feedback in regional languages (Tamil, Hindi, Marathi, Telugu) using Gemini 1.5 Flash multimodal understanding.
2. **Predictive Prioritization Index (IPI):** Computes a dynamic urgency score:
   $$\text{IPI} = w_1(\text{Demand Density}) + w_2(\text{Vulnerability Factor}) + w_3(\text{Scheme Gap}) - w_4(\text{Spam/Dupes})$$
3. **Spatial Data Fusion:** Cross-references citizen demand clusters with real open public datasets (Jal Jeevan Mission, PMGSY roads, Census demographic indicators).
4. **Automated Policy Briefs:** Generates formal administrative sanction directives for District Collectors using Gemini 1.5 Pro.

---

## 🛠️ Google Cloud Tech Stack

- **Generative AI:** Gemini 1.5 Flash (low-latency extraction), Gemini 1.5 Pro (policy synthesis)
- **Data & GIS:** BigQuery GIS (`ST_GEOHASH`, `ST_CLUSTERDBSCAN`), Google Maps Platform / Leaflet
- **Backend & Deployment:** FastAPI, Cloud Run, GitHub Pages

---

## 💻 Quick Start & Deployment

### Run Frontend Locally
Open `index.html` directly in any web browser, or access the live deployment:
👉 **[Live Prototype Demo](https://swethaswinirajmohan.github.io/jansetu-ai/)**

### Run Backend API
```bash
git clone [https://github.com/](https://github.com/)<your-username>/jansetu-ai.git
cd jansetu-ai
pip install -r requirements.txt
export GEMINI_API_KEY="your-api-key"
uvicorn backend.main:app --reload --port 8080

