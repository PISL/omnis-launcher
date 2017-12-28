# omnis-launcher
An [Omnis Studio](http://www.omnis.net) library that can be used to automatically open other libraries upon startup.  Normally, libraries placed in the startup folder are opened in alphabetical order, so this utility was created to open libraries in an arbitrarily assigned order and regardless of their location.

## Usage
Place launcher.lbs in the Omnis startup folder along with a text file named launcher.txt.  The library will open this file in its Startup_Task.$construct method.

## launcher.txt format
This file should contain full path names of the libraries you wish to open, one per line. 

`Users/my/path/to/library/lib.lbs`

or 

`C:/path/to/library/lib.lbs`

The file can contain comments marked with a hash '#' 

`Users/my/path/to/library/lib.lbs   # this is the important app`

or

`# Users/my/path/to/library/lib.lbs   this lib will not be opened`

The path can be prefixed with '!!!' and the libarary will be opened  but the startup task of the library will not be instantiated until all libraries in the file have been opened.

`!!!Users/my/path/to/library/lib.lbs`