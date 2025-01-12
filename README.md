**DEPLOYING VOTING APP ON KUBERNETES.**

This project is about deployment of Voting App that is developed in with microservice architecture.

This app make use of
* Postgresql DB
* Redis

For this app to work, it is divided into 5 different pods on Kubernetes cluster. I made use of Minikube on my local machine.

5 pods was created:
- Redis
- Postgresql
- result page
- voting page
- worker page

4 services was created
1. DB service with ClusterIP because it works in the background and does not require access by the users.
2. Redis service also with a Cluster IP
3. Voting Service and Result service are deploying with NodePorts so as to give access users to be able to use the app. 

Using kubernetes, I was able connecting all pods as well as their service. They exposing them for external access for a complete app to run.
