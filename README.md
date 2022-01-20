# ELK-Stack-k8s
### Elastic-Search HA cluster
### Filebeat to catch logs
### Metricbeat + kube-metrics to catch metrics
### Curator Cronjob to autodelete old logs
### A timer logger app that generates periodic logs for test
## Enjoy x)

# Steps:
kuebctl apply -f pv-pvc.yaml
### For whole ES Cluster ( Prod)
kuebctl apply -f elastic-cluster.yaml
### For single ES Node ( Test / Dev )
kuebctl apply -f elastic-mono.yaml
kuebctl apply -f filebeat.yaml
kuebctl apply -f metricbeat.yaml
kuebctl apply -f kibana.yaml
### To test logging, launch test app that generates some logs for you
kuebctl apply -f counter.yaml

## For any improv / suggestions, PR the project or PM me :)
# Happy Logging !