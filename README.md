# Sample resource server Guide

This is a demonstration application that serves primarily as a tool to test an API gateway or as a sample resource server backed by OAuth2.

## Getting Started

### Prerequisites
1. Clone this repository to your local machine.
2. Optionally, you may also set up a [Spring Cloud Config Server](https://docs.spring.io/spring-cloud-config/docs/current/reference/html/#_spring_cloud_config_server).

There are two methods to get this application up and running on your local machine:

### Running without the Spring Cloud Config Server
Simply select the `local` profile and run the application. The application will be accessible on `port 8990`.

### Running with the Spring Cloud Config Server
1. Initiate the setup of the server and start it.
2. Define the following two-environment variables and start the server:
   1. `CONFIG_SERVER` should be set to the URL of your config server (append a `/` at the end).
   2. `PROFILE` should match the profile that you're planning to use and which is also available in the config server, registered for your application.

## Testing the Sample Resource

After the application has successfully started, access the following URL from your browser: `http://localhost:<port>/resource`. If everything has been configured correctly, you should be greeted with the following message:
```
Treasure!!!!!!
```