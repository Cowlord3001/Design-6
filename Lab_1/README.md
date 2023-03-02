>> Errors & observations encountered while installing GHDL and GTKWave:

- After advisement from a peer, downloaded [**Ubuntu**](https://en.wikipedia.org/wiki/Ubuntu) to install the programs through [**WSL**](https://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux).
- Download process was smooth, except for the process of deciding a username. This was attempted multiple times, culminating in the simple username of "chris" after Ubuntu refused the other choices. Further investigation is required to determine why this occured, although it is likely that certain characters are blacklisted from the WSL username.
- Download for GHDL / GTKWave failed using Linux download instructions.

>> Installation through Windows:

- After numerous issues during installation attempts through Windows / Ubuntu, decided to instead install GHDL and GTKWave through Windows.
- Instructions followed in the GHDL GitHub, downloading and extracting the files before moving their subfolders to the new "eda" folder.
- Environmental variables were added (note: I have had issues with environmental variables in the past, so this should be the first place to debug if issues arise).
- The command "$ cp ~/dsd/ghdl/*vhdl ." failed on the Command Prompt, creating another roadblock.
    - This was solved by using Windows PowerShell.
- The ghdl commands failed on Windows PowerShell.
    - After peer review, this was solved by adding "\bin" to the environmental variables in path
- ghdl -h was successfully run, meaning the rest of this lab should theoretically move forward without issue.

>> [**VHDL**](https://en.wikipedia.org/wiki/VHDL) / GHDL Studying:

- Reading the resources provided, alongside the wikipedia page, the reason for using VHDL became abundantly clear. VHDL allows for the coding of typically hardware-exclusive logic structures (hence HDL: Hardware Description Language) such as AND, OR, NAND, etc. While the language (based on [**Ada**](https://en.wikipedia.org/wiki/Ada_(programming_language))) is quite different compared to C++ and other languages typically learned in the CPE curriculum,the basics make structural sense. The "entity" characterizes the variables for input and output ports, while the "architecture" determines what the logic gate does with these ports.
- Looking into GHDL, the first piece of information I found is that the "G" apparently doesn't stand for anything. While the "V" in VHDL stands for "Verification and," the "G" in GHDL has no other meaning. GHDL is an *"analyzer, compiler, simulator and (experimental) synthesizer that can process (nearly) any VHDL design"* ([**GHDL Github**](https://ghdl.github.io/ghdl/about.html)). Effectively, it acts as a simulator and compiler for VHDL code without the need for intermediary steps (such as translating to a C-based language first).

>> [**Icarus Verilog**](https://en.wikipedia.org/wiki/Icarus_Verilog) Exploration:

- [**Verilog**](https://en.wikipedia.org/wiki/Verilog) is another HDL that is used to verify different types of circuits. Icarus Verilog acts as a compiler for the language that reformats the resulting code into [**EDIF**](https://en.wikipedia.org/wiki/EDIF). This is used to format [**netlists**](https://en.wikipedia.org/wiki/Netlist), which in turn is a way to describe how circuit components connect.

>> Running GHDL / GTKWave:

[**Hello, World!**](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program):

![image](https://user-images.githubusercontent.com/39775736/222575570-592b6c92-f0ca-4b1a-a4e8-8c70398a1ae6.png)

[**Half Adder**](https://en.wikipedia.org/wiki/Adder_(electronics)#Half_adder):

![image](https://user-images.githubusercontent.com/39775736/222576919-11789efa-1a64-4d59-bb9e-cb33e2cec8b6.png)
![image](https://user-images.githubusercontent.com/39775736/222576782-174ed3d3-763e-4c00-9094-2bb07d84e8aa.png)

[**1-to-4 Demultiplexer**](https://allaboutfpga.com/vhdl-code-for-1-to-4-demux/):

![image](https://user-images.githubusercontent.com/39775736/222577677-4b9eee08-2636-412b-86e0-87ee60c41916.png)
![image](https://user-images.githubusercontent.com/39775736/222577643-56a6ea20-ddb0-43b2-9db9-2c6c21d3d6e5.png)
