# Nginx-gatling

This repository creates a very basic web server using nginx on docker, and then uses gatling to test requests to it every second for thirty seconds.

## Requirements
This repository requires you to have docker and docker-compose installed.
https://docs.docker.com/compose/install/

## Starting docker
Git clone this repository, open a terminal in the repository directory and run:

```docker-compose up```

You should then be able to go to http://localhost:8080/ and see the webpage.

You should see the HTTP the terminal where you ran `docker-compose up.` every time you visit the webpage on your browser.

## Using gatling

For simplicity I have placed the Gatling binarys in this repository.

Set the environment variable `GATLING_HOME` to gatling-charts folder i.e
```
GATLING_HOME=$PWD/gatling-charts-highcharts-bundle-3.3.1
```

Then run the simulation using:
```
$GATLING_HOME/bin/gatling.sh
```
Then
1. Press 0 to select the simulation
2. Press enter to leave a blank description

If you have the terminal open were you ran `docker-compose up` you should see the requests coming in once every second.

The code for the simulation is the following file:  
`gatling-charts-highcharts-bundle-3.3.1/user-files/simulations/computerdatabase/TommySimulation.scala `

Any results of simulations will be in:
`gatling-charts-highcharts-bundle-3.3.1/results`

