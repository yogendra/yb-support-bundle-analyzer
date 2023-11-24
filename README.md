
# YugabyteDB - Support Bundle Analyzer

This is a ELK based tool for analysing support bundles.

## Pre-requisites

1. Docker
2. Support Bundle
3. Browser

## How to use this tool

1. Get a support bundle package
2. Extract in under `./support-bundles` directory. This should create a directory with name starting with  `yb-support-bundle`
3. Run tool with simple `docker compose up`
4. Navigate to [Kibana / Observability / Logs / Stream](http://localhost:5601/app/logs/stream)
5. See the events get loaded into the UI

*Please note the log file will be deleted after they are loaded into this tool*


## FAQ

1. What logs does is capture and visualizes?

    This tool, captures universe and YBA logs that are part of the bundle. For a universe, it captures logs for controller, tserver, master and postgres

2. Is there a way to only see universe logs or tserver logs, etc.

    All log events are tagged with component type, so you can filter the logs based on this component type to narrow your searches.



