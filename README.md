# Terminal-Command
## Motivation: Technicalities during 'Programming Parallel Supercomputers' course and command line arrguments. 

### Part 1: Command Line  
To know the logged-in user: Type `whoami` <br />
To know the working directory: Type `pwd` or `cd $WRKDIR` <br />
To create a file: Type `vim practice.c` or `touch practice.c`. Note: `vim` and `touch` also works on different file extensions or different type of files. <br />
To know if the file exists: Type `ls | grep *.c` `ls | grep practice.c` or `find . --name practice.c` or `locate practice.c` <br />

#### Things to add on:
Explain sbatch and srun <br />
`sbatch --account=courses --partition=courses practice.sh`
`less +F slurm-'batch_no'.out`, ctrl+c + q(or anything to get out)
in vim, insert mode, 
non-insert mode, `u` to undo, :q to quit, :wq to save and exit



