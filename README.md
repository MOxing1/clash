排除第一条链接（机场链接）⭐ 香港故转`fallback`!!GROUPID=!1!!  

subconverter后端  
http://localhost:25500/sub   openwrt本机docker地址  
https://sub.qichiyu.com/sub  VPS 域名反代 地址/  
http://192.168.10.5:25500/sub 局域网其他设备地址	  

DIRECT 直连
Proxy 代理
规则自定义：  
##- PROCESS-NAME,curl,DIRECT #匹配路由自身进程(curl直连)  
##- DOMAIN-SUFFIX,google.com,Proxy #匹配域名后缀(交由Proxy代理服务器组)  
##- DOMAIN-KEYWORD,google,Proxy #匹配域名关键字(交由Proxy代理服务器组)  
##- DOMAIN,google.com,Proxy #匹配域名(交由Proxy代理服务器组)  
##- DOMAIN-SUFFIX,ad.com,REJECT #匹配域名后缀(拒绝)  
##- IP-CIDR,127.0.0.0/8,DIRECT #匹配数据目标IP(直连)  
##- SRC-IP-CIDR,192.168.1.201/32,DIRECT #匹配数据发起IP(直连)  
##- DST-PORT,80,DIRECT #匹配数据目标端口(直连)  
##- SRC-PORT,7777,DIRECT #匹配数据源端口(直连)  
