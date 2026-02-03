# Graph Neural Network for Molecular Property Prediction

![PyTorch Geometric](https://img.shields.io/badge/PyTorch_Geometric-Deep_Learning-red)
![RDKit](https://img.shields.io/badge/RDKit-Cheminformatics-blue)

## 🧬 Project Overview
This project implements a **Graph Neural Network (GNN)** to predict molecular properties directly from chemical structures (SMILES). By representing molecules as graphs—where atoms are nodes and bonds are edges—the model captures the topological structure of drugs better than traditional string-based methods.

## ⚙️ Methodology
1.  **Data Processing:** * Used **RDKit** to parse SMILES strings.
    * Converted molecules into **Undirected Graphs**.
    * Node Features: Atomic Numbers.
    * Edge Features: Connectivity (Adjacency List).
2.  **Model Architecture:**
    * **3x GCNConv Layers:** To perform message passing and aggregate local chemical environments.
    * **Global Mean Pooling:** To generate a fixed-size molecular fingerprint from variable-sized graphs.
    * **Linear Output:** To regress the final property score.
3.  **Dataset:** * Utilized the **ESOL (Delaney)** benchmark dataset to train and validate the graph topology extraction pipeline.

## 🚀 How to Run
1.  Install dependencies: `pip install torch torch_geometric rdkit-pypi pandas`
2.  Run `Drug_Interaction_GNN.ipynb`
