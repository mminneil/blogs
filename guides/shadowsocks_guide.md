# Installtion Guide for Shadowsocks

## Server

* **Update System**

```bash
    apt update
    apt upgrade
```

* **Install Python Dependencies**

```bash
    apt install python-pip
    apt install python-setuptools
```

* **Install Shadowsocks Server**

```bash
    pip install shadowscoks
```

* **Add Shadowsocks Configuration**

```bash
    vim /etc/shadowsocks.json

    {
        "server": "45.76.51.55",
        "local_address": "127.0.0.1",
        "local_port": "1080",
        "port_password":{
            "12225":"maomaomin"
        },
        "timeout":600,
        "method":"aes-256-cfb",
        "fast_open":false
    }
```

* **Start Shadowsocks Server**

```bash
    ssserver -c /etc/shadowsocks.json -d start
```

## Client

* **Configuration**

```bash
    {
        "server":"45.76.51.55",
        "server_port":12225,
        "password":"maomaomin",
        "timeout":600,
        "method":"aes-256-cfb"
    }
```