Definitely this assignment should be my lowest graded assignment. LOL

# This is a what-to-do for folders: mod_heq & cn_heq 

## Introduction to mod_heq

**ModHeatEq.f90** % the Fortran module for calculating Heat Equation

**write2d.f90** % the Fortran code for writing output file of the results

**HeatEq.f90** % the 'Main Program' for calculating the Heat Equation (calling modules and subroutines)

**Makefile** % this is the Makefile for compiling the above three codes

**results_correct.txt** % the correct result used for comparing with the output file

**viz_results.py** % the python code used for visualization the output file

## How to compile these files
Please download all the files in this folder or clone my repository via:

$ git clone https://github.com/Yukiooooo/PHYS-5391.git

to compile these Fortran codes, please use command line via:

$ make heat.exe 

you'll get a executable heat.exe, in your command line, with:

$ ./heat.exe 

then a 'results.txt' output file is created, you can compare this data with the reference data via:

$ diff results.txt results_correct.txt or use tkdiff
  
to get the plot, in your command line via:

$ make viz or try:

$ chmod +x viz_results.py 

$ ./viz_results.py results.txt

then you'll get the finally plot of the results of Heat Equation, the .png will store inside the current directory with "Mod_HEQ.png"

## Introduction to cn_heq

**ModHeatCN.f90** % the Fortran module for calculating Heat Equation

**ModWrite2d.f90** % the Fortran code for writing output file of the results

**nmum_e10_4.f90** % the 'Main Program' for calculating the Heat Equation (calling modules and subroutines)

**Makefile** % this is the Makefile for compiling the above three codes

**results_correct_CN.txt** % the correct result used for comparing with the output file

**viz_results.py** % the python code used for visualization the output file

## How to compile these files
Please download all the SIX files in this folder or clone my repository via:

$ git clone https://github.com/Yukiooooo/PHYS-5391.git

to compile these Fortran codes, please use command line via:

$ make 

you'll get a executable heat.exe, in your command line, with:

$ ./heat.exe 

then a 'results.txt' output file is created, you can compare this data with the reference data via:

$ diff results.txt results_correct_CN.txt or use tkdiff
  
to get the plot, in your command line via:

$ make viz or try:

$ chmod +x viz_results.py 

$ ./viz_results.py results.txt

then you'll get the finally plot of the results of Heat Equation, the .png will store inside the current directory with "CN_HEQ.png"

__Some Comments__

1. To compile these Fortran codes inside cn_heq, you need to install the -llapack library, e.g.,

$ brew install lapack

2. When using Mac to run the .exe in Fortran, sometimes you need to add the path of the dynamic library since they are not in your current 
directory, in your command line via:

$ otool -L heat.exe

you'll get the path of your dynamics library, such as:

/usr/local/opt/gcc/lib/gcc/10/libgfortran.5.dylib. then add this path to your _export_

$ export DYLD_LIBRARY_PATH=/usr/local/opt/gcc/lib/gcc/10/


