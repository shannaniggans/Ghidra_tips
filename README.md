# Ghidra_tips

## 1. Resize Ghidra for High DPI screens

> If you run Ghidra on a high DPI screen, you will probably find the GUI to be scaled down so small to be almost of no use.
There is a setting that you can adjust to scale the Ghidra GUI:

### Linux

* In `$GHIDRA_ROOT/support` is a file named launch.properties. 
* In this launch.properties file is the following configuration key: `VMARGS_LINUX=-Dsun.java2d.uiScale=1`
* Change this line to: `VMARGS_LINUX=-Dsun.java2d.uiScale=2`

Credit: gist.github.com/nstarke/baa031e0cab64a608c9bd77d73c50fc6

### Windows
* modify line 10 in ghidraRun.bat as follows (for 1.5 x scale): `call "%~dp0support\launch.bat" bg Ghidra "%MAXMEM%" "-Dsun.java2d.uiScale=1.5" ghidra.GhidraRun %*`

## 2. Ghidra training can be found under GhidraDocs/GhidraClass
* Served online here - https://static.grumpycoder.net/pixel/docs/GhidraClass/Beginner/Introduction_to_Ghidra_Student_Guide_withNotes.html#Introduction_to_Ghidra_Student_Guide.html


## 3. Awesome IDA, Ghidra, x64DBG & OllyDBG plugins
* A curated list of IDA x64DBG and OllyDBG plugins - https://github.com/fr0gger/awesome-ida-x64-olly-plugin

## 4. How to tame your Ghidra
> A brief introduction to setting up Ghidra, and then configuring it with a familiar UI and shortcuts, so that you would not need to re-learn all the key sequences you have got used to over the years.
* https://securelist.com/how-to-train-your-ghidra/108272/?es_id=818188ccb0
