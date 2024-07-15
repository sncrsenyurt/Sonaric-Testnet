# Sonaric

> After installing Node, our sonaric scores will come in real-time.

> They said they are still working on an incentive program..

> There is no guarantee that our scores will be rewarded - we are just inside as RC.

> We have no server costs; we will use one of our existing servers.

#

# Hardware.

> We need Ubuntu 22 or later.

> I used one of the devices where I actively installed Node.

> However, if you are going to buy a new server, 2 vCPU and 2 RAM will be sufficient.

#

# Setup

```console
# sunucu update
sudo apt-get update && sudo apt-get upgrade -y

# install nodejs using nvm 
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"
nvm install 20
nvm use 20
npm install -g npm@latest

# sonaric install
sh -c "$(curl -fsSL https://raw.githubusercontent.com/monk-io/sonaric-install/main/linux-install-sonaric.sh)"
````

> `sonaric node-info` If we get node information output with the command, it is ok.

<img width="661" alt="Ekran Resmi 2024-07-03 12 29 31" src="https://github.com/ruesandora/Sonaric/assets/101149671/a61730fe-2fd7-4e34-a802-41158e24f6ee">

#

```console
# update
sudo apt update
sudo apt upgrade sonaric
sonaric node-info
```

```console
# edit the end of code.
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
# If you are using root as user, type root.
```

> To understand that the above command works: `curl http://localhost:44004`

<img width="874" alt="Ekran Resmi 2024-07-03 12 37 19" src="https://github.com/ruesandora/Sonaric/assets/101149671/d23fa136-1889-4f1c-b90d-930ce53c67ce">

```console
sonaric identity-export -o node-ismi.identity
# delete the node-name and set a name.
# enter your password.
````

> You can download the backup file on our server via SFTP (File) connection applications or via Termius (Mac - Windows - Phone), Mobaxterm.

If Termius, you entered SFTP - you selected your server, dragged the xxxx.identy file on your server and copied it to the file you want on your own computer - you downloaded it.

![image](https://github.com/ruesandora/Sonaric/assets/141464235/27431eba-c1a0-4dad-8dff-edf0ec429a70)


> For Backup (Pub ID - Priv Key - Key - Key - Key PW when setting through the site)

We will tunnel between the node and our PC. 

```console
ssh -L 127.0.0.1:44003:127.0.0.1:44003 -L 127.0.0.1:44004:127.0.0.1:44004 -L 127.0.0.1:44005:127.0.0.1:44005 -L 127.0.0.1:44006:127.0.0.1:44006 user@your-vps-ip
```

Set the User - And IP Address according to your server, paste it into CMD and enter your server. The tuner will be active as long as CMD stays open. 

From your browser: http://localhost:44004/ - Go to the address - You will see your node's score - your ranking. 

There will be a settings button at the top center right - Click on the Export button - Set your password and confirm it, it will now give you your keys. Save it and then press save to json file to save the json file to your computer.

![image](https://github.com/ruesandora/Sonaric/assets/141464235/2a2c9b7b-e75c-4c8f-ada4-1559c13af1c0)


#

> We can see our points with `sonaric points`.

<img width="276" alt="Ekran Resmi 2024-07-03 12 39 26" src="https://github.com/ruesandora/Sonaric/assets/101149671/fe2aea28-99ea-45ae-948f-5b6a23a9e116">










