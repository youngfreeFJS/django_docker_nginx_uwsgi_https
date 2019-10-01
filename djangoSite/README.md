# django docker compose with mysql



## 安装和配置
```bash
# 编辑环境变量
$ mv env.env .env
$ vim .env

# 编译 Docker 镜像 
$ docker-compose build web

# 安装依赖环境和迁移数据库
$ docker-compose run web pipenv install --dev
$ docker-compose run web python manage.py migrate
```

## 直接运行 django，开发调试模式(dev//生产模式 prod )
```bash
$ docker-compose run -p 8080:8080 web dev
```
## 直接运行 nginx
```
docker-compose run -p 1443:443 nginx
```
## 直接运行
```bash
docker-compose up
```

## 其他注意事项
- 替换nginx.conf 的 serviceName 为 域名 ； ssl文件夹下放入crt文件和key文件，并修改nginx.conf文件内容
- 在系统 hosts 中把 www.example.com 指向docker所在的ip
- 访问 <https://www.example.com>
- 众所周知的原因，国内访问国际服务速度感人
  - [Docker - 国内镜像的配置及使用](https://www.cnblogs.com/anliven/p/6218741.html)
  - [清华大学开源软件镜像站 - pypi](https://mirrors.tuna.tsinghua.edu.cn/help/pypi/)

如有问题，联系：471011042@qq.com
  
  


