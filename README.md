#环境说明
以下7台服务器配置均为：CentOS7.2+2G内存+2核处理器
     一台WEB服务器：172.16.10.1（tomcat+nginx+MariaDB+JDK+logstash）
     一台Redis服务器：172.16.10.2（Redis+JDK）
     一台logstash-server服务器：172.16.10.3（JDK+logstash）
     三台ES服务器：172.16.10.4+172.16.10.5+172.16.10.6（elasticsearch+JDK）
     一台kibana+grafana服务器：172.16.10.7（kibana+JDK+grafana）

启动：
	 按照每个服务器对应的IP去安装,全部安装完成之后再分别启动：
	 172.16.10.1：/server/application/logstash-5.3.0/bin/logstash -f /server/application/logstash-5.3.0/conf.d/full.conf
	 172.16.10.3: /server/application/logstash-5.3.0/bin/logstash -f /server/application/logstash-5.3.0/conf.d/full.conf
	 172.16.10.4-6: nohup /server/application/elasticsearch-5.3.0/bin/elasticsearch > /server/application/elasticsearch-5.3.0/logs/es.log 2>&1 &
	 