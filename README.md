# MNNIT_Proxy_Setups
Setup Proxy for terminals and more difficult places! (which are not directly accessible!)

Updates to this repo is welcome! Please create a **PR** to merge changes, or open an **Issue** to help us add more data to this repo!


## Quick Access
  - [Windows 11](#windows-11)
  - [Windows 10](#windows-10)
  - [Ubuntu](#ubuntu)
  - [Git](#git)
  - [Linux Terminal](#linux-terminal)
  - [MSYS2](#msys2)
  - [Node](#node)

<hr>

## Windows 11
**Settings** > **Network & Internet** > **Proxy** > **Manual proxy setup** > **Edit**

1. Toggle **Use a proxy server** to **On**
2. Proxy IP address - ```172.31.102.29```
3. Port - ```3128```
4. Click **Save**

<hr>

## Windows 10
**Settings** > **Network & Internet** > **Proxy** > **Manual proxy setup**

1. Toggle **Use a proxy server** to **On**
2. Address - ```172.31.102.29```
3. Port - ```3128```
4. Click **Save**

<hr>

## Ubuntu
**Settings** > **Network** > **Network Proxy**

1. Click on **Gear** icon
2. Choose **Manual**
3. HTTP Proxy - ```172.31.102.29``` & ```3128```
4. HTTPS Proxy - ```172.31.102.29``` & ```3128```
5. FTP Proxy - ```172.31.102.29``` & ```3128```
6. Sockets Host - ```172.31.102.29``` & ```3128```
7. Close the pop-up.

<hr>

## Git
Open command prompt (in Windows) and run the following commands one by one

1. ```git config --global --unset-all https.proxy```
2. ```git config --global --unset-all http.proxy```
3. ```git config --global --add http.proxy http://edcguest:edcguest@172.31.102.29:3128```
4. ```git config --global --add https.proxy http://edcguest:edcguest@172.31.102.29:3128```

<hr>

## Linux Terminal
Open terminal (in Linux) and follow the steps below:

1. Run ```sudo -i```
2. Enter your root password (password is not visible while typing in linux terminal)
3. Run ```gedit /etc/apt/apt.conf```
4. Write ```Acquire::http::Proxy "http://edcguest:edcguest@172.31.102.29:3128";``` and **Save** and then **Close** the text editor
5. Run ```gedit /etc/bash.bashrc```
6. Write the following at the bottom of the file.
```
export http_proxy=http://edcguest:edcguest@172.31.102.29:3128/

export ftp_proxy=http://edcguest:edcguest@172.31.102.29:3128/

export https_proxy=https://edcguest:edcguest@172.31.102.29:3128/
```
7. **Save** and **Close** the text editor.
8. **Close** the terminal.

<hr>

## MSYS2
Open **MSYS2 MSYS** prompt (in Windows) and run the following commands one by one

1. ```export HTTP_PROXY="edcguest:edcguest@172.31.102.29:3128"```
2. ```export HTTPS_PROXY=$HTTP_PROXY```
3. ```export http_proxy=$HTTP_PROXY```
4. ```export https_proxy=$HTTP_PROXY```

<hr>

## Node
Run these commands one by one in command prompt.
Make sure **Node is Installed** and added to path.

1. ```npm config set proxy http://edcguest:edcguest@172.31.102.29:3128```
2. ```npm config set https-proxy http://edcguest:edcguest@172.31.102.29:3128```


More help [here](https://www.jhipster.tech/configuring-a-corporate-proxy/).

<hr>

