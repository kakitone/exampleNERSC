# exampleNERSC
## Using Cori (reference: http://www.nersc.gov/users/computational-systems/cori/getting-started/your-first-program-on-cori-p1/)

1. log in to the system: 
    
    ssh -Y yourusername@cori.nersc.gov

2. Compile your code 
     

3. Create a batch script
    
\#!/bin/bash -l

\#SBATCH -p debug

\#SBATCH -N 2

\#SBATCH -t 00:10:00

\#SBATCH -J my_job

srun -n 64 ./helloWorld

4. Submit your job

    sbatch my_batch_script

5. Check your status
    
    squeue -u username
