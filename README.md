# jsbsd

A collection of scripts to quickly bootstrap a FreeBSD-box as a complete js development environment


This script assumes that you have a fresh install of FreeBSD 10 on a amd64 box with one network adapter. 
You must run this as root. So read it all if you want to be on the safe side. I may have made many mistakes along the way so keep the host-box safe.

You run setup and that will tell you what you need to provide.

A note on convenience: Plop any id_rsa.pub in the folder that you are running the scripts from and that will be populated as an authorized key for all the sandboxes. This way you don't have to do that afterwards. 


1: Install needed software on host, Creates aliases on the nic, creates jails 

   * Creates the appropriate sandboxes for application, db, session store and a web proxy

   * Populates sandboxes with ssh keys from the host and those you supply

   * Starts the sandboxes

2: Some network and user configuration

   * Starts sshd and provides dns-settings and hostnames for the other boxes in the project

   * Boilerplates a non-root user and tests SSH. 

   * Creates applications that can be used as short-hand for firing commands to the nodes

   * Tests those applications by having the box return it's given hostname

3: 

   * Configures services on the sandboxes

   * Installs some programming languages and frameworks in the app sandbox

   * Installs mongodb or couchdb on the db sandbox

   * Installs redis on the session store sandbox

   * Installs nginx on the web proxy sandbox

   * Fixes g++ missing symlink to clang++

   * Installs a set of node modules on the application-sandbox

   * Starts mongodb, redis and nginx on the three different jails

   * Adds user as boilerplated in step 2

4: 

   * Copying ssh keys to the unpriviledged user

   * Creating a new application for running commands as the unpriviledged user

   * Create a new sails project

   * 

