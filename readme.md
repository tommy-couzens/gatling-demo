Set the environment variable `GATLING_HOME` to gatling-charts folder
I.e
```
GATLING_HOME=$PWD/gatling-charts-highcharts-bundle-3.3.1
```

Then run the simulation using:
```
$GATLING_HOME/bin/gatling.sh
```

Press 0 to run the similation, and enter a description for it (or just press return for no description.)
If you have the terminal open were you ran `docker-compose up` you should see the requests coming in once every second.

