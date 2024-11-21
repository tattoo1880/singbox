```
{
    "dns": {
      "servers": [
        {
          "tag": "google",
          "address": "tls://8.8.8.8"
        },
        {
          "tag": "local",
          "address": "223.5.5.5",
          "detour": "direct"
        }
      ],
      "rules": [
        {
          "outbound": "any",
          "server": "local"
        }
      ]
    },
 "inbounds": [
    {
      "type": "tun",
      "inet4_address": "198.18.0.1/16",
      "auto_route": true,
      "stack": "mixed",
      "sniff": true
    },
    {
      "type": "socks",
      "tag": "socks-in",
      "listen": "::",
      "listen_port": 5353
    }
  ],
    "outbounds": [
       
              {
                "type": "hysteria2",
                "server": "193.32.150.11",
                "server_port": 443,
                "up_mbps": 100,
                "down_mbps": 100,
                "password": "7788421",
                "tls": {
                  "enabled": true,
                  "server_name": "bing",
                  "insecure": true
                }
              },
         
      {
        "type": "direct",
        "tag": "direct"
      },
      {
        "type": "dns",
        "tag": "dns-out"
      }
    ],
    "route": {
      "rules": [
        {
          "protocol": "dns",
          "outbound": "dns-out"
        },
        {
          "geoip": [
            "private"
          ],
          "outbound": "direct"
        }
      ],
      "auto_detect_interface": true
    }
  }
```
