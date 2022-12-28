# Bittorrent Kit

## 预装内容

- qBittorrent（供pt用)
- qBittorrent Enhanced Edition （下载公网种用）
- caddy（反代后面两个qbt，再配合basicauth鉴权）

## 使用说明

1. 安装`podman`和`git`
2. clone本项目
3. 运行`podman play kube podman-btkit.yaml`
4. 访问38080端口，用户名密码`admin/ad@min`

## FAQ
1. 如果需要绑定域名怎么办  
   暴露443端口，修改caddyfile加上你的域名
2. 怎么修改密码  
   运行`caddy hash-password`生成一个新的密码hash，修改caddyfile第三行后面的hash