# Deployment Discovery Under Kubernetes

The purpose of this lab is to demonstrate how to have a service bind between alternate deployments

Go the `manifests` directory of the project. The `manifests` directory contains all the `yaml` files
we'll need to set up Red and Green deployments as well as the Kubernetes service that will bind to each accordingly.

**Step 1:** To go the `manifests` directory execute the following command:

`cd manifests`

## Set up the Red and Green Deployments

**Step 2:** Execute the following command to execute the Red deployment in your Kubernetes cluster

`kubectl apply -f red-deployment.yaml`

**Step 3:** Execute the following command to execute the Green deployment in your Kubernetes cluster

`kubectl apply -f green-deployment.yaml`

## Set up the Kubernetes service

**Step 4:** Execute the following command to execute the service in your Kubernetes cluster

`kubectl apply -f service.yaml`

## Confirm installation of Deployments and Service

**Step 5:** Execute the following command to confirm that the service is running under Kubernetes

`kubectl get services | grep echocolor`

**Step 5:** Execute the following command to confirm that the deployments are running under Kubernetes

`kubectl get pods | grep echocolor`

