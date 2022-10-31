Simple CRUD MERN WSL
========================================

This is a basic CRUD with MERN (MongoDB, Express, React, Nodejs) tech stack. The backend (server) running on WSL (Windows Subsystem on Linux) with using Ubuntu distro in this case.

*Special thanks to M. Fikry Setiadi for his amazing work in https://mfikri.com/artikel/mern-stack-crud*

Requirements
-------------------
- Windows 11 build number higher than 22000
- WSL 0.67.2 and above
- Ubuntu on WSL2 

Why Windows 11?
-------------------
Linux systemd only supported on WSL 0.67.2 and above, this package only available on Windows 11. So, goodbye Windows 10.

Server Setup (WSL)
-------------------
- Install [Ubuntu on WSL2](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-11-with-gui-support), do until step 4 only.
- Open Windows Terminal
```shell
ubuntu
```
- Enable systemd
```shell
sudo -e /etc/wsl.conf
```
- Add this into systemd
```shell
[boot]
systemd=true
```
- shutdown ubuntu
```shell
sudo poweroff
```
- shutdown wsl
```shell
wsl --shutdown
```
- restart ubuntu
```shell
ubuntu
```
- check if systemd running
```shell
sudo systemctl status
```
- install [Node.js version 18](https://joshtronic.com/2022/04/24/how-to-install-nodejs-18-on-ubuntu-2004-lts) manually
- install [MongoDB on WSL](https://dev.to/seanwelshbrown/installing-mongodb-on-windows-subsystem-for-linux-wsl-2-19m9) manually

Start Basic MERN Stack
-------------------
- clone [this repo](https://github.com/arifinssu/crud-mern-wsl)
- open 2 windows terminals. one for client side, and another for server side
- on server side
```shell
cd server
npm install
npm install -g nodemon
nodemon index
```
- on client side
```shell
cd client
npm install
npm start
```

License Information
-------------------

This is an _**open source**_ project! 
Please review the [LICENSE.md](LICENSE.md) file for license information. 