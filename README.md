# groovy-cli-maven-dolt-trigger

## Description
Creates a small database table
called `dog` with an `insert after` trigger.
The trigger function `ins_dog_trigger` calls `sp_rolling_audit`
that remmoves old entries. 


All output normally
seen in a terminal will be in `groovy-srv/log` which will dump to the screen. The project may seem to hang but the logs from the container must be written to the project this can take up to 3 min.

## Tech stack
- groovy
- maven
  - log4j
  - dolt driver

## Docker stack
- dolthub/dolt-sql-serverdb:latest
- maven:3-openjdk-17

## To run
`sudo ./install.sh -u`
Creates groovy-srv/log

## To stop
`sudo ./install.sh -d`
Removes groovy-srv/log

## For help
`sudo ./install.sh -h`
