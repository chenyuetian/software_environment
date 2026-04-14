## Prerequisites
To have a good starting point, make sure the default modules are loaded

    module list
    
    Currently Loaded Modules:
    1) shared   2) cpu/0.17.3b (c)   3) slurm/expanse/23.02.7   4) sdsc/1.0   5) DefaultModules
If needed, run `module reset` again to set the modules to default

## Hands-on session 1: working with modules
We run a few module commands to search and load the system-wide installed MATLAB software
1. Search with the module string to show how to load a particular MATLAB

       module spider matlab
       module spider matlab/2022b
       module spider matlab/2022b/lefe4oq

2. Load MATLAB 2022b from the **GPU** software stack

       module reset
       module list
       module load gpu matlab/2022b    # same as module load gpu/0.17.3b matlab/2022b/nmbr5dd since gpu/0.17.3b is the default GPU stack
       module list
       module show matlab/2022b
   
4. Check if the path to the MATLAB executable is correctly set

       which matlab
