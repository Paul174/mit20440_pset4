---
title: "MIT 20.440 final project"
author: "Paul Kramer y Rosado"
output: html_document
bibliography: ["references.bib"]
csl: ama.csl
---


# MIT 20.440 final project
 - Title: **Metabolic Modeling of Cyanobacteria for Evolutionary Inference**
 - Authors: **Dylan Hirsch, Paul Kramer y Rosado**
## Overview
This directory contains version-controlled information about our final project for the MIT subject 20.440 (Analysis of Biological Networks). The project aims to model the metabolism of cyanobacteria in different environmental conditions in order to understand the evolution of their metabolism, and also their fitness in different environments. In order to do this, we will analyze the flux distributions using flux balance analysis (FBA) [Orth] and flux variability analysis (FVA) [Mahadevan] using the the constraint-based reconstruction and analysis (COBRA) package in python [Ebrahim].


## Data

Our main source of data is the available genome-scale metabolic model of Synechocystis sp. PCC 6803 [Joshi] from BiGG Models [King]. This model contains information about the metabolic reactions of this organism, with the metabolites stoichiometry, lower and upper bounds on reaction fluxes and additional information about the reactions.

## Repository Structure

The repository is organized in a main directory containing:
 - Basic git configuration files such as `.gitattributes` and `.gitignore`.
 - It also contains the `requirements.yml` file, which lists the package dependencies and allows to create a virtual environment.
 - The `README.md` file, with the description and information about the project and repository.
 - File containg the references (`references.bib`) and the citation style file (`ama.csl`).
    
In addition, there are two additional subdirectories:
 - The `data` subdirectories: contains the genome-scale metabolic model data. It will have additional data files if we need them for our project.
 - The `notebook` subdirectories: it has the jupyter notebook and a subdirectory called `figures`, with the figures generated by the notebook.


## Installation

To reproduce the results, you can download the contents of this repository by running:
``` bash
git clone https://github.com/Paul174/mit20440_pset4.git
```

To run the code, Anaconda needs to be installed. The dependencies are listed on the `requirements.yml` file. It is recommended to create a virtual environment using Anaconda and the .yml file provided.
```bash
conda env create -n <env_name> -f requirements.yml
```
Then activate the environment:
```bash
conda activate -n <env_name>
```
Then, you can run jupyter notebook and open the notebook on the \notebook folder:
```bash
jupyter notebook
```


## References

[Ebrahim] Ebrahim, Ali, et al. "COBRApy: constraints-based reconstruction and analysis for python." BMC systems biology 7.1 (2013): 1-6.

[Joshi] Joshi, Chintan J., Christie AM Peebles, and Ashok Prasad. "Modeling and analysis of flux distribution and bioproduct formation in Synechocystis sp. PCC 6803 using a new genome-scale metabolic reconstruction." Algal research 27 (2017): 295-310.

[King] King ZA, Lu JS, Dräger A, Miller PC, Federowicz S, Lerman JA, Ebrahim A, Palsson BO, and Lewis NE. BiGG Models: A platform for integrating, standardizing, and sharing genome-scale models (2016) Nucleic Acids Research 44(D1):D515-D522.

[Mahadevan] Mahadevan, R., and C. H. Schilling. "The effects of alternate optimal solutions in constraint-based genome-scale metabolic models." Metabolic engineering 5.4 (2003): 264-276.

[Orth] Orth, Jeffrey D., Ines Thiele, and Bernhard Ø. Palsson. "What is flux balance analysis?." Nature biotechnology 28.3 (2010): 245-248.
