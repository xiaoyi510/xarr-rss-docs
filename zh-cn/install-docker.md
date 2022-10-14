# Docker 安装

XArr-Rss Dokcer 镜像仓库: [xiaoyi510/xarr-rss](https://hub.docker.com/r/xiaoyi510/xarr-rss)

## 安装命令

```shell
# 拉取镜像
docker pull xiaoyi510/xarr-rss
# 创建容器
docker run -d --name xarr-rss --add-host=api.themoviedb.org:108.156.91.21 -e TZ=Asia/Shanghai -p 8086:8086 -v <你的本地路径>:/app/conf --restart unless-stopped xiaoyi510/xarr-rss:latest
```

记得修改<你的本地路径>哦

**Dokcer 配置**

| 容器配置      | 主机配置   | 类型   |
|-----------|--------|------|
| 8086      | 您的端口号  | 端口   |
| /app/conf | 您的本地路径 | 目录映射 |

安装完成 访问 <http://主机:端口号> 即可进入配置中心

**Docker Compose**

```dockerfile
version: "2.1"
services:
  xarr-rss:
    image: xiaoyi510/xarr-rss:latest
    container_name: xarr-rss
    environment:
      - TZ=Asia/Shanghai
    volumes:
      - /mnt/user/appdata/xarr-rss:/app/conf
    ports:
      - 8086:8086
    restart: unless-stopped
```