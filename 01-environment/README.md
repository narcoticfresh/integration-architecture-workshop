# Integration Architecture Workshop Platform

The environment for this course is completely based on docker containers. 

In order to simplify the provisioning, a single docker-compose configuration is used. All the necessary software will be provisioned using Docker.  

You have the following options to start the environment:

 * [**Local Virtual Machine Environment**](./LocalVirtualMachine.md) - a Virtual Machine with Docker and Docker Compose pre-installed will be distributed at by the course infrastructure. You will need 50 GB free disk space.
 * [**Local Docker Environment**](./LocalDocker.md) - you have a local Docker and Docker Compose setup in place which you want to use
 * [**AWS Lightsail Environment**](./Lightsail.md) - AWS Lightsail is a service in Amazon Web Services (AWS) with which we can easily startup an environment and provide all the necessary bootstrapping as a script.


## Post Provisioning

These steps are necessary after the starting the docker environment. 

### Add entry to local `/etc/hosts` File

To simplify working with the Streaming Platform and for the links below to work, add the following entry to your local `/etc/hosts` file. 

```
40.91.195.92	integrationplatform
```

Replace the IP address by the public IP address of the docker host. 

## Services accessible on Integration Platform
The following service are available as part of the platform:

Type | Service | Url
------|------- | -------------
Development | Apache Zeppelin | <http://integrationplatform:38081>
Development | StreamSets Data Collector | <http://integrationplatform:18630>
Governance | Schema Registry UI  | <http://integrationplatform:8002>
Management | Adminer | <http://integrationplatform:38080>
Management | Minio | <http://integrationplatform:9000/hawtio>
Management | Hawtio | <http://integrationplatform:8090/hawtio>
Management | ActiveMQ Admin | <http://integrationplatform:8161>
Management | Servicemix | <http://integrationplatform:8161>
Management | Kafka Manager  | <http://integrationplatform:39000>


