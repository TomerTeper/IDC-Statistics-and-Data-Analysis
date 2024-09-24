
# Homework 3: Statistics and Data Analysis - Differential Gene Expression in Acute Myocardial Infarction

## Overview
This assignment delves into the analysis of gene expression profiles to compare the circulating endothelial cells (CECs) from patients with acute myocardial infarction (AMI) against those of healthy individuals. The focus is on identifying **differentially expressed genes (DEGs)** using statistical tests like the **Wilcoxon Rank-Sum (WRS)** test and **Student’s t-test**. The workflow includes data pre-processing, applying DE tests, and performing advanced correlation analysis, ultimately culminating in a visualization of significant genes.

## Dataset
The dataset used in this analysis is derived from two major sources:
1. **NCBI GEO Database**: [GSE66360](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE66360)
2. **Research Paper**: Muse et al., Sci Rep 2017, [Published Study](https://www.nature.com/articles/s41598-017-12166-0)

The provided dataset is a CSV file that contains gene expression data. The dataset includes metadata and expression values, where the samples are categorized into two classes: 
- **H (Healthy)**: Control samples.
- **M (Myocardial Infarction)**: Samples from patients with AMI.

## Key Topics Covered
- Data pre-processing and cleaning
- Wilcoxon Rank-Sum Test (WRS) for differential expression
- Student’s t-test for gene expression comparison
- Boxplot visualization for gene expressions
- Spearman ρ correlation analysis
- Differential expression overabundance plots
- Robust Differentially Expressed Genes (RDEG) analysis
- Heatmap generation for gene expression patterns

## Questions Overview

1. **Data Pre-processing**:
   - **Data Cleaning**: The raw CSV file contains metadata that is removed before further analysis. The file's first 59 rows contain irrelevant information, which are dropped to retain the core expression data and sample labels.
   - **Missing Values**: Rows (genes) with any missing values are completely removed from the dataset to ensure accurate analysis.
   - **Numeric Conversion**: Helper functions are used to convert non-numeric data (e.g., sample labels) into a numeric format suitable for statistical analysis.
   
   After pre-processing, the dataset is ready for DE and correlation analysis.

2. **Exploratory Data Analysis**:
   - **Basic Descriptive Statistics**: You are required to answer fundamental questions about the dataset, such as:
     - Total number of genes profiled.
     - Total number of samples.
     - Number of samples in each class (H vs. M).
   - **Visualization**: Select 20 random genes and generate pair boxplots comparing their expression levels across the two sample classes (healthy vs. AMI). This helps in visualizing the differences between the gene expressions in the two groups.

3. **Differential Expression Analysis**:
   - **Wilcoxon Rank-Sum Test (WRS)**:
     - This test is used to determine if there is significant differential expression (DE) between the two classes (H vs. M) for each gene. You calculate the sum of ranks for expression values for samples labeled M and compare them against the expected null model.
     - **Expected Values**: Calculate and explain the expected sum of ranks and probabilities for different values under the null hypothesis of no DE.
     - **DE Histograms**: Generate a histogram of the rank-sum values (RS) for all genes after data cleaning and present key statistics like the interquartile range (IQR) to visualize the spread of the data.

   - **Student’s t-test**:
     - Perform a t-test to evaluate DE in both one-sided directions for each gene (overexpression in M vs. underexpression in M) at a significance threshold (p-value ≤ 0.07). Use both the WRS test and t-test for a comparative analysis.

4. **Correlation Analysis**:
   - **Gene Correlations**:
     - Select the 80 most significant genes from each one-sided WRS DE analysis and create a union of these to form a dataset with 160 genes (denoted as D).
     - **Spearman ρ Correlations**: Compute the pairwise Spearman correlation coefficients for all genes in D and represent these correlations in a 160x160 heatmap.
     - Analyze the average correlation and compare it with values under a null model assumption (pairwise independence).
     - **Co-expression Analysis**: Report on co-expression patterns observed among genes, and estimate the number of co-expressed gene pairs at an FDR threshold of 0.05.

5. **DE Overabundance Plots**:
   - Construct overabundance plots for genes showing overexpression in AMI vs. healthy controls (M > H). 
   - Apply both the WRS test and Student’s t-test to generate overabundance plots at different FDR thresholds (τ = 0.05, 0.01, 0.005) and report the number of significant genes identified.

6. **Robust Differentially Expressed Genes (RDEG)**:
   - **Label Swap Error Analysis**:
     - Compute the maximum possible p-values (𝑝!(g)) for each gene after simulating labeling errors and re-running the analysis with FDR set at 𝜏 = 0.05. This provides a list of robust DEGs.
     - Compare the robust DEG list with the original list and analyze the overlap.

7. **Final Reporting and Visualization**:
   - **Visualization of DE Genes**: Select three differentially expressed genes from D and generate plots to graphically demonstrate the observed DE.
   - **Heatmap**: Draw a heatmap representation of the expression values for genes in D, across all samples (both H and M). Use hierarchical clustering or another technique to maximize visual clarity and interpretation.

## References:
- Dataset: [GSE66360](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE66360)
- Muse et al., Sci Rep 2017: [Published Study](https://www.nature.com/articles/s41598-017-12166-0)
