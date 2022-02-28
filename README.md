# MLinQCbook22-KMP

This case study was performed with MLatom 2.1.0 package which can be downloaded, installed and used as discribed in http://MLatom.com 

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

Geomtry optization can be performed in a similar way:  
```bash 
[path to MLatom]/MLatom.py opt.inp > opt.out 
```

The file with the optimized geometry is saved to xyz_temp.dat for this version of MLatom, but it may vary in the future releases (see documentation).  
