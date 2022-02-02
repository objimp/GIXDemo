# GIXDemo
Demo repository for TECHIN514 - NOT FOR STUDENT USE


This lab is designed to become familar with github and conda.  

github is the tool for sharing code and working on projects together.  its also sometimes important to manage dependencies so everyone is running from the same set of libraries.

we can do this with package managers or with python virtual environments. conda is a popular package manager that makes it easy to manage a list of library dependencies that might need to be installed.   there are other options too of course, but conda is pretty good.

so for this lab... 

install github and miniconda
clone this repository (GIX514Demo) onto your computer.

it includes a conda environment yaml that you'll need to activate.

from the respository, create a new conda environment from GIX514Demo.yaml

conda env create --file GIX514Demo.yaml

and activate the new environment

conda activate GIX514Demo

and run the python script GIX_envtest.py

you should see these version numbers for python and the installed numpy package. record these for your answer.... 


now let's do the same for someone else and setup an environment to share!

create a new public repository, name it TECHIN514-xxxxx where xxxxx is whatever you think is a good name copy the file env-test.py from this repo into your new repository.
you'll also need numpy installed, and we'll specify a specific version, and do to that we'll use conda.

let's say for exmaple we need a specific version of numpy to be compatible with our code e.g. 1.19.5 (even though the current version might be 1.21)

create a new conda environment called GIX514Assignment that includes numpy 1.19.5

(conda create env --name GIX514Assignment python=3.8 numpy=1.19.5)




to test this, open python and note the current version.  and the version of the numpy library.  on my computer for example... 

Python 2.7.18 (default, Nov 13 2021, 06:17:34)
[GCC Apple LLVM 13.0.0 (clang-1300.0.29.10) [+internal-os, ptrauth-isa=deployme on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import numpy as np
>>> print(np.__version__)
1.8.0rc1
>>>

then check your list of available environments 
(conda env list)

then activate the new conda environment GIX514Assignment

(conda activate GIX514Assignment)

you'll see the prompt change to show the active environment.  now repeat the same steps and note your python and numpy version.

(GIX514Assignment) blah@blahblah ~ % python
Python 3.8.11 (default, Aug 16 2021, 12:04:33)
[Clang 12.0.0 ] :: Anaconda, Inc. on darwin
Type "help", "copyright", "credits" or "license" for more information.
>>> import numpy as np
>>> print (np.__version__)
1.19.5

pretty cool!  we've specified our environment exactly.
now export your environemnt so you can share it with someone else.
conda env export --name GIX514Assignment > GIX514Assignment.yaml
add that file to your repository on github.

update the readme file to explain that the yaml file includes a conda environment for the necessary dependencies you might need to run files from this repository.






resources:

this is a good cheat sheet for conda https://docs.conda.io/projects/conda/en/latest/_downloads/843d9e0198f2a193a3484886fa28163c/conda-cheatsheet.pdf




