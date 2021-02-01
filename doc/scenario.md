# Load testing with Artillery scenario

It is requested to define the load tests for an application REST API that manages a library. Specifically, it is requested to write a TestScript that contains the needed configuration to run load tests with [Artillery](https://artillery.io/) and also the results of its execution.

## 1. Requisites

* A unique phase of 40 seconds will be defined and the rate of users per second will be 5.
* Only 8 simultaneous connections to the API will be allowed.
* 95% of the requests cannot overcome 100 ms of latency.
* The error rate must be 0%.

*Note 1:* is not needed that the execution cover the requisites, only is requested to define them properly.

## 2. Scenarios

The following scenarios must be defined:

* Scenario 1: Retrieve the first book. A user without logging retrieves all the books and it requests the first book in order to retrieve more information.
* Scenario 2: Create a book. A logged user creates a book and when it is created, the user retrieve the book to check it.
* Scenario 3: Delete a book. The admin user creates a book, after check it, it deletes it and check that the book doesn't exist.

*Note 2:* In case that authentication is needed, a logIn request is required first.

*Note 3:* In order to simulate a real behavior, the following probability will be assigned to each scenario:

* Scenario 1: 70%
* Scenario 2: 20%
* Scenario 3: 10%

*Note 4:* For the requests of each scenario, is required to verify the http status of responses.
