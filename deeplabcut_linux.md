# Installation manual - deeplabcut (fro Linux)

## Requirement

- Ubuntu (20.04.3 LTS)
- docker
- python 3.8.

## Procedure

### 1. Install docker
See https://docs.docker.com/install/ & for Ubuntu: https://docs.docker.com/install/linux/docker-ce/ubuntu/

### 2. Check docker works properly

```sh
$ sudo docker run hello-world
```

The output should be: 
```sh
Hello from Docker! This message shows that your installation appears to be working correctly.
```

### 3. Add your user to the docker group
```sh
$ sudo groupadd docker
$ sudo usermod -aG docker $USER
```

### 4. Install deeplabcut-docker
```sh
$ pip install deeplabcut-docker
```

### 5. Launch deeplabcut-docker gui
```sh
$ deeplabcut-docker gui
```

## Note
For the detailed info, see https://github.com/DeepLabCut/DeepLabCut/tree/master/docker