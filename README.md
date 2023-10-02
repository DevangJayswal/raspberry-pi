# RASPBERRY PI RESOURCES
## Commands
### Update and upgrade 
`sudo apt update && sudo apt upgrade -y`
### Remote Desktop
  Server: xrdp: `sudo apt install xrdp`
    Refer to Issues in this repository if you've problem login with xrdp.
    
  Client: Remmina: `sudo apt install remmina`

### Add remove .deb
`dpkg -l` or `dpkg -l | grep <package_name>`

`sudo apt install ./<deb package>`

### Check Raspberry Pi OS information
`lsb_release -a`

### SDKMan
https://sdkman.io/

`curl -s "https://get.sdkman.io" | bash`

`source "$HOME/.sdkman/bin/sdkman-init.sh"`

`sdk install java 21-oracle`
