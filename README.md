# Hello World Spring Boot Application

This is a simple Hello World application built using Spring Boot, showcasing an API and microservice deployment using Java Spring Boot, Mockito, Maven, Jenkins, OpenShift, and Docker.

## Getting Started

These instructions will help you set up the project and run it on your local machine for development and testing purposes.

### Prerequisites

You need to have the following software installed on your machine:

- JDK 11 or later
- Maven
- Docker (optional)

### Installing and Running

1. Clone this repository to your local machine:

git clone https://github.com/escarta/HelloWorld.git
cd helloworld

2. Build the project using Maven:

mvn clean install

3. Run the application:

mvn spring-boot:run

4. Access the Hello World API endpoint at http://localhost:8080/hello

## Docker

To build a Docker image for the application, run the following command in the project directory:

docker build -t your-dockerhub-username/your-image-name .

To run the Docker container:

docker run -p 8080:8080 your-dockerhub-username/your-image-name

Access the Hello World API endpoint at http://localhost:8080/hello

## Deployment

This application can be deployed using Jenkins and OpenShift, following the provided configuration files.

## License

This project is open-source and available under the [MIT License](LICENSE).