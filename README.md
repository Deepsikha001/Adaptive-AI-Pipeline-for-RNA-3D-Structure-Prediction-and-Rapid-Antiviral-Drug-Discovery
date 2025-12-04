# Adaptive-AI-Pipeline-for-RNA-3D-Structure-Prediction-and-Rapid-Antiviral-Drug-Discovery
Code Structure Plan 
Adaptive AI Pipeline for RNA 3D Structure Prediction and Rapid Antiviral Drug Discovery
Case Study on SARS-CoV-2 Spike RBD (PDB: 7WBP)

Author: Deepsikha Pramanick, IIT Guwahati
Contact: d.pramanick@op.iitg.ac.in
## Overview

This repository contains the computational workflow, datasets, molecules, structures, and figures used for a rapid antiviral-design pilot study for the CARE Conference 2025 poster presentation.

The goal of the project was to develop an adaptive AI pipeline that can:

Predict RNA/protein structures

Generate new molecular analogs

Evaluate biochemical properties

Perform fast docking

Produce interpretable, presentable scientific outputs within 48 hours

## Project Workflow
SARS-CoV-2 RBD → Structure Preparation → RDKit Molecule Generation
→ QSAR Features → AutoDock Vina Screening → Ranking + Visualization

## Target Used

Protein: SARS-CoV-2 Omicron BA.1 Spike RBD

PDB ID: 7WBP

This region was chosen for:

Biological relevance (ACE2 receptor binding)

Ideal size for computational docking

High-quality resolved structure

## New Molecules Generated

10 Remdesivir-based analogs were generated via RDKit
(chemically valid & unique)

Example:

Analog 1: CCC(NC(=O)C(CC(C)C)NC(=O)C(O)C(C)(C)C)C(=O)Nc1cc(F)c(C)cc1C(=O)O
Analog 2: CCC(C)CC(NC(=O)C(O)C(C)(C)C)C(=O)NC(C)C(=O)Nc1cc(F)c(C)cc1C(=O)O
...
Analog 10: Cc1cc(C(=O)O)c(NC(=O)C(C)NC(=O)C(CC(C)CF)NC(=O)C(O)C(C)(C)C)cc1F


All SMILES included in the /molecules/ folder.

## Computed QSAR-Style Properties

For each analog:

Molecular Weight

LogP

H-bond Donors

H-bond Acceptors

TPSA

Rotatable Bonds

Aromatic Rings

(See: results/properties.csv)

## Docking Method

Software: AutoDock Vina

Grid: Centered on Spike RBD binding surface

Result:
Docking scores for all analogs fell in the 0.0 to –0.1 kcal/mol range → indicating:

✔ Binding box likely too large
✔ Uniformly neutral scoring
✔ Screening workflow functional but requires refinement

## Visualizations

RBD 3D model

Molecule overlays

py3Dmol renders

Pipeline diagram (BioRender)

Available inside /figures/

## Repository Structure
├── data/
│   ├── 7WBP.pdb
│   └── sequences/
├── molecules/
│   ├── analog_1.sdf
│   └── analog_10.sdf
├── results/
│   ├── docking_scores.csv
│   └── properties.csv
├── figures/
│   ├── rbd_view.png
│   ├── docking_visualization.png
│   └── pipeline.png
├── notebook/
│   └── antiviral_pipeline.ipynb
└── README.md

## Citation

If you use this workflow, please cite the project poster.
