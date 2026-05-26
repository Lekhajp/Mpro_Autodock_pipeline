# Mpro_Autodock_pipeline
NumPy-automated Vina pipeline for SARS-CoV-2 Mpro. Validates -8.7 manual with -8.576 automated. Identifies GLU166/ASN142.
# NumPy-Automated Pipeline for SARS-CoV-2 Mpro Inhibitor Discovery

## Results Summary
| Method | Compound | Affinity (kcal/mol) | Key Residues |
| --- | --- |
| Manual | Sennoside B | -8.7 | Gly195, Asn133, Asp197 |
| Automated | Lead compound | -8.576 | GLU166, ASN142 |
| **Reproducibility** | | **0.124 kcal/mol** | |

## Pipeline Features
1. **PDB Parser**: Fixed-width field slicing `x=31:38, y=39:46, z=47:54` to extract coordinates
2. **Grid Box**: Auto-calculated centroid and AABB with 12 Å padding from 6LU7.pdb  
3. **Validation**: Vina run with exhaustiveness=32, RMSD 0.0 Å
4. **Analysis**: Custom PDBQT parser identifies residues within 5.0 Å of ligand

## Proof Files
- `molecular_docking.ipynb`: Full pipeline code
- Screenshots of Vina output, LigPlot+, and residue analysis included

Developed for Research Associate applications, 2024.
