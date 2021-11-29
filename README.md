# Uniborrow

Uniborrow is an application allowing users to loan each other items.

## Architecture

The Uniborrow application uses cloud native principles. It consists of
the following microservices:

* Users: [github](https://github.com/RSO-cloud-native-application/uniborrow-users)
* Items: [github](https://github.com/RSO-cloud-native-application/uniborrow-items)
* Loans: [github](https://github.com/RSO-cloud-native-application/uniborrow-loans)


The application is deployed on Google Cloud, using Kubernetes to
orchestrate the deployment.

## Development information

### Consul K8S setup

The consul servers are running on the kubernetes cluster. You can see
the pods used by Consul with:

```
$ kubectl get pods
```

To connect to the Consul CLI, execute:

```
$ kubectl exec <pod-name> -it /bin/sh
```

Currently the pod name is `consul-consul-server-0`. The UI is
currently not exposed via the load balancer.
