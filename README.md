# Load testing with Artillery

This repository provides a script to run load tests with [Artillery](https://artillery.io/) to a [SpringBoot](https://spring.io/projects/spring-boot) application with a H2 database that exposes a REST API. 

The script implements the following [scenario](doc/scenario.md).

## Steps to run the load test

### Prerequisite

Install artillery in your system. This can be done in ubuntu executing the command:

```
$ npm install -g artillery
```

Updated information about Artillery installation can be found [here](https://artillery.io/docs/guides/getting-started/installing-artillery.html)

### Run SpringBoot application

```
$ mvn spring-boot:run
```

### Execute load testing

In order to run the [script](artillery/solution.yml) for load testing, execute:

```
$ cd artillery
$ artillery run solution.yml -o output.json
```

**Important:** the above command will overwrite the provided [output.json](artillery/output.json), if you wish to preserve it, please select another filename for output report.

## Author

[David Rojo(@david-rojo)](https://github.com/david-rojo)
