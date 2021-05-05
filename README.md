# **Kubernetes Introduction**

This is a little project to show how we can start working with Kubernetes cluster.

**Simple Project to test kubernetes in minikube**

This sample project has a simple demo solution, you can see it in the following diagram:

_Mongo demo_
![abstract view](https://github.com/jparanda/code-examples/blob/main/kubernetes_intro/images/demo_diagram.png?raw=true)


You can follow these instructions in order to use this project :


* It order to build the above solution you need install minikube and kubectl in your personal computer, following the official instructions https://kubernetes.io/docs/tasks/tools/

* Execute the command *kubectl apply -f {file_name}* for the following yaml files :
  * **mongo-secret.yaml**, this yaml will create the **secret component** used by mongo DB
  * **mongo-db.yaml**, this yaml will create the mongo DB pod and also the internal service to allow comunication from mongo-express.
  * **mongo-configMap.yaml**. this yaml will crete the **configMap component** used by mongo-express.
  * **mongo-express.yaml**, this yaml will create the mongo-express pod and also the external service to allow the communication ouside the kubernetes cluster, in this case from browser to allow us use mongo-express application.
  * We need to assign a public IP to external service use this command
    * *minikube service mongo-express-service*

Finally you will see the mongo-express web app interface :

![abstract view](https://github.com/jparanda/code-examples/blob/main/kubernetes_intro/images/mongo-express-ui.png?raw=true)


Feel free to fork this project to play with it !!
