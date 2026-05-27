Cytometry Analysis in R

Flow and mass cytometry analysis in R using the Bioconductor ecosystem — flowCore, CATALYST, and diffcyt workflows for differential discovery in high-dimensional cytometry data.

Status:
In active development. This repository is being built throughout 2026 as part of a computational immunology portfolio. Sections are added as the corresponding skills are developed across a 12-week Python + R learning plan. Target completion: August-September 2026.
Until then, this README serves as a planning document for the project's scope and structure. Code, notebooks, and figures will be added as each stage of the analysis is completed.

Project Goal:
To execute a complete differential-discovery cytometry workflow in R, applied to a public CyTOF or spectral flow dataset, following the methodology established by Nowicka et al. (F1000Research) and the CATALYST framework. The output will be a fully reproducible RMarkdown report.

Planned Pipeline:
- Data ingestion — flowCore::read.FCS() and conversion to SingleCellExperiment
- Quality control — diagnostic plots, sample- and channel-level QC
- Transformation — arcsinh with cofactor selection appropriate to the data
- Clustering — FlowSOM with ConsensusClusterPlus metaclustering
- Cluster annotation — manual merging informed by marker expression
- Dimensionality reduction — UMAP for visualization
- Differential abundance — diffcyt-DA-edgeR
- Differential state — diffcyt-DS-limma for cluster-level marker expression
- Reporting — RMarkdown rendered to HTML, hosted via GitHub Pages

Tools:
R 4.4+, Bioconductor 3.20+, flowCore, CATALYST, diffcyt, FlowSOM, ConsensusClusterPlus, SingleCellExperiment, ggplot2, pheatmap. Dependencies will be managed via renv and documented in renv.lock.

Reproducibility:
When complete, this repository will include:
- A data download script
- The renv.lock file for exact package version reproduction
- A single RMarkdown source file that renders the full report
- The rendered HTML report linked from this README

Background: 
I work as a Resource Technologist at the University of Pennsylvania's Institute for Immunology and Immune Health. This portfolio represents independent computational work undertaken in preparation for graduate study in molecular biotechnology.

See also: 

cytometry-python ; 
integrated-cytometry-analysis ; 
python-r-fundamentals

License: 
MIT — see LICENSE file.
