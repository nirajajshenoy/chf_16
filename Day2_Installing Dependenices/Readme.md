# Installing the Dependencies

Note: If any of the following dependencies are available on your laptop, then no need to install it.

## Update Packages

In case of a fresh Ubuntu 22 installation, use the following command to update the packages before installing other dependencies.  
```
sudo apt update

sudo apt upgrade
```

## Visual Studio Code
Download and install the latest version of VS code from here: https://code.visualstudio.com/download

(or)

Use this command to install VS Code
```
wget "https://code.visualstudio.com/sha/download?build=stable&os=linux-deb-x64" -O vscode.deb
```

To install, either launch it by providing execution permission, or execute the following command from the same folder where VS Code is being downloaded
```
sudo dpkg -i [filename]

sudo dpkg -i vscode.deb
```


## cURL
Install curl using the command
```
sudo apt install curl -y

curl -V
```

## Git
Install git using the command
```
sudo apt install git -y
```

## NVM

**Note**: If **Method 1** fails then follow **Method 2**.

**Method 1**

Install NVM (Node Version Manager), open a terminal and execute the following command.
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

```
Close the current terminal and open a new one.

In the new terminal execute this command to verify nvm has been installed

```
command -v nvm

```
**Method 2**

- Open the /etc/hosts file using 


```
sudo nano /etc/hosts

```
or

```
sudo gedit /etc/hosts

```

- Add the following IP address at the end of the file:


```
185.199.108.133 raw.githubusercontent.com

```

- Save and close the file.


```
source ~/.bashrc

```
To install NVM (Node Version Manager), execute the following command.
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

```
Close the current terminal and open a new one.

In the new terminal execute this command to verify nvm has been installed

```
command -v nvm

```

## NodeJS (Ver 18.x)

Execute the following command to install NodeJs
```
nvm install --lts
```  

Check  the version of nodeJS installed
```
node -v
```

Check  the version of npm installed
```
npm -v
```

## Docker

Step 1: Download the install script
```
curl -fsSL https://get.docker.com -o get-docker.sh
```
Step 2: Execute permission for the script
```
sudo chmod +x get-docker.sh
```
Step 3: Execute the script
```
./get-docker.sh
```
Step 4: Remove the script
```
rm get-docker.sh
```
Step 5: To manage Docker as a non-root user
```
sudo usermod -aG docker $USER
```
```
docker-compose --version
docker --version

```

## JQ
INstall JQ using the following command
```
sudo apt install jq -y
```

To verify the installtion enter the following command


```
jq --version
```

## Build Essential
Install Build Essential uisng the commnad
```
sudo apt install build-essential
```
To verify the installtion enter the following command


```
dpkg -l | grep build-essential

```


## Go
Step 1: Download Go
```
wget https://go.dev/dl/go1.24.2.linux-amd64.tar.gz
```
Step 2: Extract
```
sudo tar -C /usr/local -xzf go1.24.2.linux-amd64.tar.gz
```

Step 3: Add /usr/local/go/bin to the PATH environment variable. Open the /etc/environment file
```
sudo gedit /etc/environment
```
Or
```
sudo nano /etc/environment
```
Step 4: Append the following to the end of `PATH` variable and save
```
:/usr/local/go/bin
```

To verify the installtion enter the following command


```
go version

```


## Restart
Finally, restart the system to make the changes permanent.

**Install Minifab**

```
curl -o minifab -sL https://tinyurl.com/yxa2q6yr && chmod +x minifab

sudo cp minifab /usr/local/bin

minifab
```
