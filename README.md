# STEM Simulation Software Overview
An overview of available simulation softwares for Scanning Transmission Electron Microscopy.

**Feel free to PR to update the list or change mistakes!**

I spent a lot of time trying out the various STEM simulation softwares, so I thought I'd summarise my exploration here, in order to help future researchers in the field. This is just intended as a quick overview and there are probably mistakes here, so don't take this list as gospel, and please don't be offended if I have mis-represented your software! STEM simulation has a bit of an entry barrier, and my intention is only to make it a kinder experience for the new user.

If you intend to do STEM simulation to compare with experimental data, you are likely going to need a computer more powerful than your average desktop computer. You will probably either want to use modern NVidia GPU* or a supercomputer**. If you have one or more latest generation GPUs (like GTX 1080TI or RTX 2080TI), you will probably experience better performance on that than you will on supercomputers!

If you are just getting started with STEM simulation, I highly recommend checking out [Prismatic](http://prism-em.com/). The PRISM algorithm it is based on is very fast, it has a reasonably intuitive GUI and *fantastic* documentation online.

*\* Nearly all simulations softwares currently use CUDA, which is only supported by NVidia GPUs. The only exception is STEMcl, which can be run on any modern GPU, including Intel and AMD ones. When using NVidia, you probably want to use at least a GTX 900-series GPU.*

*\*\*check with your university IT department - it is often possible to get free CPU time depending on your access.*

There are now a lot of STEM simulation softwares available. They are all extremely impressive pieces of software, often building on each other. The following table summarizes a few aspects to make it easier for the new researcher to choose the software that is most applicable to their situation.

| Name        	| CPU 	| MPI 	| GPU 	| CPU&GPU 	| GUI 	| Open-Source 	| Scripting? 	| Comments                                                                             	|
|-------------	|-----	|-----	|-----	|---------	|-----	|-------------	|------------	|--------------------------------------------------------------------------------------	|
| [Dr Probe](http://www.er-c.org/barthel/drprobe/index.html)    	| ✅   	|     	| ✅   	| ✅       	|     	|    ✅          	|            	|                                                                                      	|
| [Prismatic](http://prism-em.com/)   	| ✅   	|     	| ✅   	| ✅       	| ✅   	| ✅           	| Python     	| Uses an extremely fast algorithm, but large simulations can require much (>32GB) ram 	|
| [MULTEM](https://github.com/Ivanlh20/MULTEM)      	| ✅   	|     	| ✅   	|         	| ✅   	| ✅           	| Matlab     	| Extremely many types of (S)TEM simulation, can add carbon to sample                  	|
| [STEMSalabim](http://www.stemsalabim.de/en/latest/) 	| ✅   	| ✅   	|     	|         	|     	| ✅           	|            	| The only software designed for CPU supercomputers                                    	|
| [MuSTEM](https://github.com/HamishGBrown/MuSTEM)      	| ✅   	|     	| ✅   	|         	|     	|   ✅           	|            	| Convenient for PACBED patterns, more accurate phonon models                                                       	|
| [QSTEM](https://github.com/QSTEM/QSTEM)       	| ✅   	|     	|     	|         	|     	|    ✅         	| Python     	|                                                                                      	|
| [STEMcl](https://github.com/stemcl/stemcl)       	| ✅   	|     	| ✅    	|  ✅       	|     	|    ✅          	|      	|   Only GPU solution that supports non-NVidia GPUs                                                                                   	|
| [py_multislice](https://github.com/HamishGBrown/py_multislice)       	| ✅   	|     	| ✅    	|  ✅       	|     	|    ✅          	|  Python    	|   Uses PyTorch for acceleration, based on prism algorithm                                                                                   	|



There are some conventions that differ from software to software. The following clarifies the unit of the Debye-Waller factor (root-mean-square or mean-square) and whether it is the top or the bottom of the sample that is at Z=0.

| Name | Debye-Waller<sup>✝</sup>|Is sample Z=0 hit first by beam?
|----|----|----
|Prismatic| RMS |Last
|MULTEM | RMS | First
|STEMSalabim | MS | First


✝ Debye Waller can be expressed as the "Debye-Waller" value in Å, as the root-mean-square value in Å, or the mean square value in Å<sup>2</sup>.
