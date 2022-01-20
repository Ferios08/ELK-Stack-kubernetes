# ELK-Stack-k8s
### Elastic-Search HA cluster
### Filebeat to catch logs
### Metricbeat + kube-metrics to catch metrics
### Curator Cronjob to autodelete old logs
### A timer logger app that generates periodic logs for test
## Enjoy x)

# Steps:
kubectl apply -f pv-pvc.yaml
### For whole ES Cluster ( Prod)
kubectl apply -f elastic-cluster.yaml
### For single ES Node ( Test / Dev )
kubectl apply -f elastic-mono.yaml
kubectl apply -f filebeat.yaml
kubectl apply -f metricbeat.yaml
kubectl apply -f kibana.yaml
### To test logging, launch test app that generates some logs for you
kubectl apply -f counter.yaml

## For any improv / suggestions, PR the project or PM me :)
# Happy Logging !