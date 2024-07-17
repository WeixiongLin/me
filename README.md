# README

- [README](#readme)
  - [Install Jekyll with Docker](#install-jekyll-with-docker)
  - [Homepage Deploy](#homepage-deploy)
  - [参考资料](#参考资料)


## Install Jekyll with Docker

```bash
docker pull do.nark.eu.org/jekyll/jekyll
docker build -t homepage:v1 .

docker compose up
docker exec -it $container_id /bin/bash

```

## Homepage Deploy


```bash
git clone --bare https://github.com/RayeRen/acad-homepage.github.io.git
git push git@github.com:WeixiongLin/me.git main
rm -rf jekyll-docker
git clone git@github.com:WeixiongLin/me.git

```

进入之后执行

```bash
bundle config mirror.https://rubygems.org https://gems.ruby-china.com
bundle install
bundle add webrick
bundle exec jekyll liveserve --port 4000
```



## 参考资料

- [acad homepage](https://github.com/RayeRen/acad-homepage.github.io)
- [国内如何下载 Docker Image](https://blog.csdn.net/weixin_50160384/article/details/139861337)
