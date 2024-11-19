```
{
    "log": {
      "level": "info",
      "output": "stdout"
    },
    "outbounds": [
      {
        "type": "hysteria2",
        "server": "193.32.148.226",
        "server_port": 4406,
        "up_mbps": 100,
        "down_mbps": 100,
        "password":"7788421",
        "tls": {
          "enabled": true,
          "server_name": "bing.com",
          "insecure": true
        }
      }
    ],
    "inbounds": [
      {
        "type": "socks",
        "tag": "socks-in",
        "listen": "127.0.0.1",
        "listen_port": 1086
      },
      {
        "type": "http",
        "tag": "http-in",
        "listen": "127.0.0.1",
        "listen_port": 9876
      }
    ]
  }
  
```
