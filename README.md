# Drug-Target Interaction (DTI) Prediction using GNNs

## Project Overview
Predicting the binding affinity between drug molecules and protein targets is a fundamental challenge in AI-driven drug discovery. This project implements a **Graph Neural Network (GNN)** to process molecular structures directly from SMILES strings, treating atoms as nodes and chemical bonds as edges. This approach allows the model to learn structural fingerprints without manual feature engineering.

## Technical Approach
1. **Featurization:** Utilized **RDKit** to convert SMILES strings into graph representations (Adjacency Matrices + Node Feature vectors based on atom type).
2. **Architecture:** Implemented a custom Message-Passing GNN in **PyTorch**. The model aggregates atomic features across the molecular graph to learn a latent representation of the molecule.
3. **Learning Task:** Trained on a regression task to predict Binding Affinity (pKd) scores.

## Key Technologies
- **Python**
- **RDKit** (Cheminformatics & Graph Generation)
- **PyTorch** (Deep Learning & Autograd)
- **Graph Theory** (Adjacency Matrices)

## Usage
Run the `Drug_Target_Interaction_GNN.ipynb` notebook to see the end-to-end pipeline, from SMILES input to affinity prediction.
