# How to install Nodejs on Ubuntu
A simplified guide on the basics of how to setup your Ubuntu Server to run Nodejs from the downloaded binary

## 1. Download the binary archive
> #### [`Download Here`](https://nodejs.org/en/download/)

## 2. In the terminal, set the `VERSION` and `DISTRO` variables to match the binary archive file name.
```
 VERSION=v10.15.0
 DISTRO=linux-x64
```
## 3. Unzip the archive to any directory
```
 sudo mkdir -p /usr/local/lib/nodejs
 sudo tar -xJvf node-$VERSION-$DISTRO.tar.xz -C /usr/local/lib/nodejs 
```
## 4. Create the -s link to the binaries:
```
sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/node /usr/bin/node
sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/npm /usr/bin/npm
sudo ln -s /usr/local/lib/nodejs/node-$VERSION-$DISTRO/bin/npx /usr/bin/npx
```
## 5. Test installation
```
$ node -v
$ npm version
$ npx -v
```
