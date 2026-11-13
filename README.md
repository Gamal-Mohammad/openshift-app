# vProfile on OpenShift – Manifests

![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![OpenShift](https://img.shields.io/badge/OpenShift-EE0000?logo=redhatopenshift&logoColor=white) ![Tomcat](https://img.shields.io/badge/Tomcat-F8DC75?logo=apachetomcat&logoColor=black) ![MySQL](https://img.shields.io/badge/MySQL-4479A1?logo=mysql&logoColor=white) ![Memcached](https://img.shields.io/badge/Memcached-2C5BB4) ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white)

> OpenShift/Kubernetes manifests to run the multi-tier vProfile stack using custom images.

## Overview

Kubernetes manifests that run the **vProfile** multi-tier stack: the Tomcat application, a **MySQL** database, **Memcached** and **RabbitMQ**, each with its own Deployment and internal ClusterIP Service, plus an externally exposed app Service and a Secret for the database and broker passwords.

## Tech Stack

- **Kubernetes**
- **OpenShift**
- **Tomcat**
- **MySQL**
- **Memcached**
- **RabbitMQ**

## Repository Structure

```text
app/app-secret.yml
app/app-service.yml
app/db-cip.yml
app/deployment-app.yml
app/deployment-db.yml
app/deployment-mc.yml
app/deployment-rmq.yml
app/mc-cip.yml
app/rmq-cip.yml
```

## Getting Started

```bash
kubectl apply -f app/
kubectl get pods,svc
```

On OpenShift use `oc apply -f app/` and `oc expose svc/vproapp-service` to create a route.

## Author

**Gamal Mohammad**

[![GitHub](https://img.shields.io/badge/GitHub-Gamal--Mohammad-181717?logo=github)](https://github.com/Gamal-Mohammad)
