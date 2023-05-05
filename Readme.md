This is VSCode configuration for running and debugging C/C++ codes aimed at doing competitive programming

To get started follow the below steps

## Pre-requisites
* Install C/C++ for Visual Studio Code extension for vscode
* Install gcc/g++ compiler on your system

## Install GCC compiler on your platform
You need to install gcc compiler on every platform since it is the preferred environment for competitive programming, hence the configurations are geared towards gcc compiler.

The three commands which are needed include `gcc` and `g++` for compiling C++ source files and `gdb` for debugging purpose.

The following are the steps to install gcc compiler in each platform

#### Windows
You can refer this link: https://code.visualstudio.com/docs/languages/cpp#_example-install-mingwx64

#### MacOS
Usually the installed `gcc` command on MacOS is just a shortcut to `clang` compiler, you can check this by running `gcc --version`. Your output will say that it is a clang compiler.

Hence we will install actual gcc compiler and override the gcc command, although it is not recommended, you can specify `compilerPath` in `c_cpp_properties.json` for the installed gcc compiler directly as well.

> **Note:** Since setting up `gdb` on MacOS is difficult, you can skip its installation.
> Consequently debugging will not work in case of MacOS

* Install [Homebrew](https://brew.sh/)
* Run the following commands:
  ```bash
  brew install gcc
  brew install gdb # You can skip this
  ```
* Check installed gcc/g++/gdb
  ```bash
  ls -a /usr/local/bin
  ```
* You will find `gdb` (if installed), `gcc-xx` and `g++-xx` in the list of files, where xx is version of gcc installed. For me it was `gcc-12` and `g++-12` respectively. We can make softlinks (shortcuts) to these binaries (change the command according to your gcc/g++ version):
  ```bash
  ln -s /usr/local/bin/gcc-12 /usr/local/bin/gcc
  ln -s /usr/local/bin/g++-12 /usr/local/bin/g++
  ```

#### Linux
Here are commands you can run on ubuntu or similar linux
```bash
sudo apt update
sudo apt install gcc g++ gdb
```

### Check installation
You can run the following commands one by one to check if each command is installed properly after following the above instructions:

```bash
gcc --version
g++ --version
gdb --version # if installed
```

## Steps to compile and run
1. Clone the repository using git or download it and open it in vscode
2. Create Shortcut to run the C/C++ file
   1. Click <kbd>F1</kbd> to open search bar and type "keyboard shortcut"
   2. Select "Preferences: Open Keyboard Shortcuts"
   3. Search "test" and select "Run Test Task" and assign it to <kbd>Ctrl</kbd>+<kbd>Enter</kbd> (or <kbd>⌘</kbd>+<kbd>Enter</kbd> if MacOS). I am using these keyboard shortcuts as they are usually present in online IDEs but you can choose whatever shortcut you'd like to configure
3. Now you can open any C/C++ file, type your code and hit <kbd>Ctrl</kbd>+<kbd>Enter</kbd> (or <kbd>⌘</kbd>+<kbd>Enter</kbd> or whatever you have configured) shortcut to run the file

## Debugging
If you want to debug your file you can put a debug point at any line and go to `Run > Start debugging` from your menu bar or hit <kbd>F5</kbd> to start debugging