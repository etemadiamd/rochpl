# rocHPL container based on ROCm 5.0.2 GA and Ubuntu 20.04

## Command to build the container
```
wget https://github.com/etemadiamd/rochpl/blob/main/rocm502/BaseDockerfile
sudo docker build -t rocm502ga-ubuntu20:latest -f BaseDockerfile .
``` 
