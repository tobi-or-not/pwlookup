# pwlookup
 

## What

*pwlookup* is a script that manages the retrieval of passwords from a plain text file within an encrypted disk image under MacOs.

## Why

There are tons of password managers out there. And they are probably more capable and faster. But hey, this was more fun to build.

## How

### Setup
This script assumes that you have an encryped disk image on your machine that contains a plain text file with your passwords. One password per line.

1. Copy the file pwlookup to some place within your PATH.
2. Copy the file example/pwlookup.conf.example into the same directory as pwlookup
	* Rename it to "pwlookup.conf"
	* Modify it so it matches your system setup

  

### Usage
There are two modes: lookup and insert

#### Lookup
	$ pwlookup <searchTerm>
	
Upon hitting return, you will be asked to enter the password for you disk image. If everything went right, you should receive a list of results matching your search string.

#### Insert
	$ pwlookup -insert

Calling the script this way will open the password file using Vim.

#### Exit
After lookup or insert operations, hit any key to quit the script. It will close the current terminal, so it is a good habit to use a separate terminal window when using the script
