# V2Ray
# 安装 V2Ray 配置 WebSocket+Nginx+TLS #
V2Ray 官网
V2Ray 白话文教程

- **一、V2Ray**
	1. 更新源
	2. 安装 curl
	3. 配置 V2Ray
	4. 修改 V2Ray 配置
	5. 启动 V2Ray

----------

- **二、域名与证书**
	1. 安装 socat
	2. 安装 acme.sh
	3. 生成证书
	4. 移动证书到配置目录

----------

- **三、Nginx**
	1. 安装 Nginx
	2. 配置 Nginx
	3. 修改 Nginx 配置
	4. 重启 Nginx

----------

- **V2Ray 命令**
## 一、V2Ray ##
1. 更新源

    `apt-get update`

2. 安装 curl

    `apt-get install curl`

3. 配置 V2Ray

    `vim /etc/v2ray/config.json`

4. 修改 V2Ray 配置

5. 启动 V2Ray

    `systemctl start v2ray`
## 二、域名与证书 ##
1. 安装 socat

    `apt-get install socat`

2. 安装 acme.sh

    `curl  https://get.acme.sh | sh`

3. 生成证书

    `~/.acme.sh/acme.sh --issue -d smalltoe.ooo --standalone -k ec-256`

4. 移动证书到配置目录

    `~/.acme.sh/acme.sh --installcert -d smalltoe.ooo --fullchainpath /etc/v2ray/v2ray.crt --keypath /etc/v2ray/v2ray.key --ecc`
## 三、Nginx ##
1. 安装 Nginx

    `apt-get install nginx`

2. 配置 Nginx

    `vim /etc/nginx/sites-available/default`

3. 修改 Nginx 配置
	> 在 Nginx 最下面添加以下配置

4. 重启 Nginx

    `service nginx restart`
## V2Ray 命令 ##
1. 启动 V2Ray

    `service v2ray start`

2. 停止 V2Ray

    `service v2ray stop`

3. 状态 V2Ray

    `service v2ray status`

4. 重装 V2Ray

    `service v2ray reload`

5. 重启 V2Ray

    `service v2ray restart`
