# foafx_gui

*Tested on Mac OS 13.2 with Max 8.5.2*

foafx is a command line tool for applying spatially positioned audio effects to first order ambisonic sound files.

foafx_gui is a Max patch for configuring and running foafx. 

<img width="1066" alt="foafx_gui" src="https://user-images.githubusercontent.com/2341558/220534903-b39fd911-87e3-4af7-90fb-9ccaf88f5ac8.png">


# Installation

Move the "foafx-helper" folder to the top level of your home directory so that it can be located in Terminal at:

~/foafx-helper

This folder contains two files that are written and run by the Max patch: 
1. foafx.command 
2. foafxconfig.json

There is also an input and output folder. 

Files processed with foafx_gui will automatically be saved to the output folder.

The input folder is only there as a suggested place to store your source files. The patch will allow you to select files from anywhere on your computer.

# Dependencies

You will need to install the following: 

shell object for Max 
https://cycling74.com/forums/shell

ICST Ambisonics via the Max Package Manager

node.js
https://nodejs.org/en/download/

foafx 
https://github.com/risdsound/foafx

foafx is a Node.js program distributed on npm. Therefore, before installing foafx you must first install Node.js.

If you install Node.js with the installer available at https://nodejs.org/en/download/, you can install foafx as a global command line as follows,

```
 sudo npm install -g foafx
```

# Running

Source audio files must be encoded as first order ambisonics (4-channel) in ACN format (not FuMa). The patch allows you to select either N3D or SN3D normalization as appropriate.

Follow all the steps in order listed in the patch (1-4).
1. Set position, global, and effects parameters
2. Save updates to configuration file
3. Set options (choose the effect, normalization, and input file)
4. Run the foafx process

Please note, on a Mac when you run the foafx process the first time you will likely get a message like, 

> foafx.command” cannot be opened because it is from an unidentified developer.
macOS cannot verify that this app is free from malware. ...

To bypass this issue you will need to go to your System Settings under Security to choose the "open anyway" option that should appear there. 


# More

More information on foafx can be found at:
https://github.com/risdsound/foafx

