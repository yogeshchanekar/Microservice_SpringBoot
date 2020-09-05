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

What is Service-oriented architecture (SOA) ?
Service-oriented architecture (SOA) is a style of software design in which application components provide services to other components via a communications protocol that is typically over a network.

![service-oriented-architecture-vs-microservices](https://user-images.githubusercontent.com/55848417/92139096-e4a1c480-ee2c-11ea-8836-d40f68b26ba2.png)

Service-oriented architecture was largely created as a response to traditional, monolithic approaches to building applications. SOA breaks up the components required for applications into separate service modules that communicate with one another to meet specific business objectives. Each module is considerably smaller than a monolithic application, and can be deployed to serve different purposes in an enterprise. Additionally, SOA is delivered via the cloud and can include services for infrastructure, platforms, and applications.

SOA’s two main roles are as a service provider and a service consumer. Its service provider layer includes the different services involved in SOA, while the consumer layer operates as the user interface. 

![Microservice Vs SOA](https://user-images.githubusercontent.com/55848417/92152475-59322e80-ee40-11ea-8705-ee09539506aa.png)

What is a microservice?

Microservice architecture is generally considered an evolution of SOA as its services are more fine-grained, and function independently of each other. Therefore, if one of the services fail within an application, the app will continue to function since each service has a distinct purpose. The services in microservices communicate via application programming interfaces (APIs) and are organized around a particular business domain. Together, these services combine to make up complex applications.

Since each service is independent, a microservice architecture can scale better than other approaches used for application building and deployment. This characteristic also gives microservice applications more fault tolerance than other application development methods. Microservices are frequently built and deployed in the cloud; in many instances they operate in containers.


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






