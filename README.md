## Usecase of the dataset from Copy Number Variation Booklet

This repository serves as tutorial for the Copy Number Variation Booklet "Usage notes".

| Input  | Spreadsheet with the complete CNV dataset [`data/all_cnvs_table.xlsx`](data/all_cnvs_table.xlsx) |
|--------|---------------------------------------------------------------------------------------------------------|
| Output | Network and network analysis linking CNV diseases to phenotypes [`figures`](figures)  |

## Requirements
- [Conda](https://docs.conda.io/en/latest/)
- [Cytoscape](https://cytoscape.org/)

## Environment setup
```sh
conda env create -f environment.yml
```
## Run the notebook
 [`scripts/build_network.ipynb`](scripts/build_network.ipynb) 

## Results
- Disease-Phenotype network [`figures/disease_phenotype_network.png`](figures/disease_phenotype_network.png): Network output without custom styling applied.
    - Layout optimization: Different Cytoscape layouts can be further applied for better organization.
    - Manual adjustments: Nodes and edges were repositioned (i.e. dragged if overlapping) in the final figure of the submitted paper for improved clarity.
- Phenotype-based disease similarity [`figures/disease_similarity_heatmap.png`](figures/disease_similarity_heatmap.png). Diseases were clustered based on the Jaccard similarity index.
- Top shared phenotypes [`figures/top20_shared_phenotypes.png`](figures/top20_shared_phenotypes.png). Most shared phenotypes among the diseases.
