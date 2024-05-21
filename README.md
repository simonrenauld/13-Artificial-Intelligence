# 13-Artificial-Intelligence Ollama

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
ollama run llama2



### Check performance of the model
watch -n 0.5 nvidia-smi


## add Open AI in a Docker Container

# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin

# run in docker

sudo docker run -d --network=host -v open-webbui:/app/backend/data -e OLLAMA_BASE_URL=http://127.0.0.1:11434 --name open-webui --restart always ghcr.io/open-webui/open-webui:main
### to see what is running
sudo docker ps
![Uploading image.png…]()


AWS Environment Cost Calculations
1 endpoint x 1 instance per endpoint x 24 hours per day x 30 days per month = 720.00 SageMaker Real-Time Inference hours per month 720.00 hours per month x $2.03 per hour instance cost = $1,461.60 (monthly On-Demand cost).

Total cost for Inference (monthly): $1,461.60

Here is the link to the AWS Cost Estimation Report: AWS Cost Estimate

