1����docker-compose.yml ��������
docker-compose up -d

2 ����webgui(ֻ����һ̨��������ִ��)
��������ssmgr 
ssmgr -c webgui.yml


ss�����
docker run -d \
      -u root \
	  --name="shadowsocks-libev" \
	  --network=host \
	  shadowsocks/shadowsocks-libev:v3.2.5 \
	  ss-server -s 0.0.0.0 -p 22 -k 1234,abcd -m aes-256-cfb -u

