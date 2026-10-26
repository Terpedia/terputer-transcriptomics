# Terputer transcriptomics

A standalone study package for descriptive analyses of terpene-exposure RNA-seq and a separate genetic Perturb-seq context comparison. This study does **not** establish a reproducible universal terpene response or target-specific mechanism.

## Question

Which metabolic and signaling responses to terpene exposure are reproducible, and which depend on cellular context or a specific target?

## Run the notebook

Create the conda environment with `conda env create -f environment.yml`, activate it, then run `jupyter lab notebooks/analysis.ipynb`. The notebook reads the checked-in inputs in `data/` and outputs under `results/`.

## Repository map

- `notebooks/analysis.ipynb` — executable analysis record.
- `whitepaper/white-paper.md` — methods and results, with evidence boundaries.
- `whitepaper/critical-review.md` — review findings and release caveats.
- `data/manifest.tsv` — source and checksum manifest.
- `data/` — compact processed source data and sample manifests.
- `results/` — derived tables and figures.

The reviewed analysis uses processed FPKM values; reported expression ratios are descriptive, not formal differential expression. Candidate cohorts in the selected-sample manifest are metadata-only. Perturb-seq comparisons are genetic perturbation evidence and remain separate from chemical exposure experiments.

A SHA-256/size inventory for bundled files is provided in [`data/manifest.tsv`](data/manifest.tsv). The frozen result bundle supports review without network access; the notebook verifies checked-in source inputs and writes its derived outputs under `results/`.
