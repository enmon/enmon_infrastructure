## enmon_infrastructure
This repository contains the infrastructure required for enmon plant monitoring as a Docker Compose stack. It particular:
- the Mosquitto MQTT broker
- live weather informations for the connected power plant locations
- capture of MQTT plant data through Telegraf
- permanent storage of caputred data on InfluxDB
- visualization of captured and live plant data on Grafana

A number of secret environment variables (for credentials and API tokens) are required to successfully start the Docker stack. The variables can be placed in a `.env` in the same directory as `docker-compose.yml` (Docker will automatically source all variable defined in the `.env` file).
`secrets.base.env` can be used as a base for the required `.env` file
