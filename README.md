# SpringCloud

This repository demonstrate the spring cloud configutation.

It contains :- 
Configuration Server
Discovery Server
GateWay Server(Zull)
Authentication Server

Microservices:- 
Book Service
Rating Service

The Configuration server fetches information from a git repository.
In this git repository configuration files for all the other servers are present.

Discovery Server is a Eureka server which takes care of the service discovery.

GateWay is the Zull proxy server implementation.

Authentication Server is responsible to secure underlying microservices.
It uses JWT token based authentication.
To call a microservice you first need to get a token from the authentication server and then this token will be verified at gateway and then if its valid then access is granted otherwise accesss will be blocked.

Steps:- 

1. Start configuration server.
2. Start discovery server.
3. Restart configuration Server so that the it gets registerd properly with eureka.
4. start other servers in any sequence.
