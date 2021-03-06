---
title: Mac OSX
---

Mac
===

Mavericks
---------

We do not recommend following this training on older versions of OSX without an app store: upgrade
to OSX Mavericks. It should be possible to complete the instructions on any OSX version with the
App store (Snow Leopard (10.6) and newer) However, we recommend upgrading to Mavericks if possible
since this is the most well tested.

XCode and Command line tools
----------------------------

Install the XCode command-line-tools by opening a terminal and run the following.

``` bash
xcode-select --install
```
And follow the on screen instructions.

You may also install Xcode from the Mac app store if you wish, but it is not needed.

Pre Mavericks:

Install [XCode](https://itunes.apple.com/us/app/xcode/id497799835) using the Mac app store.

Then, go to Xcode...Preferences...Downloads... and install the command line tools option.

##Git

The XCode tools comes with Git so no need to do anything more.

Homebrew
--------
[Homebrew](brew.sh) is a package manager for OSX which enables the installation of a
lot of software useful for scientific computing. It is required for some of the installations
below. But not essential for Software Carpentry. Homebrew requires the Xcode tools above.

Install Homebrew via typing this at a terminal:

``` bash
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

and then type.

```bash
brew doctor
```

And read the output to verify that everything is working as expected.

If you are already running MacPorts or another package manager for OSX we don't recommend
installing homebrew.


Python
------

We recommend installing a complete scientific python distribution. One of these is
Enthought Canopy.
The Enthought Canopy python distribution exists in two different versions. A basic free version
with a limited number of packages (Canopy express) and a non free full version. The full version
can be obtained free of charge for academic use. Register with [Enthought Scientific Computing](https://enthought.com/products/canopy/academic/) using your UCL
e-mail address for an academic licence.

You may then use your Enthought user account to sign into the installed application and activate the
academic version. Canopy comes with a package manager from where it is possible to install and
update a large number of python packaged. The packages installed by default should cover our needs.

Python from Homebrew
--------------------

Alternatively if you wish to install python manually you can use Homebrew. 
OSX ships with python and some packages. However this has known limitations and we do not recommend it. 
You can install a new version of python from Homebrew with the following.
Please follow the instructions above to install the Xcode tools and Homebrew before attempting
this.

```bash
brew install python
```

In order to ensure that this version of python is selected over the OSX default version you should
execute the following command:

```bash
echo export PATH='/usr/local/bin:$PATH' >> ~/.bash_profile
```
and reopen the terminal. Verify that this is correctly installed by executing

```
python --version
```

Which should print:

```
Python 2.7.8
```
The System Python version on OSX Mavericks is 2.7.5

Then install additional python packages by executing the following.

brew install [package-name]
*  pkg-config
*  freetype
*  gfortran

pip install [package-name]
*  numpy
*  nose
*  scipy
*  matplotlib
*  ipython[all]

The following packages should be installed automatically as dependencies. But we recommend 
installing them manually just in case. 

*  tornado
*  jinja2
*  pyzmq


Editor and shell
----------------

The default text editor on OS X *textedit* should be sufficient for our use. Alternatively
http://mac.appstorm.net/roundups/office-roundups/top-10-mac-text-editors/ lists a number of other good editors.

A new open source option is Github's Atom editor. You can get it from https://atom.io/
However, note that this is still in somewhat early development.

To setup git to use *textedit* executing the following in a terminal should do.

``` bash
git config --global core.editor /Applications/TextEdit.app/Contents/MacOS/TextEdit
```

The default terminal on OSX should also be sufficient. If you want a more advanced terminal
[iTerm2](http://www.iterm2.com/) is an alternative.

