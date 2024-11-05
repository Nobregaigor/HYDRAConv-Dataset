# Dataset for the paper: HYDRAConv A Novel Graph Neural Network for Finite Element Emulation in Biomechanical Modeling
 

This repository contains the dataset for the paper **"HYDRAConv: A Novel Graph Neural Network for Finite Element Emulation in Biomechanical Modeling"**. The dataset supports research on finite element analysis (FEA) emulation using graph neural networks (GNNs), especially in the context of biomechanical modeling.

## Repository Structure

The repository is organized as follows:

- **Dataset**: Contains subsets of FEA simulations, each as a `.zip` file, representing different biomechanical models or scenarios.
- **Example**: Provides a Jupyter notebook (`Example.ipynb`) that demonstrates how to run a simulation, load the results, and convert them into graph data.

## Dataset Overview

Each `.zip` file in the `Dataset` folder contains FEBio input files (`.feb` files) for FEA simulations. These files define the mesh, material properties, boundary conditions, and loading conditions, making them ready to run in FEBio. To manage storage size, only the input files are provided. By running these input files, users can generate and analyze the necessary FEA data on their own, ensuring full reproducibility of the results.

## How to Use the Dataset

1. **Clone the Repository**: Clone the repository to your local machine:
    ```bash
    git clone https://github.com/yourusername/HYDRAConv-Dataset.git
    cd HYDRAConv-Dataset
    ```

2. **Extract Dataset Subsets**: Each subset is provided as a compressed `.zip` file in the `Dataset` folder. Extract the desired subset:
    ```bash
    unzip Dataset/BEAM_2D.zip -d Dataset/BEAM_2D/
    ```

3. **Run FEBio Simulations**:
   - The extracted `.feb` files can be directly executed in FEBio to generate simulation results.
   - Each `.feb` file contains all the necessary configurations for FEA, including mesh structure, material properties, boundary conditions, and loading specifications.
   - You can run FEBio either from the command line or through the `febio_python` Python package.

4. **Process Simulation Results**:
   - After running the simulations, load the results using Python.
   - Use the `Example.ipynb` notebook to see how to process and convert FEA results into graph data suitable for GNNs with PyTorch Geometric.

## Example Notebook

The `Example.ipynb` notebook in the `Example` folder provides a step-by-step guide on how to:
- Run an FEA simulation using FEBio.
- Load and inspect simulation results.
- Convert the results into graph format using PyTorch Geometric, making them suitable for GNN applications.

This notebook serves as a helpful starting point for reproducing the results in the HYDRAConv paper or for developing new GNN-based methods for FEA emulation.

## Requirements

To use this dataset and run the example notebook, ensure you have the following Python packages installed:

- **febio_python**: Python interface for running FEBio simulations.
  - Installation: `pip install febio-python`
  - [febio_python documentation](https://github.com/Nobregaigor/febio-python)

- **torch_geometric**: Library for handling graph data, built on PyTorch, and used here to convert FEA data into graphs.
  - Installation: Follow the installation instructions for your system at the [PyTorch Geometric Documentation](https://pytorch-geometric.readthedocs.io/en/latest/index.html)
  
- **pyvista**: Library for 3D visualization, useful for inspecting FEA data.
  - Installation: `pip install pyvista`
  - [Pyvista documentation](https://docs.pyvista.org/)

**Note**: FEBio software is required to run the simulations. Visit [FEBio’s website](https://febio.org/) for installation details.


## Citation

If you use this dataset in your research, please cite the HYDRAConv paper:
