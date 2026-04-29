# SHM_in_the_act

A comprehensive bioinformatics analysis pipeline for single-cell Somatic Hypermutation (scSHM) characterization in lymphoid malignancies and follicular lymphoma.

## Project Overview

This repository contains a series of Jupyter Notebook-based analyses for studying somatic hypermutation events in single-cell RNA sequencing data. The project focuses on characterizing SHM dynamics across different disease contexts including:

- **CLL/MBL** - Chronic Lymphocytic Leukemia / Monoclonal B-cell Lymphocytosis samples
- **FL (K123)** - Follicular Lymphoma dataset K123
- **FL (K45678)** - Follicular Lymphoma dataset K45678

## Repository Structure

### Core Analysis Notebooks

#### Stage 1: scSHM Classification
- `01_scSHM_CLL_MBL_v0.8.ipynb` - scSHM analysis for CLL/MBL samples
- `01_scSHM_FL_K123_v2.ipynb` - scSHM analysis for FL K123 dataset
- `01_scSHM_FL_K45678_v6.ipynb` - scSHM analysis for FL K45678 dataset

#### Stage 2: Expression Analysis
- `02_Expression_analysis_CLL.MBL_v0.5.ipynb` - Gene expression profiling for CLL/MBL
- `02_Expression_analysis_K45678_v2.ipynb` - Gene expression profiling for FL K45678
- `Expression_analysis_K123_v2.3.ipynb` - Gene expression profiling for FL K123

#### Stage 3: Quality Control
- `03_Doublet_analysis_CLL_MBL.ipynb` - Doublet detection in CLL/MBL samples
- `03_Doublet_analysis_K123_v1.ipynb` - Doublet detection in FL K123
- `03_Doublet_analysis_K45678B.ipynb` - Doublet detection in FL K45678

#### Stage 4: Differential Expression Analysis
- `04_Diferential_expression_analysis_K7B_S10000.ipynb` - DE analysis for K7B sample
- `04_Diferential_expression_analysis_K8B_S13553.ipynb` - DE analysis for K8B sample
- `05_Diferential_expression_analysis_v2.ipynb` - Comprehensive DE analysis (v2)
- `05_Diferential_expression_analysis_v3.ipynb` - Comprehensive DE analysis (v3)
- `05_Diferential_expression_analysis_v3.1.ipynb` - Comprehensive DE analysis (v3.1)

#### Stage 5: Integration & Advanced Analyses
- `05_Expression_analysis_Integration.ipynb` - Multi-dataset integration
- `05_Expression_analysis_Integration_v1.ipynb` - Integration analysis (v1)
- `05_Expression_analysis_Integration_v2.ipynb` - Integration analysis (v2)
- `05_Integration_scSHM_events_v2.ipynb` - SHM event integration analysis
- `06_Final_integracion_mice_data.ipynb` - Final integration with mouse data

#### Specialized Analyses
- `Cell-Cycle Scoring and Regression.ipynb` - Cell cycle phase annotation
- `Cell-Cycle Scoring and Regression_v1.ipynb` - Cell cycle analysis (v1)
- `1.cell_cycle_FL.ipynb` - Cell cycle analysis for FL samples
- `seurat_protocol.ipynb` - Seurat-based analysis protocol
- `RNA_velocity_analysis_python.ipynb` - RNA velocity trajectory analysis
- `Spliced_unspliced_analysis.ipynb` - Splicing kinetics analysis
- `Intron_analysis_v1.ipynb` - Intron-level analysis (v1)
- `Intron_analysis_v2.ipynb` - Intron-level analysis (v2)

#### Visualization & Reporting
- `Figures_v1.ipynb` - Publication-quality figure generation
- `scSHM_plot.ipynb` - SHM visualization plots
- `scSHM_and_WILLOW.ipynb` - Integration with WILLOW tool
- `master_table_v*.ipynb` - Master data table compilation (multiple versions)
- `Metrics.ipynb` - Quality metrics and statistics
- `mean_depth.ipynb` - Sequencing depth analysis
- `umi_count_proportion.ipynb` - UMI count distribution analysis
- `pathfindR.ipynb` - Pathway enrichment analysis
- `para_diego.ipynb` - Collaborative analysis notebook

### Data Files

#### Input/Output Data
- `summarized_data.csv` - Summarized analysis results
- `summarized_data_order.csv` - Ordered summary data
- `final_output.csv` - Final compiled results
- `cell_positives.csv` - Cell positivity information
- `cellularYieldLong.xlsx` - Cellular yield metrics

#### Pathway & Functional Analysis
- `df_combinations.csv` - Gene combination data
- `df_hsa04010.csv` - KEGG pathway: Mapk signaling pathway
- `df_hsa04068.csv` - KEGG pathway: FoxO signaling pathway
- `df_hsa04110.csv` - KEGG pathway: Cell cycle
- `df_hsa04218.csv` - KEGG pathway: Immune response
- `df_hsa05210.csv` - KEGG pathway: Colorectal cancer

#### Visualization Files
- `master_table.html` - Interactive data table visualization
- `hsa*.png` / `hsa*.pathview.png` - KEGG pathway visualizations
- `hsa*.xml` - KEGG pathway data files

### Configuration & Metadata
- `.dvc/` - DVC (Data Version Control) directory
- `.gitignore` - Git ignore rules
- `archive.dvc`, `input.dvc`, `output.dvc`, `event_plotting.dvc`, `foldchanges.rds.dvc`, `rna_velocity.dvc` - DVC tracked files

## Key Technologies & Tools

- **Python** - Primary analysis language
- **Jupyter Notebooks** - Interactive analysis and documentation
- **Seurat** - R/Python toolkit for scRNA-seq analysis
- **Scanpy** - Python library for scRNA-seq analysis
- **scVelo** - RNA velocity analysis
- **Pathway Analysis** - KEGG pathway enrichment and visualization
- **DVC** - Data Version Control for managing large datasets
- **R/ggplot2** - Statistical visualizations (via RMarkdown files)

## Data Management

Large data files are tracked using **DVC (Data Version Control)**. The `.dvc` files reference external data storage. To access the complete datasets, ensure you have DVC configured and can access the remote storage.

## Analysis Workflow Summary

1. **Quality Control** - Initial scRNA-seq data processing and filtering
2. **Normalization & Integration** - Expression normalization and multi-sample integration
3. **Cell Cycle Analysis** - Cell cycle phase assignment and regression
4. **Doublet Detection** - Identification and removal of doublets
5. **scSHM Classification** - SHM event identification and characterization
6. **Expression Profiling** - Gene expression analysis and annotation
7. **Differential Expression** - Between-group expression comparison
8. **Pathway Enrichment** - Functional annotation of findings
9. **Integration** - Cross-dataset analysis and comparison
10. **Visualization** - Publication-quality figure generation

## Output & Results

- Interactive data tables (HTML format)
- KEGG pathway visualizations with expression overlays
- Statistical summaries and metrics
- Expression matrices and metadata tables
- RNA velocity vectors and trajectory plots

## Requirements

This project requires:
- Python 3.7+
- Jupyter Notebook
- Key Python packages: scanpy, seurat, scvelo, pandas, numpy, matplotlib, seaborn
- R (for Seurat and pathway analysis components)
- DVC (for data retrieval)

## Usage

1. Clone this repository
2. Install DVC and configure remote storage access
3. Run `dvc pull` to retrieve large data files
4. Open and execute Jupyter Notebooks in sequential order
5. Results will be generated in corresponding output directories

## License

Please check repository settings for license information.

## Contact

For questions about this analysis, please contact the repository owner.

---

**Repository Language:** Jupyter Notebook  
**Last Updated:** 2026-04-29  
**Size:** ~32 MB
