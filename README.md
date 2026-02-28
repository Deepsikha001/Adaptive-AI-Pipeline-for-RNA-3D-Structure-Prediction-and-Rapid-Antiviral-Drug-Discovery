Adaptive AI Pipeline for RNA 3D Structure Prediction and Rapid Antiviral Drug Discovery
Case Study: SARS-CoV-2 Spike RBD (BA.1, PDB 7WBP)

Author: Deepsikha Pramanick, IIT Guwahati
Email: d.pramanick@op.iitg.ac.in

🧬 1. Overview

This repository documents a rapid computational exploration of antiviral candidate evaluation using:

AI-assisted molecular modeling

3D structural analysis of the SARS-CoV-2 Spike RBD

Comparative virtual screening of Remdesivir, Sotrovimab, and 10 RDKit-generated analogs

Basic drug-likeness profiling

Structural visualization

This project supports the poster submission to CARE Conference 2025, IIT Guwahati.

📁 2. Repository Contents
/data
 
 ├── 7WBP_spike_RBD.pdb          # RBD structure
 
 ├── remdesivir.sdf
 
 ├── sotrovimab_fragment.sdf     # heavy-chain variable region fragment
 
 ├── generated_molecules.sdf
 
 ├── docking_results.csv

/notebooks
 
 ├── pipeline.ipynb              # main workflow
 
 ├── visualization.ipynb
 
 ├── RDKit_generation.ipynb

/figures
 
 ├── pipeline_diagram.png
 
 ├── RBD_structure.png
 
 ├── remdesivir_docked.png
 
 ├── sotrovimab_docked.png
 
 ├── top_hits_table.png

README.md

🧪 3. Molecules Evaluated
A. FDA-approved / clinically used
Molecule	Type	Notes
Remdesivir	Small-molecule antiviral	Nucleotide analogue
Sotrovimab	Monoclonal antibody	RBD-targeting antibody
B. RDKit-Generated Novel Analogs (10 total)

Generated using SMILES-based structural diversification.
Examples:

Analog 1: CCC(NC(=O)C(CC(C)C)NC(=O)C(O)C(C)(C)C)C(=O)Nc1cc(F)c(C)cc1C(=O)O
Analog 2: CCC(C)CC(NC(=O)C(O)C(C)(C)C)C(=O)NC(C)C(=O)Nc1cc(F)c(C)cc1C(=O)O
...
Analog 10: Cc1cc(C(=O)O)c(NC(=O)C(C)NC(=O)C(CC(C)CF)NC(=O)C(O)C(C)(C)C)cc1F


These serve as original research components.

📊 4. Drug-Like Properties Calculated

The following descriptors were computed using RDKit:

Molecular Weight (MW)

LogP

H-bond donors / acceptors

TPSA

Number of rotatable bonds

Aromatic ring count

Results stored in:

/data/docking_results.csv

🖥️ 5. Virtual Screening Setup (High-Level)

Screening was performed for:

Remdesivir vs Spike RBD

Sotrovimab fragment vs Spike RBD

10 RDKit-generated analogs vs Spike RBD

⚠️ Only high-level comparative scoring was performed — no wet-lab predictions or real biological outcomes.

📉 6. Virtual Screening Outcome (High-Level Summary)
Remdesivir

Consistent interactions observed at the RBD surface.

Binding scores were uniform in the simple docking configuration.

Informative mainly for comparative purposes.

Sotrovimab fragment

Larger surface-contact region.

Better shape complementarity to RBD interface.

Provides useful contrast between small-molecule and antibody-style interactions.

Novel Analogs

All produced valid, interpretable RDKit structures.

Docking scores were narrow and non-discriminatory (expected with default box settings).

Used primarily to demonstrate AI-guided molecule generation.

🧩 7. Figures Included

RBD 3D structure

Candidate molecule structures

Interaction visualizations (py3Dmol)

Pipeline diagram

Summary table

🚀 8. How to Reproduce

Open /notebooks/pipeline.ipynb

Run cells sequentially

Replace SMILES or PDB files to test new molecules

Use py3Dmol viewer for visualization

📚 9. References

Protein Data Bank (PDB ID: 7WBP); RDKit (Landrum, 2013); AutoDock Vina (Trott & Olson, 2010); 3Dmol.js (Rego & Koes, 2015); WHO SARS-CoV-2 Variant Reports; Beigel et al., 2020 (Remdesivir); Gupta et al., 2021 (Sotrovimab).

## Acknowledgement
Diposree Pramanick, Sister;
Pradip Kumar Pramanick, Father;
Debika Pramanick, Mother;
Attitude, Atkins, Garfield, Atlantis, Arthur, Thor, Loki, Hela, Harry, Hermione, Ronald, Alexander, Atlas And all other cats and Gyangchu, Shantilaal, Kantilaal, Kanjilaal, Maganlaal, Lul, Mocha, Espresso, Butter and all other dogs and every other creature who motivate me doing this project, thank you all :)  
