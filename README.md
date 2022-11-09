# START SEQUENCE
# eureka-server -> admin-service-> authentication-service -> employee-service -> consumer-service (dummy)

<h1> Service Functions </h1>

    -> Added jwt filtering in consumer-service
    -> employee-service         =>  Employee Model => Cassandra Database => created basic CRUD services
    -> admin-service            =>  User Model (admin) => H2 Database   => created basic login, signup services
    -> authentication-service   =>  Token Service => creating and getting the decoded token 
    -> consumer-service         =>  Proxies of above 3 services created here 
                                    For accessing : 
                                                    User -> signup, login (and then generate token)
                                                    employee -> CRUD ops (all WITH token required Authorizaiton)
                                                    authentication -> required for generating token at login time
                                                    
                                                    
                                                    
                                                    
                                                    
                                                    
   Spring Boot Cassandra Assessment
Establish a connection to Cassandra from a Spring Boot microservice.
Create keyspaces, user-defined types, entities, and repositories.`
Create a basic CRUD Operation for the following Application
This application should contain two account access:

Admin 
Employee

Admin Dashboard
- Signup
- Sign In => Generate JWT
Employee
JWT Token should be used for the following apis as an authentication
  => Able to view all Employee Details
  => Create a new Employee
  => Edit Employee [Should only be limited to generic details change not password or email of login]
  => Delete Employee
