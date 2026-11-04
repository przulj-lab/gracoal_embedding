<div align="center">

<img src="images/header02.jpg" width="100%">

# Graphlet-Based Hyperbolic Embeddings Capture Evolutionary Dynamics in Genetic Networks

**S. F. L. Windels, D. Tello Velasco, M. Rotkevich, N. Malod-Dognin and N. Pržulj**

Corresponding author: Prof. N. Pržulj, natasa.przulj@mbzuai.ac.ae

</div>

## Downloads

- [Code and data (zip)](https://github.com/przulj-lab/gracoal_embedding/releases/download/v1.0/gracoal_embedding.zip)

## Installation

To create an environment with Gracoal embedding and SAFE installed, download and unzip the archive above, then run from the project root:

```bash
conda env create -f env.yml
```

Activate the environment:

```bash
conda activate gracoal
```

Install the scripts in the local `src` directory:

```bash
pip install -e .
```

## Reproducing the experiments presented in the paper

Activate the `gracoal` environment (see above) and run:

```bash
snakemake -s Snakefile -c 1
```

The `-c 1` flag runs the pipeline on a single core.

The standard enrichment results and the enrichment results for the robustness to annotation noise experiment are stored in `results/safe/merged_results.csv` and `results/safe_noise/merged_results.csv`, respectively.

The results can be viewed with the provided Jupyter notebook, `SAFE_analysis.ipynb`.

## Running Gracoal standalone

To compute the nine Gracoal embeddings for any given graph, activate the `gracoal` environment (see above) and run:

```bash
python src/gracoal_embedding.py <path_to_edgelist> <output_prefix>
```

This outputs nine embedding files named `<output_prefix>gracoal-<graphlet>.npy`, where `graphlet` indicates the corresponding underlying graphlet adjacency.

## Reporting computational issues

If you encounter any issues while running our code, please open an issue using the **Issues** tab of this repository.

## Citation

S. F. L. Windels, D. Tello Velasco, M. Rotkevich, N. Malod-Dognin and N. Pržulj. Graphlet-based hyperbolic embeddings capture evolutionary dynamics in genetic networks. *Bioinformatics* 40(11), btae650 (2024). [PMID: 39495120](https://pubmed.ncbi.nlm.nih.gov/39495120/)
