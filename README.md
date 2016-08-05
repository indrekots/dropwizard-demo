# Simple hello world application with Dropwizard

## Building the app

This dropwizard app uses Maven as a build tool. Additionally Java 1.8 is required. 
```bash
#run the following in your terminal to build the app
mvn package

```

## Running the app
The app is built as a fat JAR, meaning that it contains all the `.class` files which are needed to run the application.
```bash
#run the following in your terminal to run the app
java -jar target/dropwizard-demo-1.0-SNAPSHOT.jar server hello-world.yml
```

This will start a service which listens on port 8080 for incoming requests.

## API endpoints

* `GET     /hello-world` - responds with "Hello world"
* `GET     /hello-world?name="Enter your name"` - responds with "Hello, your name".

## Admin port

In addition to port 8080, the service listens on port 8081 which is the admin port. This provides access to different health metrics. For more information visit the [user manual for Dropwizard](http://www.dropwizard.io/1.0.0/docs/manual/index.html).
