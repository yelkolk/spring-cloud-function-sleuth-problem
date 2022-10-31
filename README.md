# spring-cloud-function-sleuth-problem

Sample project to demonstrate a cloud function and sleuth problem using cloud version 2021.0.4

## Requirements

Java 17

## Getting Started

Start a rabbitmq docker container to test this demo

```shell
docker run -d -p 5672:5672 -p 15672:15672 rabbitmq:3.11.2-management
```

Run

```shell
./gradlew test
```

### Behaviour with spring cloud 2021.0.3

One exchange is created in RabbitMQ, ``demo.destination``

### Behaviour with spring cloud 2021.0.4

Two exchange are created in RabbitMQ, ``traceFunctionAroundWrapper-in-0``
and ``traceFunctionAroundWrapper-out-0``
