# `kubecert`: Parse kubeconfig certificate

kubecert is a utility to parse kubeconfig certificate and generate certificate files for furthur usage like curl k8s api server swagger.json

![kubectx demo GIF](img/kubecert.gif)

## Usage

```sh
$ kubecert
Generating ca certificate to ca.pem
Generating context "cluster1" client certificate to cluster1-client.pem
Generating context "cluster1" client key to cluster1-client-key.pem
```

## Installation
Since `kubecert` is written in Bash, you should be able to install them to any POSIX environment that has Bash installed.


## Example

```
curl --cacert ./ca.pem --key ./cluster-key.pem --cert ./cluster.pem  'https://<api-server-ip-address>/swagger.json'
```
