# Reproducing a Core Single-Cell RNA-Seq Analysis Pipeline Using Scanpy

This project implements single-cell RNA-seq (scRNA-seq) analysis workflow using Scanpy, starting from raw data and ending with clustering, annotation, and biological interpretation. The goal is to reproduce the core steps used in modern scRNA-seq pipelines and interpret the resulting cellular landscape.

## 🔬 What I Did

- Installed and imported the required Python libraries

- Loaded the dataset (labeled as bone marrow) into an AnnData object

- Performed quality control (mitochondrial %, ribosomal %, gene filtering)

- Normalized, log-transformed, and identified highly variable genes

- Computed PCA, neighborhood graph, and UMAP

- Ran Leiden clustering to define cell groups

- Annotated cell types based on marker expression

- Interpreted the biological meaning of the identified clusters

🧬 What I Found

The sample is dominated by unconventional lymphoid cells (γδ T cells, Nuocytes), with reduced neutrophils, monocytes, and B cells, a pattern not typical for healthy bone marrow. Expected bone-marrow lineages such as hematopoietic stem/progenitor cells, erythroid precursors, and megakaryocytes were not observed.

The overall composition suggests the tissue is in a perturbed or activated immune state, consistent with viral infection or systemic inflammation, rather than healthy bone marrow.


