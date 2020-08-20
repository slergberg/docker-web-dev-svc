# Useful containers for local web development

This project consists of a Docker Compose project with several useful
pre-configured containers that are useful for development environments.

The following services/containers are available:

- [DynamoDB](#DynamoDB)
- [Jaeger Tracing](#JaegerTracing)
- [MailCatcher](#MailCatcher)
- [Memcached](#Memcached)
- [MongoDB](#MongoDB)
- [MySQL](#MySQL)
- [NGINX Proxy](#NGINXProxy)
- [Portainer](#Portainer)
- [Postgres](#Postgres)
- [Redis](#Redis)

It's pretty easy to get up and running by following these steps:

1. Clone this repository to your local Docker environment.
2. `cd` into the cloned repository and run `docker-compose up -d` for the services that you want, e.g.:

```
user@ubuntu:~$ docker-compose up -d mysql portainer
```

3. Check out each service's section on this README file in order to access the available endpoints.

## DynamoDB

Amazon DynamoDB is a key-value and document database that delivers single-digit
millisecond performance at any scale. It's a fully managed, multiregion,
multimaster, durable database with built-in security, backup and restore, and
in-memory caching for internet-scale applications. DynamoDB can handle more than
10 trillion requests per day and can support peaks of more than 20 million
requests per second.

### Endpoints:

- **Management UI:** http://dynamodb-admin.web-dev-svc.localhost/
- **Service:** dynamodb.web-dev-svc.localhost
- **Port:** 80

## Jaeger Tracing

Jaeger, inspired by Dapper and OpenZipkin, is a distributed tracing system
released as open source by Uber Technologies. It is used for monitoring and
troubleshooting microservices-based distributed systems, including:

- Distributed context propagation
- Distributed transaction monitoring
- Root cause analysis
- Service dependency analysis
- Performance / latency optimization

### Endpoints:

- **Management UI:** http://jaegertracing.web-dev-svc.localhost/
- **Service:** jaegertracing.web-dev-svc.localhost
- **Ports:**
  - 5775/udp
  - 5778
  - 6831/udp
  - 6832/udp
  - 9411
  - 14268
  - 16686

## MailCatcher

MailCatcher runs a super simple SMTP server which catches any message sent to it
to display in a web interface. Run mailcatcher, set your favourite app to
deliver to smtp://mailcatcher.web-dev-svc.localhost:25 instead of your default
SMTP server, then check out http://mailcatcher.web-dev-svc.localhost to see the
mail that's arrived so far.

### Endpoints:

- **Management UI:** http://mailcatcher.web-dev-svc.localhost/
- **Service:** mailcatcher.web-dev-svc.localhost
- **Port:** 25

## Memcached

Memcached is an in-memory key-value store for small chunks of arbitrary data
(strings, objects) from results of database calls, API calls, or page rendering.

### Endpoints:

- **Management UI:** http://phpmemadmin.web-dev-svc.localhost/
- **Service:** memcached.web-dev-svc.localhost
- **Port:** 11211

## MinIO

MinIO is a high performance, distributed object storage system. It is
software-defined, runs on industry standard hardware and is 100% open source
under the Apache V2 license.

### Endpoints:

- **Management UI:** http://minio.web-dev-svc.localhost/
- **Service:** minio.web-dev-svc.localhost
- **Port:** 80
- **Credentials:**
  - Access Key: 123456789
  - Secret Key: 123456789

## MongoDB

MongoDB is a document database with the scalability and flexibility that you
want with the querying and indexing that you need.

### Endpoints:

- **Management UI:** http://mongo-express.web-dev-svc.localhost/
- **Service:** mongodb.web-dev-svc.localhost
- **Ports:**
  - 27017
  - 27018
  - 27019
  - 28017
- **Credentials:**
  - Root Username: admin
  - Root Password: admin

## MySQL

MySQL is the world's most popular open source database. Whether you are a fast
growing web property, technology ISV or large enterprise, MySQL can
cost-effectively help you deliver high performance, scalable database
applications.

### Endpoints:

- **Management UI:** http://phpmyadmin.web-dev-svc.localhost/
- **Service:** mysql.web-dev-svc.localhost
- **Port:** 3306
- **Credentials:**
  - Root Username: root
  - Root Password: root

## NGINX Proxy

NGINX Proxy sets up a container running NGINX and `docker-gen`. `docker-gen`
generates reverse proxy configs for NGINX and reloads NGINX when containers are
started and stopped.

### Endpoints:

- **Management UI:** N/A
- **Service:** N/A
- **Port:** N/A
- **Credentials:** N/A

## Portainer

Portainer is a simple management solution for Docker.

It consists of a web UI that allows you to easily manage your Docker containers,
images, networks and volumes.

### Endpoints:

- **Management UI:** http://portainer.web-dev-svc.localhost/
- **Service:** portainer.web-dev-svc.localhost
- **Port:** N/A
- **Credentials:** Configurable on first use

## Postgres

PostgreSQL is a powerful, open source object-relational database system with
over 30 years of active development that has earned it a strong reputation for
reliability, feature robustness, and performance.

### Endpoints:

- **Management UI:** http://pgadmin.web-dev-svc.localhost/
- **Service:** postgres.web-dev-svc.localhost
- **Port:** 5432
- **Credentials:**
  - Root Username: postgres
  - Root Password: postgres

## Redis

Redis is an open source (BSD licensed), in-memory data structure store, used as
a database, cache and message broker. It supports data structures such as
strings, hashes, lists, sets, sorted sets with range queries, bitmaps,
hyperloglogs, geospatial indexes with radius queries and streams.

### Endpoints:

- **Management UI:** http://redis-commander.web-dev-svc.localhost/
- **Service:** redis.web-dev-svc.localhost
- **Port:** 5432
- **Credentials:**
  - Root Username: root
  - Root Password: root
