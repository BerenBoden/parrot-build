** Make sure to pip install ansible, apt has an older copy **

# Instructions
* Start with Parrot HTB Edition
* Install Ansible (pip3 install ansible)
* Clone and enter the repo (git clone)
* ansible-galaxy install -r requirements.yml
* Make sure we have a sudo token (sudo whoami)
* Disable host key checking for cloning repos with SSH (export ANSIBLE_HOST_KEY_CHECKING=False)
* Add github to known hosts (ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts)
* Add the SSH keys for private repos (ssh-add ~/.ssh/github)
* Run the playbook (ansible-playbook main.yml --ask-become-pass)

# Off-Video Changes
* Mate-Terminal Colors, I show how to configure it here (https://www.youtube.com/watch?v=2y68gluYTcc). I just did the steps in that video on my old VM to backup the color scheme, then copied it to this repo.
* Evil-Winrm/Certipy/SharpCollection/CME/Impacket, will make a video for these soon
* Updated BurpSuite Activation. Later versions of ansible would hang if a shell script started a process that didn't die. Put a timeout on the java process
