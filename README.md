# Properties of Lattice Structure 

This repository contains scripts for analyzing and predicting the properties of lattice structures. All scripts are designed for cubic cells with a default edge length of **a = 10 mm**. The size of a single cell and material properties can be customized as needed.

---

## Table of Contents
1. [Homogenization for Lattice Structures](#homogenization-for-lattice-structures)
2. [Prediction of Stress-Strain Curves from Geometry](#prediction-of-stress-strain-curves-from-geometry)
3. [Input and Output](#input-and-output)
4. [Dependencies](#dependencies)
5. [Contact](#contact)

---

## Homogenization for Lattice Structures

To obtain homogenized properties for a single lattice cell, use the following MatLab scripts:

### 1. **Elastic Properties**
Run the MatLab script `homogenization.m` in **COMSOL 6.2 or higher**.  
**Input:**  
- Material properties: Poisson's ratio, Young's modulus, density (default: TC4 material).  
- Geometry file in `.stp` or `.step` format.  

**Output:**  
- Elasticity tensor.  
- Compliance tensor.  
- Density.  
- Volume.  

### 2. **Plastic Properties**
Run the MatLab script `stress-strain curve for a single cell.m` in **COMSOL 6.2 or higher**.  
**Input:**  
- Material properties: Poisson's ratio, Young's modulus, density, plasticity curve (default: TC4 material).  
- Geometry file in `.stp` or `.step` format.  

**Output:**  
- Stress values.  
- Strain values.  
- Z-component reaction forces.  

Both scripts can be used as functions for streamlined calculations.

---

## Prediction of Stress-Strain Curves from Geometry

### Step 1: Geometry Parsing
Use the Python notebook `parcer.ipynb` to parse geometry files in `.stl` format.  
**Input:**  
- `.stl` file.  

**Output:**  
- Node coordinates.  
- Adjacency matrix.  
- Connection vectors.  

### Step 2: Deep Learning Prediction
Use the Python notebook `DNN.ipynb` to train a Convolutional Neural Network (CNN) for stress-strain curve prediction.  
**Process:**  
1. Dimensionality reduction.  
2. CNN-based prediction.  

---

## Input and Output

Below is a summary of the inputs and outputs for each script:

| Script                          | Input                                                                 | Output                                                                 |
|---------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| `homogenization.m`              | Material properties, `.stp/.step` geometry                            | Elasticity tensor, compliance tensor, density, volume                  |
| `stress-strain curve for a single cell.m` | Material properties, `.stp/.step` geometry                  | Stress, strain, Z-component reaction forces                            |
| `parcer.ipynb`                  | `.stl` file                                                          | Node coordinates, adjacency matrix, connection vectors                 |
| `DNN.ipynb`                     | Parsed data from `parcer.ipynb`                                       | Stress-strain curve prediction                                         |

---

## Dependencies

To run the scripts in this repository, ensure you have the following dependencies installed:

- **MatLab** (COMSOL 6.2 or higher).  
- **Python** (with libraries: NumPy, Pandas, TensorFlow/Keras, Matplotlib).  
- **COMSOL Multiphysics** (for running MatLab scripts).  

---

## Contact

For questions or support, feel free to reach out:  
- **Author**: Anna Step （Anna Stepashkina）
- **Email**: anna_step@zhejianglab.com  
- **GitHub**: [RigijAp](https://github.com/RigijAp)  

---
