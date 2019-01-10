# STEM Simulation Software Overview
An overview of available simulation softwares for Scanning Transmission Electron Microscopy
Feel free to PR to update the list or change mistakes!

I spent a lot of time trying out the various STEM simulation softwares, so I thought I'd summarise my exploration here, in order to help future researchers in the field. There are probably mistakes here, so don't take this list as gospel!

If you intend to do STEM simulation to compare with experimental data, you are likely going to need a computer more powerful than your average desktop computer. You will probably either want to use modern NVidia GPU* or a supercomputer**. However, the Prismatic software is much faster using their PRISM algorithm. However, for large simulations it can use a large amount of memory.

\* All simulations softwares currently use CUDA, which is only supported by NVidia GPUs. You probably want to use at least a GTX 900-series GPU.
\*\*check with your university IT department - it is often possible to get free CPU time depending on your access

| Name        	| CPU 	| MPI 	| GPU 	| CPU&GPU 	| GUI 	| Open-Source 	| Scripting? 	| Comments                                                                             	|
|-------------	|-----	|-----	|-----	|---------	|-----	|-------------	|------------	|--------------------------------------------------------------------------------------	|
| Dr Probe    	| ✅   	|     	|     	|         	|     	|             	|            	|                                                                                      	|
| Prismatic   	| ✅   	|     	| ✅   	| ✅       	| ✅   	| ✅           	| Python     	| Uses an extremely fast algorithm, but large simulations can require much (>32GB) ram 	|
| MULTEM      	| ✅   	|     	| ✅   	|         	| ✅   	| ✅           	| Matlab     	| Extremely many types of (S)TEM simulation, can add carbon to sample                  	|
| STEMSalabim 	| ✅   	| ✅   	|     	|         	|     	| ✅           	|            	| The only software designed for CPU supercomputers                                    	|
| MuSTEM      	| ✅   	|     	| ✅   	|         	|     	|             	|            	|                                                                                      	|
| QSTEM       	| ✅   	|     	|     	|         	|     	|             	| Python     	|                                                                                      	|
