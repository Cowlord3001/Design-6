> Lab 1

>> Errors & observations encountered while installing GHDL and GTKWave:

- After advisement from a peer, downloaded Ubuntu to install the programs through WSL.
- Download process was smooth, except for the process of deciding a username. This was attempted multiple times, culminating in the simple username of "chris" after
  Ubuntu refused the other choices. Further investigation is required to determine why this occured, although it is likely that certain characters are blacklisted
  from the WSL username.
- Download for GHDL / GTKWave failed using Linux download instructions.

>> Installation through Windows:

- After numerous issues during installation attempts through Windows / Ubuntu, decided to instead install GHDL and GTKWave through Windows.
- Instructions followed in the GHDL GitHub, downloading and extracting the files before moving their subfolders to the new "eda" folder.
- Environmental variables were added (note: I have had issues with environmental variables in the past, so this should be the first place to debug if issues arise).
- The command "$ cp ~/dsd/ghdl/*vhdl ." failed on the Command Prompt, creating another roadblock.
      ***This was solved by using Windows PowerShell.
- The ghdl commands failed on Windows PowerShell.
      ***After peer review, this was solved by adding "\bin" to the environmental variables in path
- ghdl -h was successfully run, meaning the rest of this lab should theoretically move forward without issue.

>> VHDL / GHDL Studying:

- Reading the resources provided, alongside the wikipedia page, the reason for using VHDL became abundantly clear.
  VHDL allows for the coding of typically hardware-exclusive logic structures (hence HDL: Hardware Description Language) such as AND, OR, NAND, etc.
  While the language (based on Ada) is quite different compared to C++ and other languages typically learned in the CPE curriculum,the basics make structural sense.
  The "entity" characterizes the variables for input and output ports, while the "architecture" determines what the logic gate does with these ports.
- 
