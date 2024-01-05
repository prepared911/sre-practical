# SRE Coding Exercise

Today your task will be to 
1. create a simple application
2. dockerize it
3. deploy it to an ARM machine in a k8s cluster
4. test your deployment

## Prereqs
For the purpose of this interview, all you will need installed is a 
1. Text Editor
2. Kubectl 
3. Docker

## Application Requirements
- HTTP server should respond to requests at `/[path]`
- Body of response should contain all of the namespaces in the cluster labeled `[path]: true`
  - If namespaces exist, return 200 status.
  - If no namespaces, return 404 status and print "No namespaces with label [path]".
  - `/ephemeral` should return 200 and print: `foo, env1, supersecret`
- Docker image should run using `alpine:3.17.3` or `scratch` base image, unless using an interpretted language. 

## Connecting to the Kubernetes Cluster
Your interviewer will provide you with a kubeconfig that you can use in order to connect to your interview cluster. 

## Pushing images to the docker repository
The image registry is located at `sre-practical-harbor.prepared911.dev/sre`

Credentials to the registry will be provided by your interviewer.

When creating your image, please push it to the repository at `sre-practical-harbor.prepared911.dev/sre/[YOURNAME]`

