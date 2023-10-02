# RASPBERRY PI RESOURCES (Raspberry Pi OS 64 bit)
## Commands

### Set root user password
On Raspberry Pi OS, the root account is disabled by default, so there is no default password.
In order to set new root user password, use `sudo passwd root`

### Update and upgrade 
`sudo apt update && sudo apt upgrade -y`
### Remote Desktop
  Server: xrdp: `sudo apt install xrdp`
    Refer to Issues in this repository if you've problem login with xrdp.
    
  Client: Remmina: `sudo apt install remmina`

### Add remove program
`dpkg -l` or `dpkg -l | grep <package_name>`

`sudo apt install ./<deb package>`

`sudo apt remove ./<deb package>`

`sudo apt purge ./<deb package>`

`sudo apt autoremove` Remove automatically all unused packages

### Service
`service --status-all`

### Install samba
`sudo apt install samba`

`sudo useradd raspi-samba`

`sudo smbpasswd -a raspi-samba`

Open `smb.cong` file `sudo nano /etc/samba/smb.conf` and add the config 
`[devang-hd]
path = /media/devang/Devang
writeable=Yes
create mask=0777
directory mask=0777
public=no
`

`sudo service smbd restart`


### Check Raspberry Pi OS information
`lsb_release -a`

### SDKMan
https://sdkman.io/

`curl -s "https://get.sdkman.io" | bash`

`source "$HOME/.sdkman/bin/sdkman-init.sh"`

`sdk install java 21-oracle`
