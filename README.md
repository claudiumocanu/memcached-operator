# memcached-operator

> A simple operator with a CRD for TESTING and LEARNING only.

## Boilerplate

```sh
operator-sdk init --domain claudiu.go --repo github.com/claudiumocanu/memcached-operator
operator-sdk create api --group cache --version v1alpha1 --kind Memcached --resource --controller
```

## Operator docker image

- Update `IMAGE_TAG_BASE ?= <registry>/memcached-operator` and `IMG ?= $(IMAGE_TAG_BASE):$(VERSION)`  
- Build and push the image:

```sh
make docker-build docker-push
```

## Deploy the operator in the cluster

```sh
make deploy
```
