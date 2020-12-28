This is VSCode configuration for running and debugging C/C++ codes aimed at doing competitive programming

To get started follow the below steps

## Pre-requisites
* Install C/C++ for Visual Studio Code extension for vscode
* Install gcc/g++ compiler on your system


## Steps to run
1. Clone the repository using git or download it and open it in vscode
2. Create Shortcut to run the C/C++ file
   1. Click `F1` to open search bar and type "keyboard shortcut"
   2. Select "Preferences: Open Keyboard Shortcuts"
   3. Search "test" and select "Run Test Task" and assign it to "Ctrl+Enter" (I am using "Ctrl+Enter" as it is usually the shortcut in online IDEs)
3. Now you can open any C/C++ file, type your code and hit "Ctrl+Enter" shortcut to run the file

## Debugging
If you want to debug your file you can put a debug point at any line and go to `Run > Start debugging` or hit `F5` to start debugging


### Note
This configuration is tested on Windows machine, and to make it work on Linux/Mac, it might require some tweaks