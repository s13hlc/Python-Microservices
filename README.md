# Python-Microservices

Python Flask to K8s Microservices

- https://www.youtube.com/watch?v=SdTzwYmsgoU

Installing Python 3.X
Creating Python Virtual Environments
Installing Python VS Code Extension
Sample Flask Application
Jinja templating for Dynamic Web Pages
Using Pip to Freeze Python Dependencies
Building the docker image using Dockerfile
Writing Docker Compose file
Writing Kubernetes Manifest files for the application
Creating Helm Chart

python -a venv pyK8s-env
.\PyK8s-env\Scripts\activate


(PyK8s-env) PS C:\Users\Chris NonAdmin\Desktop\Python\Python-Microservices> kubectl get all -n pythontest
Warning: apps.openshift.io/v1 DeploymentConfig is deprecated in v4.14+, unavailable in v4.10000+
NAME                            READY   STATUS    RESTARTS   AGE
pod/mywebapp-67d9868b9f-kvd2v   1/1     Running   0          2m15s
pod/mywebapp-67d9868b9f-plhbf   1/1     Running   0          2m15s

NAME               TYPE       CLUSTER-IP    EXTERNAL-IP   PORT(S)        AGE
service/mywebapp   NodePort   10.217.4.63   <none>        80:31219/TCP   2m15s

NAME                       READY   UP-TO-DATE   AVAILABLE   AGE
deployment.apps/mywebapp   2/2     2            2           2m15s

NAME                                  DESIRED   CURRENT   READY   AGE
replicaset.apps/mywebapp-67d9868b9f   2         2         2       2m15s

NAME                                   HOST/PORT                                 PATH   SERVICES      PORT   TERMINATION   WILDCARD
route.route.openshift.io/web-service   web-service-pythontest.apps-crc.testing          web-service   5000                 None

web-service-pythontest.apps-crc.testing:31219/details or health
