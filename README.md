# gitscm-config-win
---

### Basic instructions for configuration of gitbash (git-scm for Windows).

Download and install git from https://git-scm.com/downloads

When installing select use Git and optional Unix tools from the command prompt.


#### Download the zip file of this repository and extract somewhere convenient.
---

>Set name and email address.

 Open gitbash, navigate to home directory, set name and email address.

$ cd ~

$ git config --global user.name "your name"

$ git config --global user.email "addy@server.com"


>Setup ssh keys for github.

* Copy the [.bash_profile](./.bash_profile) file to the home directory.

* Create a hidden folder in the home directory called '.ssh'

$ mkdir .ssh

* Copy the file [config](./config) into the .ssh folder.

* Create ssh keys and add to the ssh agent:

$ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

$ ssh-add ~/.ssh/id_rsa

> Place public key on Github:

clip < ~/.ssh/id_rsa.pub

Login to github.com and navigate to Settings -> SSH and GPG keys.

Paste the public key in the space provided.

---
Notes:
The alias 'glog' has been added to bash_profile as an example. You may add and use what you desire.

---
References:

https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent#platform-windows

https://help.github.com/en/articles/adding-a-new-ssh-key-to-your-github-account


