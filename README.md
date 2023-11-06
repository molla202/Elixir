# Elixir


sudo apt-get update
sudo apt-get install ca-certificates curl gnupg lsb-release

sudo mkdir -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

sudo apt-get update

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


wget https://files.elixir.finance/Dockerfile

nano Dockerfile

ENV ADDRESS=YOUR ADDRESS HERE 
ENV PRIVATE_KEY=YOUR PRIVATE KEY HERE
ENV VALIDATOR_NAME=YOUR DISCORD HANDLE HERE

docker build . -f Dockerfile -t elixir-validator
docker pull elixirprotocol/validator:testnet-2
docker run -d --restart unless-stopped --name ev elixir-validator

docker logs container-name -f


https://dashboard.elixir.finance/

![image](https://github.com/molla202/Elixir/assets/91562185/e13722d8-fc45-4428-a48e-877298bc5592)

![image](https://github.com/molla202/Elixir/assets/91562185/baf5f2b9-d5f3-4ce4-9ff5-138a63be2569)

![image](https://github.com/molla202/Elixir/assets/91562185/53cdc0e9-830d-451e-b223-9661281bcc6b)




