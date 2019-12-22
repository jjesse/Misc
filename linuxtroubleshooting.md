git# Setting up Remote Inspection of Linux Devices
Forescout can inspect Linux devices remotely via SSH and there is some confusion in the documentation on how to set this up. This is done via a trusted ssh key. This guide will cover two ways:
- Manual deployment
- Scripted deployment

NOTE: This information was provided to the Slack Forescout Community and put together for all to see/use.

## Manual Deployment of the SSH Keys
## Scripted Deployment of the SSH Keys




useradd fsuser
passwd fsuser  #make it the same as from the linux plugin
mkdir /home/fsuser/.ssh
echo "<ssh public key from console>" > /home/fsuser/.ssh/authorized_keys
chmod 600 /home/fsuser/.ssh/authorized_keys
chmod 700 /home/fsuser/.ssh


/usr/local/forescout/plugin/linux/ssh/keys/ssh_key.pub 

[root@counteract ~]# ssh -i /usr/local/forescout/plugin/linux/ssh/keys/ssh_key fsuser@192.168.10.250