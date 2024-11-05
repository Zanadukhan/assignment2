# New User Setup Scripts
---

## Creating a new user

Usage: 
  
  usercreation [options] username

  Description: 
  
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

---

# User Configuration Script

Usage: 

setup [options] username

Description:

This script will help you install a suite of packages and/or pre-configure the packages for the new user who's name is passed in as an argument

    Options:

    -p, -package </path/to/file>

    This option will take in a file with package names and install them all for the user

    -c, -configure

    This option will create symbolic links between the cloned files and their respective file/dir locations in the new user's home directory