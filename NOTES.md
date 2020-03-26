# Healthcheck usages
- Restart
- Traffic shaping
- Alerting

# Conflicting patterns
Retries

# Patterns
## No healthcheck
*Restart*
N/A

*Traffic shaping*
N/A

*Alerting*
+ Based on the ratio of failed HTTP requests indirectly

## Shallow healthcheck
*Restart*
TBD

*Traffic shaping*
+ Guarantees that only healthy services will recieve traffic
+ Reduces failure rate becasue of downtime

- Won't help if dependent services are not operational


*Alerting*
TBD

## Deep healthcheck

## Passive healthcheck

# Technical Notes
Traefik does not provide TCP healthchecks?

# References
https://docs.traefik.io/getting-started/quick-start/
https://landscape.cncf.io/category=service-proxy&format=card-mode&grouping=category&license=open-source&sort=stars