# Harmony Dev environment

## Description
This is a project to help setup the development environment for developping on Harmony blockchain code with Visual Studio code on a windows machine

## Pre requesites
- Visual studio code installed on your system : https://code.visualstudio.com/ with the following extension to be installed :
  - go 
  - Remote - Containers
  - Remote development
- Docker


# How to use
- git clone https://github.com/sophoah/harmony-dev-vsc.git
- edit the file .devcontainer/devcontainer.json to replace your host local path in 
```
  	"mounts": [
		"source=YOURDRIVE:/YOUR_LOCAL_PATH,target=/data,type=bind,consistency=cached"
	],
```
this it to have a shared folder between your host and the container. I am putting here all the codes i am developping
- Open VSC and click on the green button in the bottom left
- Click on "Open folder in container" and chosse the directory we just clone and modified
- the container should now be in process to be built
- once done you can now add new folder (project) to be edited by right clicking in the VSC explorer and chosse "add Folder to Workspace ..." (under /data you'll have all your project that was shared above)