## General

### Are you looking for more information?

1. Based on: https://github.com/strimzi/strimzi-kafka-operator.git
2. Documentation: https://strimzi.io/documentation/
3. Chart Source: https://github.com/strimzi/strimzi-kafka-operator/tree/main/helm-charts/helm3/strimzi-kafka-operator


## Before Installation


> **Note:**
> no action required

## After Installation

> **Note:**
> no action required

## Before Upgrade

> **Note:**
> no action required

## After Upgrade

> **Note:**
> no action required


## Tips and Tricks

> **Note:**
> no tips and tricks


## Known Issues

> **Note:**
> Notify us: https://github.com/SourceMation/charts/issues



## CLI installation

### Preparation

```bash
export CHART_NAMESPACE=lp-system
export CHART_VERSION=0.1.2

kubectl create ns ${CHART_NAMESPACE}
kubectl config set-context --current --namespace ${CHART_NAMESPACE}
```

### Go go helm

``` bash
helm -n ${CHART_NAMESPACE} upgrade --install strimzi-cluster-operator \
--repo https://charts.sourcemation.com/ \
strimzi-kafka-operator \
--version ${CHART_VERSION}
```

### Validation and Testing

```bash
kubectl -n ${CHART_NAMESPACE} get po
```

## CLI removing

```bash
helm -n ${CHART_NAMESPACE} uninstall strimzi-cluster-operator
kubectl get crd -o name | grep -i strimzi | xargs kubectl delete
```
