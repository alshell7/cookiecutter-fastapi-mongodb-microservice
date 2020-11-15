This template is meant to be used for an individual microservice, so it could be used multiple times in the same project for different microservices each time.

---

### To use this template clone it with cookiecutter:

1. Install the `cookiecutter` library if it isn't already installed:
```pip3 install cookiecutter```

2. Use this cookiecutter template: ```cookiecutter gh:andrewguest/cookiecutter-fastapi-microservice```

3. Answer the questions when prompted (example below):
    * ```project_name []:```
        * Cart Microservice
    * ```project_slug [cart-microservice]:```
        * This will be automatically generated by lowercasing your project name and replacing any space with a hyphen. You can just press enter here to use the default project_slug.
    * ```mongodb_port []: 27123```
      * What port would you like the MongoDB container to listen on?

---

### What this template will do for you:

1. Create the folder structure for this microservice:
```
|-- app
  \-- main.py (entry point for application)
|-- database (contains all database related code)
|-- routes (contains all routes to be defined)
|-- tests (contains all of the tests)
```

2. Configure a Dockerfile needed to create an image based on this microservice.

3. Configure the docker-compose.yml file to start the API container and a MongoDB container.

4. Automatically setup the connection between the API and the MongoDB container, inside of ```app/main.py```