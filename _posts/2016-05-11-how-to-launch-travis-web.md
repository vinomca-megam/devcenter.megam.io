---
title: How to launch travis-web in MegamVertice
layout: post
author: "vinothini"
og_image_url: "https://devcenter.megam.io/res/gotalk-intro.png"
description: How to launch travis-web in MegamVertice
---
### Introduction
In software development, Travis-web is an open-source hosted, distributed continuous integration service used to build and test projects hosted at GitHub. Travis CI is configured by adding a file named .travis.yml, which is a YAML format text file, to the root directory of the GitHub repository.

<a href="https://docs.megam.io/installation/prequisites/" target="_blank">
<img src="https://s3-ap-southeast-1.amazonaws.com/megampub/images/vertice/DEPLOY-TO-MEGAM-VERTICE-BIG.png " alt="wordpres button" /></a>


### Prerequisites

* You are running Ubuntu 14.04 or Linux workstation.

* Git installed on your server, which you can do by following the [How To Install Git with Apt.](https://www.digitalocean.com/community/tutorials/how-to-install-git-on-ubuntu-14-04)

* An account on GitHub, which is a Git repository host.

* You have to create a valid credential access for [docs.megam.io](https://docs.megam.io/overview/tour/)

* You have to install openssh-server for ssh access.

		sudo apt-get install openssh-server

* Check SSH working properly

		ps aux | grep sshd
This initial section contains everything you need to get etherpad-lite running on your server.

### Step-1 Fork travis-web
* Fork travis-web
from [here](https://github.com/verticeapps/node_travisweb.git)

* You will be see the fork option in the top right corner of the git hub page.click the fork option.

* The travisweb is forked into your git repository

### Step-2 create SSHKey and launch the app
* Then go to your MegamVertice Dashboard

* Click Marketplace on the top bar.Marketplace contains all the linux distros, applications, services and microservices which megamvertice supports.

* Click Nodejs Icon.A window will pop up with for SSHkey options. You can create new sshkey, use an existing sshkey or upload your own sshkeys too.

* Pick a repository by Choose your public repository.

  Let us use Github: <mygithubid>/travisweb

*	To launch Nodejs App.Click Create.

* Voila ! Your App is up to date.

* Now that you have launched your app, you might want to launch a service (database) and bind it

### Start script
MegamVertice will look for a start script named `start as follows.

	#!/bin/sh
 	sudo invoke-rc.d shellinabox stop
    npm install -g ember-cli
 	bower install --allow-root
 	npm install -g watchman`
 	npm rebuild node-sass
 	npm install
 	ember serve


### **Step-3 Open Your Web browser**
You can access your web page using http://IP_ADDRESS/4200

![](/content/images/2016/05/Screenshot-from-2016-05-27-15-16-35.png)








### Conclusion
These are the very simple steps to launch Nodejs using travis-web. Finally using github repository and launched the travis-web to run successfully.

### To deploy your App
<a href="https://docs.megam.io/installation/prequisites/" target="_blank">
<img src="https://s3-ap-southeast-1.amazonaws.com/megampub/images/vertice/DEPLOY-TO-MEGAM-VERTICE-BIG.png " alt="wordpres button" /></a>
