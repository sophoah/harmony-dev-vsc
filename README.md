# Harmony Go Dev environment

## Description

This is a project to help setup the development environment for GO development on the Harmony one blockchain (<https://github.com/harmony-one/harmony/>) with Visual Studio code on a windows machine

## Pre requesites

All the below needs to be installed on your host system:

- Visual studio code : <https://code.visualstudio.com/> with the following extension to be installed:
  - go
  - Remote - Containers
  - Remote development
- Docker : <https://www.docker.com/products/docker-desktop>
- git for windows : <https://git-scm.com/download/win>

Go binaries doesn't need to be installed on your host machine.

## How to use

From your host machine:

- git clone <https://github.com/sophoah/harmony-dev-vsc.git>
- edit the file .devcontainer/devcontainer.json to replace your host local path in

```json
"mounts": [
  "source=YOURDRIVE:/YOUR_LOCAL_PATH,target=/data,type=bind,consistency=cached"
],
```

this it to have a shared folder between your host and the container. I am putting here all the codes I am developping. The other reason is that the git push will be done from the host machine which has access to my SSH private keys.

- Open VSC and click on the green button in the bottom left
- Click on "Open folder in container" and chosse the directory we just clone and modified
- the container should now be in process to be built
- once done you can now add new folder (project) to be edited by right clicking in the VSC explorer and chosse "add Folder to Workspace ..." (under /data you'll have all your project that was shared above)
