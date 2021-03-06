使用方法
```
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=install' --tags install
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=configure' --tags configure
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=start' --tags start
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=restart' --tags restart
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=stop' --tags stop
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=stop' --tags enable
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class2_nginx" -e 'acname=stop' --tags disable
```

使用 kafka 的主机做测试
```
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class_kafka" -e 'acname=install' --tags install
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class_kafka" -e 'acname=configure' --tags configure
$ ansible-playbook -i contrib/ec2.py nginx.yml -e "nginx_tag=class_kafka" -e 'acname=start' --tags start
```

使用 curl 发送 post 数据
```
curl -H "Content-Type: application/json" -d '{"object_kind":"merge_request"}' http://localhost/app
```

[openresty 最佳实践](https://moonbingbing.gitbooks.io/openresty-best-practices/ngx_lua/phase.html)
[nginx 接收 post 请求](http://blog.csdn.net/yangguanghaozi/article/details/52367118)