# My Python Dev Environment

## Pre-requisites
1. Docker

## Quick Usage
The image can be pulled from the hub using the following command.

```
docker pull rap999a/python-dev-env:latest
```
While you can connect to the container using vscode (make sure you have this [extension](https://code.visualstudio.com/docs/devcontainers/containers)), for persisting the data after your container is shutdown, use volumes. The best way to go about this would be to attach a volume.

## Build
```
git clone https://github.com/rohanpurekar/py-dev-env.git
cd py-dev-env
docker build -t <image name>
docker run --name <container-name> -p 8000:8000 -d -v ${pwd}:/code <image name>
```

## Usage
Once you connect a volume, just open vscode, click "open remote window" button on the bottom left corner. Select "attach to existing container" and choose the container that you just created with the attached volume. 

Start building.

