# ERP Gateway Service

## Maven

### Build

mvn clean install

### Run

cd target

java -jar file-name.jar

java -jar file-name.jar --spring.profiles.active=localhost

java -jar file-name.jar --spring.profiles.active=development

java -jar file-name.jar --spring.profiles.active=production

## Docker

### Build

docker build -t erp-gateway-service:latest -f Dockerfile .

### Run

docker run -it --restart always --name erp-gateway-service-localhost -p 1030:1030 -e SPRING_PROFILES_ACTIVE=localhost erp-gateway-service:latest

docker run -it --restart always --name erp-gateway-service-development -p 1031:1030 -e SPRING_PROFILES_ACTIVE=development erp-gateway-service:latest

docker run -it --restart always --name erp-gateway-service-production -p 1032:1030 -e SPRING_PROFILES_ACTIVE=production erp-gateway-service:latest

#### SPRING_PROFILES_ACTIVE (env)

localhost, development, production
