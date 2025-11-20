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


## 🧬 What I Found
The cell composition of the dataset does not match what is normally seen in healthy bone marrow. In bone marrow, we expect a broad mix of developing blood lineages, including hematopoietic stem and progenitor cells, erythroid precursors, megakaryocytes, and large numbers of neutrophils. These groups are not found in the data, and instead the sample is dominated by lymphoid immune cells such as γδ T cells, NK cell populations, and other mononuclear cells. This pattern is more consistent with a PBMC-like sample rather than marrow, because peripheral blood is enriched for mature immune cells and lacks the early developmental stages that are typical of bone marrow. Based on the types of cells detected and their proportions, the tissue resembles peripheral blood immune cells rather than a bone marrow environment. Validation with reference bone marrow datasets would be needed to confirm this interpretation.

The dataset mainly contains mononuclear immune cells, similar to what we usually see in PBMC samples. We can identify a mix of innate and adaptive immune populations, including NK cells, monocytes, naïve B cells, T cells, and other lymphoid subsets. Innate immune cell populations, like, NK cells, appear more prominent than expected, which can happen when the immune system is actively responding to a stimulus. We also see changes in monocyte levels and variation in T-cell states, which are signs of cytokine signaling, antigen presentation, and early immune activation.

These observations suggest that the sample may reflect an ongoing or recent immune response. However, this interpretation is based only on the cell-type proportions. To be confident, these findings should be compared against healthy PBMC reference datasets and supported with clinical information or functional assays, since cell composition alone cannot confirm infection.


