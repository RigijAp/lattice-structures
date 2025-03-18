# Properties of lattice structure

All the scripts are prepared for the cubic cells with a = 10 mm. The size od a single cell and material (material's properties) can be changed.

## Homogenization for lattice structures
To obtain the homogenisies properties for a single lattice cell, run the MatLab script *homogenization.m* from COMSOL 6.2 or higher. The input are material's properties such as Poisson's ratio, Young's modulus, density (now for TC4) and the geometry at *.stp/.step* format. As output we have elasticity tensor, complience tensor, density, volume.

For plasticity properties of a single cell structure, run the MatLab script *stress-strain curve for a single cell.m* from COMSOL 6.2 or higher. The input are material's properties such as Poisson's ratio, Young's modulus, density, plasticity curve  (now for TC4) and the geometry at *.stp/.step* format. As output we have values of stresses, strains, z-component react forces.

Both of scripts can be used as function to make a stream calculation.

## Prediction of stress-strain curves from geometry (.stl format) 
At the first step it is necessary to parce the images from .stl format to coordinates of nodes, adjection matrix, vectors. For this purpose use Python notebook *parcer.ipynb*. As input we have *.stl* file, as output adkection matix, nodes coordinates and connections.

A script *DNN.ipynb* is needed to train a convolution neural network. At the firts step thecodes allows to decrease the dimention, and then prepare the prediction with CNN.
