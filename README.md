# load_balancer_srategies


𝟖 𝐋𝐨𝐚𝐝 𝐁𝐚𝐥𝐚𝐧𝐜𝐢𝐧𝐠 𝐀𝐥𝐠𝐨𝐫𝐢𝐭𝐡𝐦𝐬 𝐘𝐨𝐮 𝐌𝐮𝐬𝐭 𝐊𝐧𝐨𝐰

1. Round Robin
It assigns a request to the first server, then moves to the second, third, and so on, and after reaching the last server, it starts again at the first.

![Spinning Globe](https://github.com/ouminaElHassane/load_balancer_srategies/blob/master/1723367376171.gif)

3. Least Connections
The Least Connections algorithm directs incoming requests to the server with the lowest number of active connections. 

4. Weighted Round Robin
It assigns different weights to servers based on their capacities and distributes requests proportionally to these weights.

5. Weighted Least Connections
The Weighted Least Connections algorithm combines the Least Connections and Weighted Round Robin algorithms. It directs incoming requests to the server with the lowest ratio of active connections to assigned weight.

6. IP Hash
The IP Hash algorithm determines the server to which a request should be sent based on the source and/or destination IP address. This method maintains session persistence, ensuring that requests from a specific user are directed to the same server.

7. Least Response Time
It directs incoming requests to the server with the lowest response time and the fewest active connections.

8. Random
It directs incoming requests to a randomly selected server from the available pool.

9. Least Bandwidth
It directs incoming requests to the server currently utilizing the least amount of bandwidth. This approach helps to ensure that servers are not overwhelmed by network traffic.


##------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
![Spinning Globe](https://github.com/user-attachments/assets/55f2d9f6-e353-4e70-9105-204747aea685)

How Data Travels Through the Layers of the Internet

As data is transmitted over the internet, it passes through several layers of communication protocols. The TCP/IP model provides a more practical framework compared to the theoretical OSI model. We examine how data becomes encapsulated as it travels across networks.

The 𝗧𝗖𝗣/𝗜𝗣 𝗠𝗼𝗱𝗲𝗹 contains four key layers:

- Application - supports end-user processes like HTTP, SMTP
- Transport - handles host-to-host communication (TCP, UDP)
- Network - addresses and routes packets (IP protocol)
- Link - moves the bits over the network's physical wires, cables or wireless channels

This model more closely matches real-world internet communication by condensing the seven OSI layers into these four fundamental ones.

An Example: 𝗦𝗲𝗻𝗱𝗶𝗻𝗴 𝗮𝗻 𝗛𝗧𝗧𝗣 𝗥𝗲𝗾𝘂𝗲𝘀𝘁

When a client sends an HTTP request to a web server, here is the encapsulation process:

- The HTTP header is added to the data at the application layer.
- A TCP header is added at the transport layer, containing sequence numbers and port numbers.
- An IP header is added at the network layer, with source and destination IP addresses.
- A data link layer header includes source and destination MAC addresses.

When the web server receives the bits, the headers get removed in reverse order until the HTTP request is left for the server to process.

## ----------------------------------------------------------------------------------------------------------------------------------------------------
![Spinning Globe](https://github.com/user-attachments/assets/26e25ae7-c8fc-4d03-9580-531d426ea579)


Do you know those 8 common problems in large-scale production systems and their solutions? Time to test your skills! 
 
1 - Read-Heavy System 
Use caching to make the reads faster. 
 
2 - High-Write Traffic 
Use async workers to process the writes 
Use databases powered by LSM-Trees 
 
3 - Single Point of Failure 
Implement redundancy and failover mechanisms for critical components like databases. 
 
4 - High Availability 
Use load balancing to ensure that requests go to healthy server instances. 
Use database replication to improve durability and availability. 
 
5 - High Latency 
Use a content delivery network to reduce latency 
 
6 - Handling Large Files 
Use block storage and object storage to handle large files and complex data. 
 
7 - Monitoring and Alerting 
Use a centralized logging system using something like the ELK stack. 
 
8 - Slower Database Queries 
Use proper indexes to optimize queries. 
Use sharding to scale the database horizontally. 
 
Over to you: What other common problems and solutions have you seen? 
