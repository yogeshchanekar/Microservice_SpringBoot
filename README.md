# Microservice_SpringBoot
MicroserviceExample1

                                                    What are microservices?
                                                             
Microservices - also known as the microservice architecture - is an architectural style that structures an application as a collection of services that are

Highly maintainable and testable
Loosely coupled
Independently deployable
Organized around business capabilities
Owned by a small team
The microservice architecture enables the rapid, frequent and reliable delivery of large, complex applications. It also enables an organization to evolve its technology stack.

                                                    Features of MicroService

![Microservices-Features-What-Is-Microservices](https://user-images.githubusercontent.com/55848417/92152003-a3ff7680-ee3f-11ea-9114-aa6cfbd919db.png)


OR we can say that 
Microservice architecture, or simply microservices, is a distinctive method of developing software systems that tries to focus on building single-function modules with well-defined interfaces and operations. The trend has grown popular in recent years as Enterprises look to become more Agile and move towards a DevOps and continuous testing. 

                                                    Architecture of Microservice

![Microservice_Architecture](https://user-images.githubusercontent.com/55848417/92303270-ed131000-ef90-11ea-81c3-8d8a2760c69e.png)

What is Monolithic Architecture?
Traditionally, applications were built on a monolithic architecture, a model in which all modules in an application are interconnected in a single, self-contained unit. All code exists inside a single codebase, which means that the entire application is deployed at the same time, and scaling is achieved by adding additional nodes.

                                                    Monolithic Vs Microservice Architecture

![microservices architecture](https://user-images.githubusercontent.com/55848417/92138506-15352e80-ee2c-11ea-9f0a-8797c7aa6ca1.png)

The problem with monoliths isn’t so much that there’s an inherent problem with the architecture. In fact, simple applications with limited feature sets may benefit from this approach. The challenge comes when companies grow their applications–adding features and bug fixes on top of everything that came before.


                                                   What are Microservices?
Microservices are designed to combat the problems associated with monoliths by going in the complete opposite direction. Microservices are an architectural style where an application is broken into a series of modules, each associated with a specific business objective.

                                            Service-oriented architecture(SOA) Vs Microservice architecture

What is Service-oriented architecture (SOA) ?
Service-oriented architecture (SOA) is a style of software design in which application components provide services to other components via a communications protocol that is typically over a network.

![service-oriented-architecture-vs-microservices](https://user-images.githubusercontent.com/55848417/92139096-e4a1c480-ee2c-11ea-8836-d40f68b26ba2.png)

Service-oriented architecture was largely created as a response to traditional, monolithic approaches to building applications. SOA breaks up the components required for applications into separate service modules that communicate with one another to meet specific business objectives. Each module is considerably smaller than a monolithic application, and can be deployed to serve different purposes in an enterprise. Additionally, SOA is delivered via the cloud and can include services for infrastructure, platforms, and applications.

SOA’s two main roles are as a service provider and a service consumer. Its service provider layer includes the different services involved in SOA, while the consumer layer operates as the user interface. 

![Microservice Vs SOA](https://user-images.githubusercontent.com/55848417/92152475-59322e80-ee40-11ea-8705-ee09539506aa.png)

What is a microservice?

Microservice architecture is generally considered an evolution of SOA as its services are more fine-grained, and function independently of each other. Therefore, if one of the services fail within an application, the app will continue to function since each service has a distinct purpose. The services in microservices communicate via application programming interfaces (APIs) and are organized around a particular business domain. Together, these services combine to make up complex applications.

Since each service is independent, a microservice architecture can scale better than other approaches used for application building and deployment. This characteristic also gives microservice applications more fault tolerance than other application development methods. Microservices are frequently built and deployed in the cloud; in many instances they operate in containers.


                                                                   Components of Microservices
                                                                   
There are the following components of microservices:

1. Spring Cloud Config Server
2. Netflix Eureka Naming Server
3. Hystrix Server
4. Netflix ZuulAPI Gateway Server
5. Netflix Ribbon
6. Zipkin Distributed Tracing Server
7. Spring Cloud Config Server

1. Spring Cloud Config Server
provides the HTTP resource-based API for external configuration in the distributed system. We can enable the Spring Cloud Config Server by using the annotation @EnableConfigServer.

2. Netflix Eureka Naming Server
Netflix Eureka Server is a discovery server. It provides the REST interface to the outside for communicating with it. A microservice after coming up, register itself as a discovery client. The Eureka server also has another software module called Eureka Client. Eureka client interacts with the Eureka server for service discovery. The Eureka client also balances the client requests.

3. Hystrix Server
Hystrix server acts as a fault-tolerance robust system. It is used to avoid complete failure of an application. It does this by using the Circuit Breaker mechanism. If the application is running without any issue, the circuit remains closed. If there is an error encountered in the application, the Hystrix Server opens the circuit. The Hystrix server stops the further request to calling service. It provides a highly robust system.

4. Netflix Zuul API Gateway Server
Netflix Zuul Server is a gateway server from where all the client request has passed through. It acts as a unified interface to a client. It also has an inbuilt load balancer to load the balance of all incoming request from the client.

5. Netflix Ribbon
Netflix Ribbon is the client-side Inter-Process Communication (IPC) library. It provides the client-side balancing algorithm. It uses a Round Robin Load Balancing:

Load balancing
Fault tolerance
Multiple protocols(HTTP, TCP, UDP)
Caching and Batching

6. Zipkin Distributed Server
Zipkin is an open-source project m project. That provides a mechanism for sending, receiving, and visualization traces.

One thing you need to be focused on that is port number.

       Application                                  Port
       
Spring Cloud Config Server	                        8888
Netflix Eureka Naming Server	                      8761
Netflix Zuul API gateway Server	                    8765
Zipkin distributed Tracing Server	                  9411



                                                         What Is the Eureka Server/Discovery Server ?

The Eureka server is nothing but a service discovery pattern implementation, where every microservice is registered and a client microservice looks up the Eureka server to get a dependent microservice to get the job done.

The Eureka Server is a Netflix OSS product, and Spring Cloud offers a declarative way to register and invoke services by Java annotation.

![Microservice Example](https://user-images.githubusercontent.com/55848417/92153305-ab278400-ee41-11ea-9976-8e14f7f66df9.PNG)


Note:- Need to run each microservice as spring boot app using cmd or sts ide.

Also for JSON view download Jsonview Extension in GoogleChrome.

Every microservice is a Spring Boot application and can be started locally using IDE or ../mvnw spring-boot:run command. Please note that supporting services (Discovery Server) must be started before any other application (Movie Catalog, Movie Info, Ratings Data). If everything goes well, you can access the following services at given location:

Discovery Server - http://localhost:8761

Movie Catalog - http://localhost:8081/catalog/{userId}

Movie Info - http://localhost:8082/movies/{movieId}

Ratings Data - http://localhost:8083/ratings/user/{userId}

Hystrix Dashboard - Go to http://localhost:8081/hystrix. Then put 'https://localhost:8081/actuator/hystrix.stream' to the textbox on the middle.

Check Attached screenshot for reference

Movie Info - http://localhost:8082/movies/{movieId}

![image](https://user-images.githubusercontent.com/55848417/92181558-26e7f780-ee67-11ea-828c-b6173cd0e9b1.png)

Movie Catalog - http://localhost:8081/catalog/{userId}

![MicroserviceExampleScreenShot2](https://user-images.githubusercontent.com/55848417/92181770-af669800-ee67-11ea-9f2b-7b899591c239.PNG)


Note : For api-key create account on https://www.themoviedb.org/ and get api-key from the API Section tab.






