# Deploy-Prometheus-on-OKD


* Deploy Prometheus : 
  * $ oc version  
  * $ oc login Addres-your-cluster-kube and okd  --token=${PRODUCTION_TOKEN}
  * $ oc project ${OKD_PROJECT}
  * $ oc create configmap prometheus-conf --from-file=prometheus.yml -o yaml --dry-run=clinet | oc replace -f -
  * $ oc apply -f statefulset.yml
  * $ oc apply -f service.yml
  * $ oc apply -f route.yml
