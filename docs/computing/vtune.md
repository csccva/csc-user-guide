# Using Intel VTune Amplifier
The Intel Tools are provided via the ```intel-vtune ``` module. For profiling one sets up the enviroment by loading the module as follows:
```
module load intel-vtune
```
If you want to get source code level information, compile your code with optimizations enabled and add also
the debugging information option ```-g```. Basic hotspot analysis is the first analysis type you should try. Here is
a sample batch job script that can be used to profile a serial and OpenMP applications:
```
#!/bin/bash
#SBATCH --job-name=VTune_example
#SBATCH --account=<project_name>
#SBATCH --partition=<partition_name>
#SBATCH --time=00:15:00
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=20
#SBATCH --mem-per-cpu=4000

# set the number of threads based on --cpus-per-task
export OMP_NUM_THREADS=$SLURM_CPUS_PER_TASK

module load intel-vtune

srun amplxe-cl -r results_dir_name -collect hotspots -- ./my_application
```
# Analysing the Results Using GUI

Results can be viewed using the amplxe-gui application. Unfortunately it does not work well with ssh
and X11 forwarding, so we recommend using the analysis tool in NoMachine environment (see NoMachine
user’s guide). The GUI is available in Puhti and Mahti when the module intel-vtune is loaded. You can inspect
the results of a profile run by giving the name of the results directory as an argument to the amplxe-gui,
for example, the results of previous example can be viewed with command ```amplxe-gui results_dir_name```.
Please see Intel’s documentation for more information on using the GUI: [https://software.intel.com/content/www/us/en/develop/documentation/vtune-help/top.html](https://software.intel.com/content/www/us/en/develop/documentation/vtune-help/top.html)