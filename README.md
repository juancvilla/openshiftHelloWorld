# OpenShiftHelloWorld

Example of OpenShift Hello World 

Crear un servicio para una aplicación que se ejecuta en cinco pods

```
oc apply  -f https://raw.githubusercontent.com/juancvilla/openshiftHelloWorld/refs/heads/main/hw-example.yaml
```

Este comando crea un deploy asociado con réplicas. El ReplicaSet tiene 5 una de los cuales ejecuta la aplicación Hello World (gcr.io/google-samples/hello-app:2.0)

```
oc get deployments hello-world
oc describe deployments hello-world
oc get replicasets
oc describe replicasets
oc expose deployment hello-world --name=mi-servicio
oc get services mi-servicio
oc describe services mi-servicio
oc get pods --output=wide
oc expose svc mi-servicio
```
**Limpiando openshiftHelloWorld**

Para eliminar el Servicio, introduzca estos comandos:

```
oc delete route mi-servicio
oc delete service mi-servicio
oc delete -f https://raw.githubusercontent.com/juancvilla/openshiftHelloWorld/refs/heads/main/hw-example.yaml
```

# Openshift nginx example

```
oc apply  -f https://raw.githubusercontent.com/juancvilla/openshiftHelloWorld/refs/heads/main/nginx.yaml
```

**Limpiando nginx example**
```
oc delete -f https://raw.githubusercontent.com/juancvilla/openshiftHelloWorld/refs/heads/main/nginx.yaml
```
