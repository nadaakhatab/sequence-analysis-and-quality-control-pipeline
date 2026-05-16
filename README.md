A complete bioinformatics preprocessing workflow implemented in Python using Google Colab.

---

## Project Overview

This notebook demonstrates essential bioinformatics preprocessing techniques commonly used in genomics and transcriptomics workflows.

The project includes:

- FASTA sequence parsing
- FASTQ quality inspection
- Read filtering
- 3′ end trimming
- Missing value imputation using KNN
- Quality control visualization

This assignment was developed as part of the Bioinformatics Programming course.

---

## Technologies Used

- Python 3
- Biopython
- Pandas
- NumPy
- scikit-learn
- Matplotlib
- Google Colab

---

## Input Files

Upload the following files before running the notebook:

| File Name | Description |
|---|---|
| `sample_sequences.fasta` | DNA sequences in FASTA format |
| `sample_reads.fastq` | Sequencing reads with quality scores |
| `expression_matrix.csv` | Gene expression matrix containing missing values |

---

## Workflow Summary

### 1. FASTA Parsing

The notebook:
- Reads DNA sequences using Biopython
- Calculates:
  - Sequence length
  - GC content
  - First 20 bases
- Exports the results to:
  - `fasta_summary.csv`

---

### 2. FASTQ Quality Inspection

The notebook analyzes:
- Total number of reads
- Read length distribution
- Average Phred quality scores
- Overall sequencing quality statistics

---

### 3. Read Filtering

Reads are removed if:
- Average Phred score < 20
- Read length < 50 bp

This improves the quality and reliability of downstream analysis.

---

### 4. 3′ End Trimming

Low-quality bases are trimmed from the end of sequencing reads using a quality threshold of Q20.

This simulates standard preprocessing steps commonly used in sequencing pipelines.

---

### 5. KNN Imputation

Missing values in the expression matrix are filled using:
- `KNNImputer(n_neighbors=5)`

The cleaned matrix is exported as:
- `expression_matrix_imputed.csv`

---

### 6. Visualization

The notebook generates:
- Histogram of read lengths
- Histogram of average quality scores
- Read filtering summary chart
- Missing values comparison chart

Plots are saved as:
- `qc_summary_plots.png`

---

## Output Files

| Output File | Description |
|---|---|
| `fasta_summary.csv` | FASTA sequence statistics |
| `expression_matrix_imputed.csv` | Imputed expression matrix |
| `qc_summary_plots.png` | Quality control plots |

---

## Running the Notebook

### Open in Google Colab

Upload the notebook to Google Colab and run the cells sequentially.

### Install Dependencies

The notebook automatically installs Biopython:

## Concepts Covered

* FASTA and FASTQ parsing
* Phred quality score analysis
* GC content calculation
* Read preprocessing
* KNN-based missing value imputation
* Biological data visualization

---

## Educational Objectives

This project helped me practice:

* Working with biological sequence data
* Using Biopython for sequence analysis
* Building preprocessing pipelines
* Handling noisy biological datasets
* Creating scientific visualizations

---

## Author

Nada Mohamed Khatab Ibrahim
Bioinformatics Programming Practical Assignment

---

## Notes

* Designed for educational purposes
* Compatible with Google Colab
* All generated files can be downloaded directly from the notebook
