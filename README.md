# MLinQCbook22-KMP
This case study is from a book chapter by Yi-Fan Hou and Pavlo O. Dral. Kernel method potentials. In Quantum Chemistry in the Age of Machine Learning, Pavlo O. Dral, Ed. Elsevier: 2023. DOI: 10.1016/B978-0-323-90049-2.00020-2.

## Calculations on the cloud 
For this case study, you do not need to install anything and can run calculations on the MLatom@XACS cloud (http://XACScloud.com). If you want to run calculations locally, please see the instructions below.

When you run calculations on the cloud, you need to run two jobs:
1. Training of the KREG model, which requires train.inp input file and auxiliary files with data: xyz.dat (with XYZ geometries) and E_FCI_451.dat (FCI energies). The calculations will generate for you the ML model file energies.unf.
2. Optimization of the H2 geometry with the trained KREG model can be performed with the opt.inp input file and it requires two auxiliary files: the initial guess of geometry (eq.xyz file is provided) and the trained model from the previous step (you can also use the pre-trained model).

## Local calculations
This case study was performed with MLatom 2.1.0 package which can be downloaded, installed, and used as described in http://MLatom.com 

A quick way to install: 
```bash 
python3 -m pip install MLatom==2.1.0 
```

This version works only on Linux.  
Example of training the KREG model with MLatom: 
```bash
[path to MLatom]/MLatom.py train.inp > train.out 
``` 

You can compare whether this train.out file is similar to the one in this repository. 

Geometry optimization can be performed in a similar way:  
```bash 
[path to MLatom]/MLatom.py opt.inp > opt.out 
```

The file with the optimized geometry is saved to xyz_temp.dat for this version of MLatom, but it may vary in future releases (see documentation).  
