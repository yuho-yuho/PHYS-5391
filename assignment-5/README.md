# This is the work space for Substorms Substorms Everywhere

## Introduction to each file
**spider.py** % the python code for downloading IMF files

**sciprog.py** % the source code for reading IMF files

**msm.py** % the python script for MSM model: find substorms

**msm_eva.py** % the python code for analyzing the substorm results

**assignment5.tex** % the Latex code for creating the report .pdf file

**dst_200301.png** % the DST figure to be inserted into the Latex code





## How to compile these files
Please download all the stuffs in this folder or clone my repository in command line via: 

$ git clone https://github.com/Yukiooooo/PHYS-5391.git

All the following steps can be achieved in command line:

__Step 0: # adding execute permission #__

You can compile all the python codes through: 

$ python *.py

Also, you can run them as scripts by adding permission via:

$ chmod +x *.py

$ ./*.py

__Step 1: # downloading IMF files #__

First, create a folder in your current directory to store the downloaded IMF files, here we name the folder as 'imf_data'

$ mkdir imf_data

$ ./spider.py

In line-76 of spider.py, you can edit your target links; In line-77 you can change the target data with keywords; In line-78 
you can change the folder name where you want to store the data. 


__Step 2: # finding substorms with MSM #__

$ ./msm.py -h

First, use the above command to check what arguments/options are needed: imffolder ==> ./imf_data; output_file ==> you can
give any name you want; -D ==> here we use 2.69 hr; -N here we use 366, which is the days in a year (you can set -D as 1 for testing); 
use the following completed command to examine substorms in 2003:

$ ./msm.py ./imf_data/ output_file.txt -D 2.69 -N 366

__Step 3: # evoluate substorms #__

$./msm_eva.py -h

Use the above command to check what arguments/options are needed. Here, the output_file created in last step is needed:

$ ./msm_eva.py output_file.txt 


__Step 4: # create substorm report #__

$ pdflatex assignment5.tex

$ open assignment5.pdf

