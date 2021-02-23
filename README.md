# Blog microservice project.

## What is this project for?

The blog is made with the idea of being able to make posts, comments and moderate them. It is an project to emulate how microservices work and learning how to get started with K8s, Docker and Skaffold. This is by no means production grade. 

## How does it work?

By using the `skaffold dev` command, the entire project will be bundled and all the services inside the project will be launched. The services are as follows:

1. A client service to display the data.
2. A Post service that enables posts.
3. A comments services that enables comments to be made when a post exists.
4. A moderation service that filters out requirements set in `/moderation/index.js`
5. A query service that updates status when and if to use moderaton.
6. An Event bus service that makes each service communicate with one another.

All these services have their respective k8s file inside `infra/k8s`. And the entire `infra/k8s` folder is loaded through the `Skaffold.yaml` file inside the main directory.

## Final notes

This project was made to learn, it is by no means a production grade service, there are better and easier alternatives to make a proper blog service.
