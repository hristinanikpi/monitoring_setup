# Monitoring Setup 

## Name: Hristina Nikolic

## Date: November 2024

## Description

This project was done as part of the interview process for Devolution. 

It is based on [this article](https://levelup.gitconnected.com/metrics-reliably-configuring-prometheus-and-grafana-with-docker-2077541c8e6d). 

The project shows how you can integrate metrics into your application so that you can use them with Prometheus, and visualise them with Grafana. 

## Usage 

Before starting, make sure you have Docker installed on your machine. 

You can read more about the installation process on [this link](https://docs.docker.com/engine/install/)

WARNING: The commands that follow correspond to Linux operating system. 

To try this code yourself, you should close the repositorium first:

```bash 
git close https://github.com/hristinanikpi/monitoring_setup.git
```

After that, build the docker image using the `docker-copose.yml` file:

```bash 
docker-compose up 
```

Then access the following links:

1. Prometheus: http://localhost:9090/graph
1. Grafana: http://localhost:3000/ - The login by default is admin:admin. Once you have logged in, just skip setting up another user as that is beyond the scope of this project.
1. The metrics from the app: http://localhost:9001/metrics - This will be what we tell Prometheus to scrape, but it gives you an idea of the format and type of metrics available to us for this project.

Now, you can use Grafana UI to access the dashboards and see how the metrics are visualised.

To stop everything, run the following command:

```bash 
docker-compose down -v
```
## Conclusion 

This simple project shows how you can set up Grafana and Prometheus to monitor your computer metrics. Grafana dashboards could be further improved and personalized. This is a diverse solution that can be applied in many settings and used vildly.  