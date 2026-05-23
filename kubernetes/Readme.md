# NOTES:
----------

* devloping dockerfiles in local and pushing to github repo.
* Installing docker in docker work station.
* Image building and pushing to docker hub. or ECR repo or ACR 

# How to run the image after creating an image from docker.?

* for running images k8s through manifest files.
* we are giving instructions inside the manifest files.
* when you run kubectl apply -f manifest.yaml ( workloads will be run on worker node machine) . it means application  running as container.

# Control Plane:
=================

* when you push the manifest files with kubectl , that files goes to any one of the workernode as a container
* image will be pulled by nodes.
* when run the container, that container where should go ( which workernode) that will decide by control plane will decide.

# what is the command to see the nodes?

* kubectl get nodes  (if you want to see which namespace it is and which cluster it is) -n <namespce> --context <cluster>

# POD:
======
* Pod is the smallest deployble unit in k'8s 

# what is the command to see the pods?

* kubectl get pods  (if you want to see which namespace it is and which cluster it is) -n <namespce> --context <cluster>

# what is the CrashLoopBackOff:
================================

* container should run always, it means container should tun infinte times , other wise will get CrashLoopBackOff error.
* in these case how to check the ?

kubectl describe pod <pod-name>   (if you want to see which namespace it is and which cluster it is) -n <namespce> --context <cluster>


# what is the command to loggin to the container?
==================================================

* kubectl exec -it <pod-name> -- bash or -- /bin/bash

* if you have multiple containers inside the pod ? how to login specific container ?
=======================================================================================

* kubectl exec -it <pod-name> -c <container-name> -- bash

# sideCar Container:
=====================
