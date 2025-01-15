# First Time Using the Server

## SSH Connection
Please refer to: [https://dku-mp-zhang-group.github.io/docs/#/./server%20users/firsttime/ssh_example](https://dku-mp-zhang-group.github.io/docs/#/./server%20users/firsttime/ssh_example)

## Network Proxy
On this server, there is no default global proxy setting. Most of the time, domestic mirrors can be used for faster downloads. For information on how to switch Python or conda mirrors, please refer to the relevant documentation.

To set the Duke proxy, run:
```shell
setprpxy
```

If you want to cancel or if you encounter any network (proxy) related errors with keywords like "proxy," "ProtocolError," or "403," please try:
```shell
unsetprpxy
```

## Changing Software Sources
Note: In this setup, we use the mirror services provided by Shanghai Jiao Tong University. If you need to use other mirrors, please search for them.

### Python
```shell
pip config set global.index-url https://mirror.sjtu.edu.cn/pypi/web/simple
```

### Anaconda/Miniconda
Edit `~/.condarc`
```shell
default_channels:
  - https://mirror.sjtu.edu.cn/anaconda/pkgs/r
  - https://mirror.sjtu.edu.cn/anaconda/pkgs/main
custom_channels:
  conda-forge: https://mirror.sjtu.edu.cn/anaconda/cloud/
  pytorch: https://mirror.sjtu.edu.cn/anaconda/cloud/
channels:
  - defaults
```