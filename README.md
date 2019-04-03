### Build and push the container to your project. 

```
docker build -t gcr.io/[YOUR_PROJECT]/k8s-api-proxy:0.1 ./build
docker push gcr.io/[YOUR_PROJECT]/k8s-api-proxy:0.1
```

Then setup the image values in `values.yaml`.

### To install k8s-api-proxy with new chart release:

Install production with release name `k8s-api-proxy` in `default` namespace:
```
$ helm install --namespace default --name k8s-api-proxy .
```

### To upgrade release by setting values:
```
$ helm upgrade --set image.tag=$TAG --name k8s-api-proxy .
```

### To delete release, use `--purge` to make its name free:
```
$ helm delete k8s-api-proxy
```

Further command and usage, see: 

* [Helm](https://helm.sh/docs/)
* [Creating GKE Private Clusters with Network Proxies for External Access](https://cloud.google.com/solutions/creating-kubernetes-engine-private-clusters-with-net-proxies)
