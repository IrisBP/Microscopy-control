# MetaMorph Controler (python) 

### INSTALLATION INSTRUCTIONS: 
- must download the script
- must download the Interop.MMAppLib.dll - Dll library allowing python to connect to MetaMorph to control the microscope
- must have MetaMorph running on the computer 

IMPORTANT LIBRARIES: 
matplotlib.pyplot, numpy, math, time, pandas,scipy.optimize, tifffile, PIL, json, PIL.TiffTags

### SETTING UP BEFORE FIRST USE: 
The acquisition of images is done by running a MetaMorph journal doing 1 acquisition.
\
If this journal does not exist, it must be created within MetaMorph. Once this journal exists, copy the path to the journal in the script (Connecting Metamorph => ex: 'C:\\MM\\app\\mmproc\\journals\\s.JNL')
\
You must also indicate the path to the file where MetaMorph saves its temporay images (Connecting Metamorph => ex: path_tmp='C:\\TEMP\\"

### DATA FORMAT

The images are saved individually as .tif files and together (grouped by position and acquisition wavelenght) as a stack (.tif). 
\
The meta data for each stack is saved as a .txt file independtly from the stack file.
\
The positions are save in a .csv file (table, readable using a text app or excel). 


### FOR FIRST TIME PYTHON USERS: 

Each square containing either some text or code is called a "cell". You can execute the cell by clicking on the Run button on the controk bar at the top of the page or using the ctr+enter command. 
Before setting up an acquision, make sure to have correctly imported the DLL, libraries and functions (you should have some text appearing when you run those specific cells such as "Libraries are Good to go"). 
\
Once all the libraries and functions are charged, you can set up your acquisition by changing the parameters. 


The script is set up to acquire timelapse on one (or multiple) position, with one (or multiple) wavelenght. You can also add an activation step (laser pulse). 

You can also write your own script based on the same logic. Don't hesitate to explore the list of function and the script encoding the acquisition to write your own. The functions are available independently in the MM_function file


### IMPORTANT: Make sure to close the MetaMorph live window before launching your acquisition. Leaving the MetaMorph live window open might resutls in MetaMorph crashing down.
If MetaMorph shuts down, just restarts it. Make sure to restart the script as well and to reconnect the DLL. 
