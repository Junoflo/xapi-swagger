# xapi-swagger
xAPI Spec in Swagger

# What’s xAPI Swagger?
This repository converts the [xAPI specification v1.0.2](https://github.com/adlnet/xAPI-Spec) into the [Swagger](http://swagger.io/) format. Swagger is a simple yet powerful way to represent a RESTful API. It also provides a variety of features that make it easier to work with APIs. The xAPI specification is inherently RESTful, therefore it lends itself well to be describe in Swagger.

The xAPI specification is very large and can be confusing to work with at first. The goal of this repository is to hopefully make it easier to understand and get started using xAPI.

This repository is a work in progress and will continue to evolve based on updates to the spec.

# Usage
It is fairly easy to get started with xAPI Swagger. Using the [Swagger UI](http://editor.swagger.io/#/), you can easily visualize the xAPI speciation

1. Goto [Swagger UI](http://editor.swagger.io/#/)
2. Import the xapi-swagger.yaml file
3. Explore!

# Limitations with xAPI
A limitation of Swagger is expectation of deterministic vs non-deterministic behavior.  For example, Statement object types (Activity, Agent, Group, Statement Reference, Sub-Statement) are difficult to fully represent since Swagger does not handle conditions by evaluating the object's objectType and correctly setting the Statement's object.

Another limitation example is evaluation of Agent / Group for Actor, Authority, etc.  When using the code generation, Swagger would only allow defaulting the body to an schema so a Content schema was created to hold Document APIs content for POST / PUT.
