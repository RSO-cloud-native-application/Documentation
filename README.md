# Uniborrow

Uniborrow is an application allowing users to loan each other items.

## Architecture

The Uniborrow application uses cloud native principles. It consists of
the following microservices:

* Users: [github](https://github.com/RSO-cloud-native-application/uniborrow-users)
* Items: [github](https://github.com/RSO-cloud-native-application/uniborrow-items)
* Loans: [github](https://github.com/RSO-cloud-native-application/uniborrow-loans)
* Requests: [github](https://github.com/RSO-cloud-native-application/uniborrow-requests)
* Chat: [github](https://github.com/RSO-cloud-native-application/uniborrow-chat)
* Cash: [github](https://github.com/RSO-cloud-native-application/uniborrow-cash)
* Reviews: [github](https://github.com/RSO-cloud-native-application/uniborrow-reviews)
* Blogs: [github](https://github.com/RSO-cloud-native-application/uniborrow-blogs)
* Ads: [github](https://github.com/RSO-cloud-native-application/uniborrow-ads)

Frontend source code is located on
[github](https://github.com/RSO-cloud-native-application/uniborrow-frontend).

The application is deployed on Google Cloud, using Kubernetes to
orchestrate the deployment.

## Development information

### Etcd K8S setup

The etcd server is running on the kubernetes cluster. You can see the
pods used by etcd with:

```
$ kubectl get pods
```

To connect to the etcd CLI, execute:

```
$ kubectl exec <pod-name> -it /bin/sh
```

To create a key:

```
etcdctl mk <key-name> <key-value>
```

To modify a key:

```
etcdctl set <key-name> <key-value>
```

To retrieve a key:

```
etcdctl get <key-name> <key-value>
```

To see the directory structure

```
etcdctl ls <key-name>
```
