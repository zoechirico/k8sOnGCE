# k8sOnGCE



*create cluster*
```bash
export PROJECT_ID=intrepid-app-299501
export COMPUTE_ZONE=us-central1-f
export CLUSTER_NAME=zdev0

gcloud config set project ${PROJECT_ID}
gcloud config set compute/zone ${COMPUTE_ZONE}

gcloud beta container clusters create ${CLUSTER_NAME} --preemptible  --no-enable-basic-auth  --cluster-version "1.18.12-gke.1201"  --enable-kubernetes-alpha  --no-enable-autoupgrade --no-enable-autorepair


```

## Get Credentials

```bash
export PROJECT_ID=intrepid-app-299501
export COMPUTE_ZONE=us-central1-f
export CLUSTER_NAME=zdev0
gcloud container clusters get-credentials ${CLUSTER_NAME} 

```

## Delete Cluster

```bash

export PROJECT_ID=intrepid-app-299501
export COMPUTE_ZONE=us-central1-f
export CLUSTER_NAME=zdev0
gcloud beta container clusters delete  ${CLUSTER_NAME} 

```


