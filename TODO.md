# Preparation
[x] Availability monitoring
[x] Availability alerts
[x] Dependent services MongoDB?
https://developer.mongodb.com/quickstart/java-setup-crud-operations

# Healthcheck & traffic shaping
[x] Getting traffic to only healthy services

# Healthcheck alerts
[x] Variable to Prometheus time window
[ ] Alerts for passive TCP health!

# Health & dependencies
[ ] How dependencies affect healthcheck overall
*TBD* - Look all the patterns.
[ ] Healthcheck and retires
[x] Pause / unpause dependent containers

# Healthcheck & restarts
[ ] Liveness and readiness probe
https://kubernetes.io/blog/2020/01/22/kubeinvaders-gamified-chaos-engineering-tool-for-kubernetes/
https://medium.com/faun/how-to-inject-chaos-on-kubernetes-resources-using-litmuschaos-c5ddee457b12

[x] Docker healthchecks?
https://howchoo.com/g/zwjhogrkywe/how-to-add-a-health-check-to-your-docker-container
https://www.katacoda.com/courses/prometheus/docker-metrics
```
echo '{ "metrics-addr" : "127.0.0.1:9323", "experimental" : true }' > /etc/docker/daemon.json
systemctl restart docker
```
The metrics endpoint will be accessible once Docker has begun. You can see the raw metrics 
using 
```
curl localhost:9323/metrics
```

# Research 
[x] Prometheus docs (Katacoda?)
[ ] Envoy docs (Katacoda?)
https://www.envoyproxy.io/docs/envoy/v1.13.1/start/sandboxes/front_proxy#running-the-sandbox
[ ] Watch patterns resiliency
[ ] Insert Envoy with metrics for better observability

# Ideation
[ ] Full patterns map

# LHF
[ ] e2e from Docker container for better portability
[ ] Makefile more variables
[ ] Rename service project
[x] Build image first then start app