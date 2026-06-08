# BRCA2-reversion-code
Code used to analyze allele frequencies in Horacek et al., 2026

##System requirements

1) For all analysis software use CRISPResso allele_frequency.txt files as input and ensure they are named in the following format {condition}_{biological replicate}. For example day_7_A, nira_B, mock_C.
2) Input of the number of technical PCR replicates is not required.
3) Additional inputs include an annotation file with sequence annotations for the gene of interest, along with relevant sgRNAs.
4) The reversion allele frequency analysis and specefic HDR allele frequency analysis codes require custom input sequences, including: the DNA sequence where translation should start and end (6 bp is typical, start and stop locations depend on the location of the primary frameshift mutation and sgRNA(s) used to induce edits), and both the wild-type and un-modified frameshift translated sequences. 
