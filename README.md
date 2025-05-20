I used my Python knowledge to analysis this data for practie. In this analysis I used sanbomics tools to get the gene symbol from enseble id.

# HBV-Induced Hepatocellular Carcinoma RNA-seq Analysis (Mouse)

## Overview

This project analyzes **RNA-seq data** from a study titled:
> 🧪 *"Hepatitis B virus promotes hepatocellular carcinoma (liver cancer) by modulating the immune response to environmental carcinogens."*

- **Data Accession**: [GSE269528](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE269528)
- 🐭 **Organism**: *Mus musculus*
- 🧫 **Samples**: 3 × HBV_DEN, 3 × Sham_DEN
- 🧬 **Platform**: Illumina HiSeq 2000
- Preprocessing and transformation of raw gene expression data
- Differential gene expression analysis (DEG)
- Volcano plot and heatmap visualizations
- Clustermap of sample relationships
- Gene set enrichment analysis (GSEA)

## 📂 Project Structure

```
├── data/               <- CSV file converted from GEO .gz
├── notebook/           <- Analysis and visualization notebook
├── results/            <- Plots are imbeded in the notebook
├── README.md           <- You're reading it
├── requirements.txt    <- Python dependencies, sanbomics
└── .gitignore
```

## ⚙️ Tools and Libraries

- Python 3.8+
- `pandas`, `numpy`, `matplotlib`, `seaborn`
- `scipy`, `statsmodels`, `sklearn`
- `gseapy` (for GSEA analysis)
- `scanpy` or `anndata` (optional for large matrix support)
-  `sanbomics`

  ## 🔬 Methods

1. **Data Import and Cleaning**
   - Raw count or FPKM values were downloaded from GEO
   - Converted `.gz` format into CSV or DataFrame for analysis

2. **Metadata Preparation**
   - Samples were grouped into **experimental** (e.g., `HBV_DEN`) and **control** (`sham_DEN`) conditions

3. **Differential Expression Analysis**
   - Used `log2 fold change` and `adjusted p-values` to identify DEGs
   - Applied filters: FDR < 0.05, |log2FC| > 1

4. **Visualization**
   - **Volcano plot**: Highlighted up- and downregulated genes
   - **Heatmap**: Displayed expression patterns of top DEGs
   - **Clustermap**: Sample-level clustering

5. **Enrichment Analysis**
   - GSEA was performed using `gseapy` with `GO_Biological_Process_2021`
   - Top pathways visualized with enrichment plots

   

6. ## 🛠️ How to Run

```bash
# Create a virtual environment
python3 -m venv env
source env/bin/activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```

## 📜 Citation

**Contributors**: Park J, Huang M  
**Contact**: sdemehri1@mgh.harvard.edu  
**Affiliation**: Harvard Medical School# RNA-Seq_Analysis
HBV-Induced Hepatocellular Carcinoma RNA-seq Analysis (Mouse)
