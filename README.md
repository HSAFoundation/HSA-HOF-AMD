# HSA-HOF-AMD
HSAIL Offline Finalizer (HOF): a tool for offline finalization of HSAIL or BRIG file to ISA.

## Command Help

```
> hof -help

  -help                          display this help menu
  -model=[small|large]           machine model to finalize for (optional)
  -profile=[base|full]           profile to finalize for (optional)
  -target=[ISA]                  target instruction set architecture (optional)
                                 "7:0:0" used if "-target" is omitted
  -output=[OUT]                  output filename (optional)
                                 "a.o" used if "-output" is omitted
  -brig [BRIGs]                  one or more brig module files
  -hsail [HSAILs]                one or more hsail text files
  -g                             generate debug information
  -O0                            disable all optimizations
  -O2                            use 2nd optimization level
  -amd-max-num-vgprs=[NUM]       set maximum number of VGPRs to NUM
  -amd-max-num-sgprs=[NUM]       set maximum number of SGPRs to NUM
  -amd-reserved-num-vgprs=[NUM]  reserve [NUM] VGPRs
  -amd-reserved-num-sgprs=[NUM]  reserve [NUM] SGPRs

```

## Running the example

The HOF example demonstrates the usage of the HOF tool to perform offline finalization of an hsail file and to launch a kernel from the finalized object.
It requires the [HSA Runtime](https://github.com/HSAFoundation/HSA-Runtime-AMD) and development files.  Simply type `make` to compile the example. 

