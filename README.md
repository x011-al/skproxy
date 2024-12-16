# skproxy tcp://nikmir-28973.portmap.host:28973 => 8080
wget https://github.com/skypool-org/skypool-nimiq-miner/releases/download/v1.3.4/skypool-nimiq-proxy-v0.0.1-linux-x64.zip && unzip skypool-nimiq-proxy-v0.0.1-linux-x64.zip \
&& cd skypool-nimiq-proxy-v0.0.1-linux-x64 \
&& ./skypool-node-proxy

#miner
wget https://github.com/skypool-org/skypool-nimiq-miner/releases/download/v1.3.4/skypool-nimiq-v1.3.3-linux-x64.zip && unzip skypool-nimiq-v1.3.3-linux-x64.zip \
&& cd skypool-nimiq-v1.3.3-linux-x64 && rm config.txt && wget https://raw.githubusercontent.com/x011-al/skproxy/refs/heads/main/config.txt \
&& ./skypool-node-client
