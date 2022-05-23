Install OVH Ubuntu 22.04

ssh into it
Update stuff

`sudo apt-get update`
`sudo apt-get upgrade`

Install deps

`sudo apt-get install libcurl4`

`sudo apt-get install net-tools`

Need to add repo for 22.04 to install libssl1

`echo "deb http://security.ubuntu.com/ubuntu impish-security main" | sudo tee /etc/apt/sources.list.d/impish-security.list`
`sudo apt-get update`
`sudo apt-get install libssl1.1`

Make folders

`cd /home`
`cd ubuntu`
`mkdir reforger`
`cd reforger`
`mkdir profile`
`mkdir configs`

Install steamcmd

```
sudo add-apt-repository multiverse
sudo dpkg --add-architecture i386
sudo apt update
sudo apt install lib32gcc-s1 steamcmd
```

Change steamcmd install directory

`steamcmd`
`force_install_dir /home/ubuntu/reforger/`

Login as anonymous

`login anonymous`

Install Reforger Server (will take a bit)

`app_update 1874900`

Leave steamcmd
`exit`

Make ArmaReforgerServer executable

`chmod +x ArmaReforgerServer`

Copy Basic.json into /home/ubuntu/reforger/configs

Copy run.sh into /home/ubuntu/reforger

Make run.sh executable

`chmod +x run.sh`

Run server!

`./run.sh`