# Terminal-Command
## Motivation: Technicalities during 'Programming Parallel Supercomputers (PPS)' course and command line arrguments. 

### Part 1: Command Line  
To know the logged-in user: Type `whoami` <br />
To know the working directory: Type `pwd` or `cd $WRKDIR` <br />
To create a file: Type `vim practice.c` or `touch practice.c`. Note: `vim` and `touch` also works on different file extensions or different type of files. <br />
To know if the file exists: Type `ls | grep *.c` `ls | grep practice.c` or `find . --name practice.c` or `locate practice.c` <br />
To delete the files, especially slurm-'smth'.out: Type `rm slurm-*.out` to delete without asking while `rm -i slurm-*.out` asks for confirmation for each slurm-'smth'.out file to be deleted or not.

#### Things to add on:
Explain sbatch and srun <br />
`sbatch --account=courses --partition=courses practice.sh`
`less +F slurm-'batch_no'.out`, ctrl+c + q(or anything to get out)
in vim, insert mode, 
non-insert mode, `u` to undo, :q to quit, :wq to save and exit


### Batch Script:
--ntasks-per-node means maximum number of tasks to be run and this will be default. However, if --ntasks is included, then it will override the --ntasks-per-node. So, in total --ntasks will be run regardless of number of nodes reserved for the code. <br />

periodic = {1,0} means wrapping around vertically (up-down) but not horizontally (left-right) while {0,1} means wrapping around horizontally (left-right) but not vertically (up-down). <br />

MPI_Cart_shift(my_new_comm, 0, 1, &up, &down) means that I am finding the neighbour 1 step from the current process in x-axis/direction (row-wise indicated by 0 in the second argument). <br />
