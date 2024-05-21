#### 13-Artificial-Intelligence

## Installing ollama on Ubuntu 
sudo apt update
sudo apt upgrade
sudo apt install build-essential dkms
curl -fsSL https://ollama.com/install.sh | sh


### Add the NVIDIA package repository to get the latest drivers:

sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt update


### Run localy 
http://localhost:11434/


### Add models to ollama

ollama pull llama2


### Check performance of the model
watch -n 0.5 nvidia-smi
