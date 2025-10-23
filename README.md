# vendor-pov-config-server

## Hierarchy
```
application.properties
a.properties
a-profile.properties
application.properties
```

## Configure Microservice to be a Client of Config Server
### Maven Dependencies
```
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-config</artifactId>
</dependency>
 
<dependency>
    <groupId>org.springframework.cloud</groupId>
    <artifactId>spring-cloud-starter-bootstrap</artifactId>
    <version>4.0.1</version>
</dependency>
```

### bootstrap.properties File
```
spring.cloud.config.uri=http://localhost:8012
```
and optionally:
```
spring.cloud.config.name=users-ws
```

### application.properties File
spring.config.import=configserver:http://localhost:8012