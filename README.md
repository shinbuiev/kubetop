# Kubeplugin Usage Guide
kubeplugin is a bash script that retrieves resource usage statistics from Kubernetes.

## Prerequisites
* Bash shell
* kubectl command-line tool installed and configured
## Usage
To use kubeplugin, you need to provide three command-line arguments:

1. COMMAND: The operation to perform on the resource (e.g., get, describe).
2. RESOURCE_TYPE: The type of the Kubernetes resource (e.g., pods, services).
3. NAMESPACE: The namespace in which the resource is located.
The script will then retrieve the resource usage statistics for the specified resource in the specified namespace and output them to the console in the format "Resource, Namespace, Name, CPU, Memory".

Here's an example of how to use kubeplugin:

```bash
./kubeplugin.sh get pods my-namespace
```

In this example, get is the operation, pods is the resource type, and my-namespace is the namespace. The script will then retrieve the resource usage statistics for all pods in the my-namespace namespace and output them to the console.

## Troubleshooting
If you encounter an error message like unknown command "po" for "kubectl", make sure you're using the correct command for the resource type. For example, the correct command for pods is pods or pod, not po.