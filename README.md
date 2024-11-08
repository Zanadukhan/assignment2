# New User Setup Scripts


This repository contains two bash scripts that will help you create and configure a new user on a linux system.

note: this must be done by the root user or through sudo



## 2. User Configuration Script (Project_1)

### Usage: 

setup [options] username

### Description:

This script will help you install a suite of packages and/or pre-configure the packages for the new user who's name is passed in as an argument

    Options:

    -p, -package </path/to/file>

    This option will take in a file with package names and install them all for the user

    -c, -configure

    This option will create symbolic links between the cloned files and their respective file/dir locations in the new user's home directory

### Example:

sudo setup -p packages -c new_user

This would install packages provided in the "packages" file and create symbolic links between the 2420 starting files and the home directory equivalents in the new_user's home directory

---

## 2. Creating a new user (Project_2)

### Usage: 
  
  usercreation [options] username

### Description: 
  
  This script allows users to create a new user with a custom home directory, custom shell, additional groups to add the new user to, and setting a password

    Options:

    -m, --man 

    This option displays the manual for this script

    -s, --shell <name of shell>

    default: bash

	This allows the user to specify a specific shell for the new user rather than the default shell for users

	-h, --home <absolute/path/to/dir>

    default: /home/<username>

	If the user provides an argument, a custom home directory will be created an  d set for the new user

	-g, --group group1[ group2 group3 group4...]

    default: <username>

	the user can be added to additional group along with the initial default group

    -i, --id <number>

    if a specific userID wants to be used for a user, a number can be passed in as an option

### Example:

sudo usercreation -i 1001 -h /home/new -s bash -g "wheel nathan" tim

This would create a new user called tim with the UID and GID of 1001, a home directory at /home/new, belonging to the groups wheel and nathan.