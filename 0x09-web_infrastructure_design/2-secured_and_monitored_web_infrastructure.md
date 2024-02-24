
# Secured and Monitored Web Infrastructure

![image](https://github.com/Gabrielafolabi/alx-system_engineering-devops/assets/35296784/74645b60-6975-426b-a80d-d0bda1c09e79)


## Description

This is a 3-server web infrastructure that is secured, monitored, and serves encrypted traffic.

## Specifics About This Infrastructure

+ The purpose of the firewalls.<br/>Firewalls in the web infrastructure here, act as barriers between a trusted internal network and untrusted external networks, like the internet. They monitor and control incoming and outgoing network traffic based on  security rules that is defined.. 
+ The purpose of the SSL certificate.<br/>The SSL certificate is for encrypting the traffic between the web servers and the external network to prevent man-in-the-middle attacks (MITM) and network sniffers from sniffing the traffic which could expose valuable information. The SSL certs ensure privacy, integrity, and identification.
+ The purpose of the monitoring clients.<br/>The monitoring clients are for monitoring the servers and the external network. They analyse the performance and operations of the servers, measure the overall health, and alert the administrators if the servers are not performing as expected. The monitoring tool observes the servers and provides key metrics about the servers' operations to the administrators. It automatically tests the accessibility of the servers, measures response time, and alerts for errors such as corrupt/missing files, security vulnerabilities/violations, and many other issues. 

## Issues With This Infrastructure

+ Terminating SSL at the load balancer level would leave the traffic between the load balancer and the web servers unencrypted.
+ Having one MySQL server can act as a single point of failure for the web infrastructure because it is not scalable . This poses a great threat
+ Having servers with all the same components would make the components contend for resources on the server like CPU, Memory, I/O, etc., which can lead to poor performance and also make it difficult to locate the source of the problem. A setup such as this is not easily scalable. 
