# itc_backend

## Challenge 1
Just run the application and the test via IDE.
```bash  
mvn clean install
```

```bash  
java -jar ./target/itc_2025-1.0-SNAPSHOT.jar
```

4 Jan - Tried to use Dropwizard, but it was not working as expected, so I used Spring Boot instead.

## Challenge 2
### Build the Docker image under the root directory of the project:
```bash  
docker build -t my-spring-boot-app .
```
### Run the Docker container:  
```bash
docker run -p 8080:8080 my-spring-boot-app
```
### Test the REST service:  
Open a web browser or use a tool like curl or Postman to send requests to http://localhost:8080.
Verify that the REST endpoints are responding as expected.
```bash
    // Local Test
    http://localhost:8080/api/coins/calculate?targetAmount=7.3&coinDenominations=0.01,0.5,1,5,10
    // Remote Test
    http://3.0.18.101:8080/api/coins/calculate?targetAmount=7.3&coinDenominations=0.01,0.5,1,5,10
```
## Challenge 3
Access to the AWS instance to start the backend application.
```bash
ssh -i "Austin.pem" ubuntu@ec2-3-0-18-101.ap-southeast-1.compute.amazonaws.com
```

```bash
java -jar ITC/backend/itc_2025-1.0-SNAPSHOT.jar
```

If you want to make the backend application running once the terminal is closed, you can use the following command:
```bash
nohup java -jar ITC/backend/itc_2025-1.0-SNAPSHOT.jar &
```

If you want to access to the frontend application, please use the following URL:
```bash
http://3.0.18.101
```
