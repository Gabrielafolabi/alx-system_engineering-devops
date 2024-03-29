# Simple Web Stack

![image](https://github.com/Gabrielafolabi/alx-system_engineering-devops/assets/35296784/66292523-39bc-47c3-9dcf-62aea5d73aba)


## Description

This is a simple web infrastructure that hosts a website that is reachable via `www.foobar.com`. Each component (database, application server) has to share the resources provided by the server.
There are no firewalls or SSL certificates for server network protection.
##  Specifics About This Infrastructure

+ What a server is.<br/>A server is a computer hardware or software that provides services to other computers, which are usually referred to as *clients*.

+ The role of the domain name.<br/DNS is responsible for finding the correct IP address for that domain name `www.foobar.com` and directing the browser to the correct website ip which `8.8.8.8` used here as an example.

+ The type of DNS record `www` is in `www.foobar.com`.<br/>`www.foobar.com` uses an **A record**. This can be checked by running `dig www.foobar.com`.<br/>**Note:** the results might be different but for the infrastructure in this design, an **A** record is used.<br/>
<i>Address Mapping record (A Record)—also known as a DNS host record, stores a hostname and its corresponding IPv4 address.</i>

+ The role of the web server.<br/>A web server plays a central role in facilitating the delivery of web content in HTML to users over the internet. It does this through the HTTP or HTTPS protocol. 
+ The role of the application server.<br/> Manages the application's business logic and facilitating interaction between the application and various clients.
+ The role of the database.<br/>Maintains a collection of organized information that can easily be accessed, managed and updated. It stores, manages, and retrieves structured data efficiently.

+ What the server uses to communicate with the client (computer of the user requesting the website).<br/>Communication between the client and the server occurs over the internet network through the TCP/IP protocol suite.

## Issues With This Infrastructure

+ There are multiple SPOF (Single Point Of Failure) in this infrastructure.<br/>For example, if the MySQL database server is down, the entire site would be down.

+ Downtime when maintenance needed.<br/>When we need to run some maintenance checks on any component, they have to be put down or the server has to be turned off. Since there's only one server, the website would be experiencing a downtime.

+ Cannot scale if there's too much incoming traffic.<br/>It would be hard to scale this infrastructure becauses one server contains the required components. The server can quickly run out of resources or slow down when it starts receiving a lot of requests.
