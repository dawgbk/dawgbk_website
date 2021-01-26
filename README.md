DAWG
====

Dog Alliance of Greenpoint and Williamsburg


What is this?
=============

This repository contains the Source Code and Build Instructions for the DAWG
website, https://dawgbk.com


How is this organized?
======================

* `-source-dawgbk.com` A directory containing the source code to generate the
  site
* `assets` Assets used to build the site
* `dawgbk.com` An untracked directory (via `.gitignore`) that contains a built
  version of the website.


How is the website built and updated?
=====================================

The website is generated using [Lektor](https://www.getlektor.com/), a Content
Management System that generates static websites.

The website uses the
[Bootstrap 4.5](https://getbootstrap.com/docs/4.5/getting-started/introduction/)
CSS and HTML Framework. Bootstrap offers a CSS Grid with multiple components that
reliable work across the most popular platforms, browsers and devices.

Third Party embedded widgets are used for additional functionality.

Access to the website server/host (in the cloud) is handled with "SSH Keys".
SSH Keys are cryptographically secure tokens that are generated on a User's
machine and then installed on the Web Server.  A member of DAWG who has already
gone through the process of installing SSH Keys on the server will be able to
help you get set up.

Instructions 
============

To build or update the website, Lektor must be installed.

1. Install Lektor 
   There are detailed instructions for Mac, Linux and Windows on
   https://www.getlektor.com/downloads/

2. Download this Source Code
   The source code repository is managed by `git` and hosted at GitHub https://github.com/dawgbk/dawgbk_website
   You can use any git client - commandline or GUI - to download the website.
   Git and Github are like a Dropbox or Google Drive, specifically used to host code.
   
   Popular Clients
   * Git Commandline
   * Github Desktop https://desktop.github.com/
   * SourceTree https://www.sourcetreeapp.com/
   
   For more information: https://git-scm.com/download/gui/windows
   

3. Navigate to the source directory and run Lektor


Example- Editing
================

On a Mac, the terminal commands might look like this:

    # make a directory to host our work
    mkdir websites
    cd websites
    
    # clone the git repository
    git clone git@github.com:dawgbk/dawgbk_website.git
    cd dawgbk
    cd ./-source-dawgbk.com
    
    # run Lektor
    lektor server

This will start running the Lektor CMS on your local computer. Using the web-based
CMS tool, you can edit or add pages.

Example- Publishing
===================

When you want to publish the website, there are two steps:

1. Click the "publish" button on the Lektor CMS that is running on your machine.
  This will connect with the webserver and update the website.

2. Commit your changes to source control and upload them, so we have a backup and
   other people can work on this.
     
  This step is done in two mini-steps: commit, then push.
  
  `commit` will save your changes locally
  `push` will upload your changes to Github
  
  If using the commandline option, it looks like this:
  
    # commit the changes
    git commit .
    # upload the changes
    git push 

  If using a GUI, there may be a button for 'commit' and another button for 'push'.

