# Cancer Genomics Data Analysis and Visualization Toolkit

This repository contains a suite of R scripts designed for the analysis and visualization of cancer genomics data. The scripts process pre-computed patient data tables (typically in RDS format) to generate various plots related to patient age, mutation load, principal component analysis (PCA) of methylation data, methylation feature distributions, ploidy, and correlations between different molecular features.

## Overview

The toolkit focuses on:
1.  **Age vs. Mutation Load:** Visualizing the relationship between patient age at diagnosis and tumor mutation load.
2.  **Correlation Heatmaps:** Generating heatmaps to show correlations between Principal Components (PCs) from methylation data and top mutated genes, as well as correlations among different CpG context methylation features.
3.  **Methylation Feature Boxplots:** Displaying the distribution of average methylation levels across different CpG genomic features (Islands, Shores, Shelves, OpenSea).
4.  **PCA Variance Explained:** Plotting the proportion of variance explained by the top principal components derived from methylation data.
5.  **Ploidy and Mutation Load Mixture Modeling:** Applying mixture models to ploidy and mutation load data to identify subgroups, and visualizing their relationship in panel plots. This script also updates the input patient tables with new cluster assignments.

## Prerequisites

*   **R Environment:** R (version 3.6 or later recommended).
*   **R Packages:**
    *   `data.table`
    *   `ggplot2`
    *   `corrplot`
    *   `RColorBrewer`
    *   `scales`
    *   `patchwork`
    *   `MASS`
    *   `mixtools`
*   **External Script:**
    *   `misc/multiModal.R`: A custom script required for the mixture modeling in the ploidy/mutation load analysis. Ensure this script is present in a `misc/` subdirectory relative to where you run the main ploidy script, or adjust the `source()` path accordingly.

You can install the R packages using:
```R
install.packages(c("data.table", "ggplot2", "corrplot", "RColorBrewer", "scales", "patchwork", "MASS", "mixtools"))

