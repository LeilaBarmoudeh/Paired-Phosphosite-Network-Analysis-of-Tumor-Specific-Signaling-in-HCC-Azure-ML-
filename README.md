# Paired-Phosphosite-Network-Analysis-of-Tumor-Specific-Signaling-in-HCC-Azure-ML-
Paired phosphoproteomic network analysis framework for identifying tumor-specific signaling modules in hepatocellular carcinoma (HCC). Built using CPTAC data and Azure ML, integrating differential analysis, network modeling, kinase enrichment, and candidate phosphosite prioritization.
Using CPTAC multi-omics data and Azure Machine Learning, the workflow integrates:

Paired tumor–normal analysis
Differential phosphosite detection
Network-based signaling inference
Kinase enrichment analysis
Prioritization of candidate dark phosphosites

Technologies:
Python (pandas, numpy, scipy, networkx)
Azure Machine Learning (compute instance, notebooks)
gseapy (Enrichr)
seaborn / matplotlib

Azure Implementation:
This project was developed and executed entirely on Azure Machine Learning, using:
Compute Instance for scalable analysis
Remote execution independent of local machine
Notebook-based workflow for reproducibility

This setup enables:
handling large phosphoproteomics datasets (~18k features)
Azure Implementation

This project was developed and executed entirely on Azure Machine Learning, using:

Compute Instance for scalable analysis
Remote execution independent of local machine
Notebook-based workflow for reproducibility

This setup enables:
handling large phosphoproteomics datasets (~18k features)
long-running computations (network + bootstrap)
reproducible cloud-based pipelines

Workflow:
1. Data preprocessing
Filter sparse phosphosites
Left-censored imputation
2. Paired statistical analysis
Tumor vs normal (within-patient)
Wilcoxon signed-rank test
FDR correction
3. Differential network construction
Spearman correlation on tumor–normal differences
Threshold |ρ| ≥ 0.6
4. Module detection
Louvain community detection
5. Kinase enrichment
KEA (Enrichr via gseapy)
6. Candidate prioritization
Score = effect size × network degree

Key Results:
1. Identified tumor-specific phosphorylation changes across ~18,000 phosphosites
2. Constructed a differential phosphosite co-regulation network
3. Detected 382 signaling modules
4. Identified a CDK-dominant module (FDR < 0.01)
5. Highlighted candidate phosphosites:
ILF3 (S382)
RFC1 (S368)
NCL (S67)


Figures:
<img width="453" height="347" alt="candidates" src="https://github.com/user-attachments/assets/c4d917d6-8804-486f-b9b7-bfa87aadc5e6" />

<img width="476" height="361" alt="CDK_dominant" src="https://github.com/user-attachments/assets/63755a8a-11e0-4f56-abb0-ef887bea9227" />

<img width="446" height="323" alt="CDK_associated_phosphosite" src="https://github.com/user-attachments/assets/305a4a27-ef4d-4a08-85cc-464f8adaccf8" />

Data
Data derived from CPTAC HCC dataset

Scientific Contribution
This project introduces a paired differential network framework that:

1. reduces inter-patient variability
2. captures coordinated signaling changes
3. identifies module-level kinase regulation
4. prioritizes poorly characterized phosphosites

   Author:
   Leila Barmoudeh







long-running computations (network + bootstrap)
reproducible cloud-based pipelines
