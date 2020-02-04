## Home-Brew

The purpose of this document is to give the overview about home-brew.


### Why do we use home-brew?

_“Home-brew is a free and open-source software package management system that simplifies the installation of software on macOS and Linux. It is similar to the other package manager like apt, yum etc. which are available for the Linux system”_

The purpose of a package manager is to install the software by identify a legitimate source of a particular piece of software and ensuring that any dependencies required by that software are installed and present at the required version level. It’s the taking the cumbersome job of installation of the software from the users who are new to the MacOS and Linux system.


Commands:

- To install the Home-brew
```mardown
    /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)
```

- To list out the packages we can install with home brew
   ```mardown
   brew search
   ```

- To search any package
```mardown
     brew search <package name>
```

-  To install any package
```mardown
      brew install <package name>
 ```     


Note: 
Home-brew installs the package into their own folder structure and then symlinks their files into /usr/local
The location of the home-brew package is 
/usr/local/Cellar/…

- To get the information about package
```mardown
brew info <package name> 
```
    
If we use the same command to get the info of not installed package then the brew command will give all the details of the package and their respective dependencies, which is required to install.

- To uninstall the package
```mardown
    brew uninstall <package name>
 ```   

- To list out the package which is installed
```mardown
    brew list
```    

- To update the newest version of all of the packages of the brew
```mardown
    brew update
```    

- To list out the outdated packages which are installed
```mardown
    brew outdated
```

- To update all the outdated packages
```mardown
    brew upgrade 
```    

- To update the specific outdated package
```mardown
    brew upgrade <package name>
```    

- To stop something from being updated/upgrade
```mardown
    brew pin <package name>
```    

- To allow that formulae to update again 
```mardown
    brew unpin <package name>
```    


Note:
By default home-brew uninstall the old version packages after 30 days.

- To remove all the older version of the packages manually
```mardown
    brew cleanup
```
- To remove specific older version of the package manually
```mardown
    brew cleanup <package name>
```    

- To disable the home-brew automatic clean up
```mardown
    export HOMEBREW_NO_INSTALL_CLEANUP=1
```    


Note:
If you ever come up with any problem with home-brew then home-brew comes up with self diagnosis tool, which diagnose the issue and let you know

- To diagnose home-brew issue
```mardown
    brew doctor
```

To install Mac OS native application home-brew uses cask to install Mac OS application into the system

- To install Mac OS application
```mardown
    brew cask <software/app name>
```    

- To get the info about the installed or yet to install software or package
```mardown
    brew cask info <software/app name>
```    

- To navigate to home page of the software
```mardown
    brew cask home <software/app name>
```    


So far home-brew installs the package which exists on the core home-brew repository.
What if the package does not exist into the core home-brew repository.
On that case we need to add/tap that repository into the home-brew core repository then install by using the same command mentioned above.

- Tap the repository
```mardown
    brew tap <repository name>
```    


If the user does not want the home-brew into the system

- To uninstall the home-brew
```mardown
    ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/uninstall)"
 ```   

Note: 
if we uninstall the brew then the package we have installed through the brew will also get uninstalled except the software or app which is installed by using brew cask.
