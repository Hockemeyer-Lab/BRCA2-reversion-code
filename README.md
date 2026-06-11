# BRCA2 Reversion Analysis

This repository contains custom analysis scripts used to process CRISPResso2 output files, calculate allele and sgRNA frequencies, compute log2 fold changes, and generate figures for the study:

**Decoding the BRCA2 reversion principles underlying PARP inhibitor resistance**

## Overview
The scripts in this repository were used for:

- Quantification of allele frequencies from CRISPResso2 output
- Classification of alleles as frameshift, in-frame, wild-type, compound frameshift, or reversion.
- Calculation of normalized allele frequencies and log2 fold changes across treatment conditions.
- Analysis of sgRNA enrichment from pooled BRCA2 sgRNA library screens. 
- Analysis of HDR-based reversion experiments in BRCA2 exons 5, 17 and 20
- Visualization of allele-frequency, sgRNA-frequency and reversion-enrichment data

## Repository contents

Example analysis notebooks include:

| File | Description |
|---|---|
| `BRCA2_sgRNA_frequency_analysis.ipynb` | Analysis of sgRNA frequencies from pooled CRISPR libraries |
| `Reversion_allele_frequency_analysis.ipynb` | Processing and visualization of reversion allele frequencies (with p.I80Yfs5 frameshift mutant used an example) |
| `HDR_Exon_5_frequency_analysis.ipynb` | HDR-designed reversion analysis for BRCA2 exon 5 |
| `HDR_Exon_17_frequency_analysis.ipynb` | HDR-designed reversion analysis for BRCA2 exon 17 |
| `HDR_Exon_20_frequency_analysis.ipynb` | HDR-designed reversion analysis for BRCA2 exon 20 |

Each notebook includes the corresponding example input and output files. The CRISPResso data in the example input files is representative but may vary in the number of technical sequencing replicates for brevity. The example input data has been significantly shortened to reduce runtime, which will vary with the number of samples and the experiment's sequencing depth. Specific instructions for each analysis are provided in the notebook.

The input DNA/protein sequences in the `Reversion_allele_frequency_analysis.ipynb` script vary by experiment. For reproducibility, additional details are available in the `BRCA2_reversion_analysis_amplicon_details.xlsx` file.

## Software and package versions

Sequencing reads were processed using **CRISPResso2 v2.2.11** and **CRISPRessoBatch v2.2.11**. Downstream analyses were performed in **Python v3.9.15**.

The main Python packages used for allele-frequency analysis, sgRNA-frequency analysis, statistical testing and plotting were:

| Software/package | Version |
|---|---:|
| Python | 3.9.15 |
| CRISPResso2 | 2.2.11 |
| CRISPRessoBatch | 2.2.11 |
| NumPy | 1.23.5 |
| pandas | 1.5.2 |
| SciPy | 1.9.3 |
| Matplotlib | 3.6.2 |
| seaborn | 0.12.2 |
| Biopython | 1.81 |

Python libraries used in the analysis included:

```text
__future__
itertools
re
functools
pathlib
os
glob
