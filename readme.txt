1运行docker-compose.yml 生成容器
docker-compose up -d

2 启动webgui(只需在一台服务器上执行)
进入容器ssmgr 
ssmgr -c webgui.yml


ss单机搭建
docker run -d \
      -u root \
	  --name="shadowsocks-libev" \
	  --network=host \
	  shadowsocks/shadowsocks-libev:v3.2.5 \
	  ss-server -s 0.0.0.0 -p 22 -k 1234,abcd -m aes-256-cfb -u

