# bsp-env
![Build](https://github.com/guerinoni/bsp-env/workflows/Build/badge.svg)

This repo allows to create a docker container for BSP development based on Ubuntu with Yocto or Buildroot.

### Preparation
Rename the `ENV USER_NAME rcc` username environment with your username.

### Build the image
```bash
docker build --build-arg "host_uid=$(id -u)" --build-arg "host_gid=$(id -g)" -t bsp-env -f <filename> .
```

### Create the container
```bash
docker run -it --privileged -v $(pwd):/home/host --name <your-conatiner-name> bsp-env
```

### Start the container
```bash
docker start -i <your-conatiner-name>
```