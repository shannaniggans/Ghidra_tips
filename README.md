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

## 2. Disabling Jython (when running ghidrathon)
>Ghidrathon disables the built-in Jython script provider to avoid conflicts when Ghidra decides which provider should handle scripts with the .py file extension. > >This means existing Jython scripts cannot be executed with Ghidrathon installed. We recommend completely disabling the Jython extension.

Use the following steps to disable the Jython extension:

* Navigate to File > Configure...
* Click Ghidra Core
* Un-check PythonPlugin

## 3. Adding columns to Listing window
It might not be obvious at first, but in the Listing heading pane, click on the button "Edit the listing fields" and you can add additional fields such as PCode. Right click on the field and enable.
> P-code is Ghidra’s intermediate representation / intermediate language (IR/IL) for assembly language instructions. Ghidra “lifts” assembly instructions of various disparate architectures into p-code, allowing reverse engineers to more easily develop automated analyses that work with assembly code.

# Plugins & plugin lists
## 1. Awesome IDA, Ghidra, x64DBG & OllyDBG plugins
> A curated list of IDA x64DBG and OllyDBG plugins
* https://github.com/fr0gger/awesome-ida-x64-olly-plugin

## 2. Replica
> Enhances the Ghidra auto analysis process.
* https://github.com/reb311ion/replica

## 3. Ghidra Bridge
> Ghidra Bridge is an effort to sidestep that problem - instead of being stuck in Jython, set up an RPC proxy for Python objects, so we can call into Ghidra/Jython-land to get the data we need, then bring it back to a more up-to-date Python with all the packages you need to do your work.
* https://github.com/justfoxing/ghidra_bridge 

### 

# Training resources
## 1. Ghidra training can be found under GhidraDocs/GhidraClass
* Served online here - https://static.grumpycoder.net/pixel/docs/GhidraClass/Beginner/Introduction_to_Ghidra_Student_Guide_withNotes.html#Introduction_to_Ghidra_Student_Guide.html
## 2. How to tame your Ghidra
> A brief introduction to setting up Ghidra, and then configuring it with a familiar UI and shortcuts, so that you would not need to re-learn all the key sequences you have got used to over the years.
* https://securelist.com/how-to-train-your-ghidra/108272/?es_id=818188ccb0
## 3. Ringzer0 training - WORKSHOP // Reversing with Ghidra // Jeremy Blackthorne
> In this short hands-on workshop, we go over the major features of Ghidra, strengths and weakness, and how it compares to similar tools. We provide exercises that run on Mac, Windows, and Linux so bring whatever environment you got. If you’ve been waiting to take a look at Ghidra, now’s the time!
* https://vimeo.com/showcase/8996638/video/660008560



