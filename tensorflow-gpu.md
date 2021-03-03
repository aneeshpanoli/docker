```curl -s -L https://nvidia.github.io/nvidia-docker/gpgkey | sudo apt-key add -
curl -s -L https://nvidia.github.io/nvidia-docker/ubuntu20.04/nvidia-docker.list > /etc/apt/sources.list.d/nvidia-docker.list
sudo apt update && sudo apt -y install nvidia-container-toolkit

docker run --user 1001 --gpus all -it -p 8888:8888  -v "/home/aneesh/Docker/tfdocker/:/tf/tfdocker/" tensorflow/tensorflow:latest-gpu-jupyter bash
```
