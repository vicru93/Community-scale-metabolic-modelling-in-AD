# Hybrid Metagenomic-Reference Genome Approach for Community-Scale Metabolic Modelling in Anaerobic Co-Digestion

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![R](https://img.shields.io/badge/R-4.0%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![Study Type](https://img.shields.io/badge/Study-In_Silico_&_Metabolomics-orange)

## 🧬 Graphical Abstract

![Graphical Abstract](docs/Infografia.png)

## 📝 Project Overview

This repository hosts the computational framework, datasets, and Genome-Scale Metabolic Models (GEMs) developed for the study: **"Hybrid metagenomic-reference genome approach for community-scale metabolic modelling in anaerobic co-digestion"**.

Anaerobic digestion (AD) is a complex bioprocess driven by intricate microbial consortia. Traditional metagenomic approaches often yield fragmented Metagenome-Assembled Genomes (MAGs), resulting in "functional holes" in metabolic reconstructions. This study introduces a **hybrid framework** that integrates MAGs with reference genomes and utilizes **metabolomics-guided gapfilling** to construct robust community models.

### Key Innovations:
* **Hybrid Assembly Strategy:** Combines 1,354 MAGs with reference genomes to maximise taxonomic and functional coverage.
* **Metabolomics-Driven Curation:** Uses untargeted LC-MS/MS profiles (e.g., SCFAs, terpenoids) to validate and gap-fill metabolic pathways.
* **Dynamic Modelling:** Employs **MICOM** and **parsimonious Flux Balance Analysis (pFBA)** to simulate temporal dynamics and syntrophic interactions.

## 📂 Repository Structure

```text
├── data/
│   ├── raw_counts/          # Metagenomic count tables
│   ├── metabolomics/        # LC-MS/MS untargeted profiling data
│   └── taxonomy/            # GTDB-Tk classification results
├── models/
│   ├── gems_individual/     # Individual GEMs (SBML) reconstructed via ModelSEED
│   └── community_models/    # MICOM community models for Bovine and WTP inocula
├── scripts/
│   ├── reconstruction/      # Python scripts for genome mapping and model building
│   ├── gapfilling/          # Custom scripts for metabolomics-guided curation
│   └── simulation/          # Flux analysis and ecological interaction inference (MICOM)
├── docs/
│   └── figures/             # Supplementary figures and the graphical abstract
└── results/
    ├── flux_distributions/  # Predicted metabolic fluxes (csv)
    └── growth_rates/        # Inferenced microbial growth rates
