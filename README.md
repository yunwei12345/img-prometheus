# img-prometheus- node-exporter  granafa


#  镜像信息

  https://cr.console.aliyun.com/repository/cn-beijing/meowbitee/prometheus/build
	
	
  registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:v1                  prometheus
	
	
  registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:v2                   node-exporter
	
	
  registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:5.3.4                grafana
   
   
#  使用方法
 
   docker login --username=devops1 registry.cn-beijing.aliyuncs.com
	 
	 
   docker pull registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:v1
	 
   docker pull registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:v2
	 
   docker pull registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:5.3.4
    
   docker run -d -p 9090:9090 --name=prometheus registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:v1
	 
   docker run -d -p 9100:9100  registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:v2
	 
   docker run -d -p 3000:3000 --name=grafana registry.cn-beijing.aliyuncs.com/meowbitee/prometheus:5.3.4
   
   
   
#  docker-compose 管理

mkdir /opt/img-prometheus -p

cp docker-compose.yml /opt/prometheus/

docker-compose up
