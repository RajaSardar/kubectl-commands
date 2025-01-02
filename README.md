# Useful Kubectl Commands

## Basic Commands
- **Get Context**
  - `kubectl config get-contexts` - List all available contexts.
- **Get Resources**
  - `kubectl get pods` - List all pods in the current namespace.
  - `kubectl get services` - List all services in the current namespace.
  - `kubectl get nodes` - List all nodes in the cluster.

- **Describe Resources**
  - `kubectl describe pod <pod_name>` - Show detailed information about a specific pod.
  - `kubectl describe service <service_name>` - Show detailed information about a specific service.

## Creating and Managing Resources
- **Create Resources**
  - `kubectl create -f <filename>.yaml` - Create a resource defined in a YAML file.
  - `kubectl apply -f <filename>.yaml` - Apply changes to a resource defined in a YAML file.

- **Delete Resources**
  - `kubectl delete pod <pod_name>` - Delete a specific pod.
  - `kubectl delete service <service_name>` - Delete a specific service.

## Logs and Monitoring
- **View Logs**
  - `kubectl logs <pod_name>` - Retrieve logs from a specific pod.
  - `kubectl logs -c <container_name> <pod_name>` - Retrieve logs from a specific container within a pod.

## Scaling and Updating
- **Scale Resources**
  - `kubectl scale deployment <deployment_name> --replicas=<number>` - Scale a deployment to a specified number of replicas.

- **Update Resources**
  - `kubectl set image deployment/<deployment_name> <container_name>=<image_name>` - Update the image of a container in a deployment.

## Executing Commands
- **Execute Commands in Pods**
  - `kubectl exec -it <pod_name> -- /bin/bash` - Open a bash shell in a running pod.

## Resource Management
- **Get Resource Usage**
  - `kubectl top pods` - Display resource usage (CPU/Memory) of pods.
  - `kubectl top nodes` - Display resource usage of nodes.

## Context and Configuration
- **Change Context**
  - `kubectl config use-context <context_name>` - Switch to a different Kubernetes context.

- **View Current Context**
  - `kubectl config current-context` - Display the current context.

## Miscellaneous
- **Get All Resources**
  - `kubectl get all` - List all resources in the current namespace.

- **Get Resource in All Namespaces**
  - `kubectl get pods --all-namespaces` - List all pods across all namespaces.

## Help
- **Get Help**
  - `kubectl help` - Display help information for kubectl commands.
