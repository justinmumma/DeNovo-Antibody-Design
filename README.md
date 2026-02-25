> Note: 
> This pipeline is still in development
> and may not be functional.

# DeNovo-Antibody-Design
De Novo antibody design for anti-fentanyl monoclonal antibodies for Pravetoni Lab UW using RFDiffusing, LigandMPNN, and AutoDock Vina / Smirna

**Core Dependencies:**
* Python >= 3.8
* PyTorch >= 1.13 (with CUDA support)
* LigandMPNN (from the Dauparas/Baker Lab repository)
* AutoDock Vina & PyMOL (for local visualization and docking)

## Quick Start / Usage
1. **Target Preparation:** Extract the `.pdb` from `/data` and ensure the small molecule parameters (fentanyl) are correctly defined.
2. **Run LigandMPNN:** Open `notebooks/LigandMPNN_Antibody_Design.ipynb` in Google Colab.
   Mount your Google Drive to ensure persistent storage of the output `.fasta` sequences.
3. **Validation:**
   Execute the AutoDock Vina script located in the notebooks folder to score the binding affinity of the newly generated sequences against the fentanyl target.

## Data Sourcing
The input target utilized in this pipeline (fentanyl_target.pdb) was extracted from the publicly available crystal structure of the HY6-F9 Fab complex (PDB ID: 7U64) published by Rodarte et al., 2023.

## Future Directions & Wet-Lab Translation
Once this pipeline is working to provide in-silico generation of candidate binders, these are ideas for next steps for this project:
* **Molecular Dynamics (MD) Simulations:** Running GROMACS/Amber to verify the stability of the fentanyl-antibody complex over time.
* **Wet-Lab Validation:** Synthesizing the top-scoring antibody candidates and testing their actual binding kinetics (Kd, Kon, Koff) using Biolayer Interferometry (BLI) or Surface Plasmon Resonance (SPR).
