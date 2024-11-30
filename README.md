```shell
brew install localstack/tap/localstack-cli
pip install aws-sam-cli-local


export LOCALSTACK_API_KEY=ls-PovU6716-jirA-SiSu-jIrA-WAfi26280c6a

export DNS_ADDRESS=0 && \
export LS_LOG=trace && \
export DEBUG=1 && \
localstack stop; \
docker stop $(docker ps -a -q); \
docker rm $(docker ps -a -q); \
docker volume prune --force;
localstack start -d


cd in git@github.com:PrettySolution/sam-app-java11.git
samlocal deploy
```