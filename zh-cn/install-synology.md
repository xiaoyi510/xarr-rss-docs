# 群晖安装


## 下载镜像
1. 打开Dokcer
2. 打开注册表
3. 搜索 xarr-rss
4. 双击下载镜像
    ![img](../assets/install_sy_1.png)

## 创建容器
1. 进入映像
2. 双击xarr-rss
3. 进行创建
![img](../assets/install_sy_2.png)

4. 设置容器目录
    
    点击高级设置-存储空间 添加目录映射 容器内的目录为/app/conf
    ![img.png](../assets/img.png)

5. 设置端口
   
    填写本地端口`为你的主机使用的端口` 和 容器端口 `8086` 类型 `TCP`
    ![img_1.png](../assets/img_1.png)

6. 设置完成 下一步就行了
