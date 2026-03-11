# Subnational Politics Project (SPP) - Data Repository

This repository (`fsotoj/spp-data`) serves as the primary data storage and distribution point for the **Subnational Politics Project (SPP)**. 
It provides the raw and processed datasets required by the SPP R Shiny interactive dashboard, which is deployed on Hugging Face Spaces and embedded on [subnationalpolitics.com](https://subnationalpolitics.com).

## 📊 Overview

The SPP Shiny application fetches and joins datasets directly from this repository to power its interactive visualizations, which include maps, charts, and detailed data tables depicting subnational political data across various countries (e.g., Mexico, Argentina, Brazil).

## 📂 Structure
- `data/`: Contains the datasets (Excel, CSV, etc.) that the Shiny application consumes.
- `public/`: Additional public-facing assets or static files.

## 🔗 Related Repositories
- **SPP App Repository**: The R Shiny application engine that consumes this data is managed in the Hugging Face Deployment repository (e.g. `spp-hf`).

## 📡 Data Flow Integration
When the SPP Shiny app initializes, it relies on this repository as its system of record:
1. The dashboard application first checks its local data cache.
2. If the locally cached data is missing or outdated, the application automatically fetches the latest data versions from this `spp-data` repository.
3. The retrieved data is then processed, joined, and served to the reactive modules of the Shiny frontend.
