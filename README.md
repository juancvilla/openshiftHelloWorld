# openshiftHelloWorld
Example of OpenShift Hello World 

Crear un servicio para una aplicación que se ejecuta en cinco pods

oc apply -f https://github.com/juancvilla/openshiftHelloWorld/hw-example.yaml

Este comando crea un deploy asociado con réplicas. El ReplicaSet tiene 5 una de los cuales ejecuta la aplicación Hello World (gcr.io/google-samples/hello-app:2.0)

oc get deployments hello-world

oc describe deployments hello-world

oc get replicasets

oc describe replicasets

oc expose deployment hello-world --name=mi-servicio

oc get services mi-servicio

NAME         TYPE        CLUSTER-IP      EXTERNAL-IP   PORT(S)    AGE
my-service   ClusterIP   172.30.121.34   <none>        8080/TCP   27m
