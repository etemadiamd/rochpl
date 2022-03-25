# rocHPL container based on ROCm 5.0.2 GA and Ubuntu 20.04

## Commands to build the rocm 5.0.2 ga container based on Ubuntu 20.04:
```
wget https://github.com/etemadiamd/rochpl/blob/main/rocm502/BaseDockerfile
sudo docker build -t rocm502ga-ubuntu20:latest -f BaseDockerfile .
#run the container
sudo docker run -it --privileged --ipc=host --network=host --device=/dev/kfd --device=/dev/dri -v ~:/datadisk-docker --group-add video  --security-opt seccomp=unconfined amddcgpuce/rocm502ga-ubuntu20:latest /bin/bash
``` 
## Commands to build and run the rocHPL based on ROCm 5.0.2 GA
```
wget https://github.com/etemadiamd/rochpl/blob/main/rocm502/rocHPL502gaDockerfile
sudo docker build -t rochpl-rocm502ga-ubuntu20:latest -f rocHPL502gaDockerfile .
#run the container
sudo docker run -it --privileged --ipc=host --network=host --device=/dev/kfd --device=/dev/dri -v ~:/datadisk-docker --group-add video  --security-opt seccomp=unconfined amddcgpuce/rochpl-rocm502ga-ubuntu20:latest /bin/bash
```

