# API Proxies (api-proxies)
An index and topic collection covering reverse-proxy and edge-proxy software used in front of APIs, including HTTP reverse proxies, edge proxies, load balancers, caching proxies, and service mesh sidecars. API proxies sit between API consumers and upstream services to provide TLS termination, routing, rate limiting, observability, traffic shaping, caching, authentication enforcement, and resilience features such as retries and circuit breaking. This collection includes general-purpose reverse proxies like NGINX, HAProxy, Caddy, Apache HTTP Server, Traefik, and Varnish, edge and service mesh proxies like Envoy, Linkerd2-proxy, Istio, Consul Connect, and AWS App Mesh, and proxy-oriented gateways like KrakenD, Tyk, Ambassador, Emissary, and Apache APISIX that overlap with the API gateway category but operate primarily as L7 proxies.

**URL:** [https://apievangelist.com](https://apievangelist.com)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - Reverse Proxy, Edge Proxy, API Proxy, Service Mesh Sidecar, Load Balancer, HTTP Proxy, Ingress

## Timestamps

- **Created:** 2026-05-19
- **Modified:** 2026-05-19

## Common Properties

- [Portal](https://apievangelist.com)
- [GitHubOrganization](https://github.com/api-evangelist)
- [JSONSchema - Proxy Route Schema](https://raw.githubusercontent.com/api-evangelist/api-proxies/refs/heads/main/json-schema/api-proxies-proxy-route-schema.json)
- [JSONSchema - Upstream Cluster Schema](https://raw.githubusercontent.com/api-evangelist/api-proxies/refs/heads/main/json-schema/api-proxies-upstream-cluster-schema.json)
- [JSON-LD](https://raw.githubusercontent.com/api-evangelist/api-proxies/refs/heads/main/json-ld/api-proxies-context.jsonld)
- [Vocabulary](https://raw.githubusercontent.com/api-evangelist/api-proxies/refs/heads/main/vocabulary/api-proxies-vocabulary.yaml)

## Features

| Name | Description |
|------|-------------|
| Layer 7 Reverse Proxying | API proxies terminate HTTP/HTTPS connections from clients and forward requests to upstream API services, hiding internal topology and providing a single front door. |
| TLS Termination and mTLS | Proxies like NGINX, HAProxy, Envoy, and Linkerd2-proxy terminate TLS at the edge and can enforce mutual TLS between services in a mesh. |
| Routing and Traffic Splitting | Edge proxies route requests by host, path, header, or method, and support traffic splitting, canary releases, and blue-green deployments. |
| Rate Limiting and Throttling | Reverse proxies enforce rate limits, quotas, and concurrency limits at the edge to protect upstream APIs from abuse and overload. |
| Caching and HTTP Acceleration | Caching proxies like Varnish, NGINX, Squid, and Cloudflare cache API responses to reduce upstream load and improve client latency. |
| Observability and Access Logging | Proxies emit structured access logs, metrics, and traces (OpenTelemetry, Prometheus, statsd) for every request crossing the edge or mesh. |
| Service Mesh Sidecar Pattern | Sidecar proxies like Envoy, Linkerd2-proxy, and Consul Connect run alongside each service to provide identity, encryption, retries, and traffic policy without changing application code. |
| WAF and Edge Security | Edge proxies and CDNs like Cloudflare, Akamai, and Azure Application Gateway provide WAF rules, bot mitigation, and DDoS protection in front of APIs. |

## Use Cases

| Name | Description |
|------|-------------|
| API Edge Termination | Front internal APIs with NGINX, HAProxy, or Envoy to handle TLS, HTTP/2, HTTP/3, compression, and request normalization before requests reach application servers. |
| Multi-Cluster Ingress | Use Envoy Gateway, Emissary, Ambassador, or Traefik as Kubernetes ingress controllers to expose APIs running across multiple clusters and namespaces. |
| Service Mesh East-West Traffic | Deploy Istio, Linkerd, or Consul Connect to manage service-to-service API calls with mTLS, retries, and traffic policy inside a Kubernetes cluster. |
| Global API Acceleration | Front public APIs with Cloudflare, Fastly, or Akamai to terminate connections at the edge, cache safe responses, and absorb DDoS traffic. |
| Canary and Progressive Delivery | Use proxy-based traffic splitting in Envoy, Istio, or Linkerd to shift a percentage of API traffic to a new version and roll back on error budget breach. |
| Legacy API Modernization | Place HAProxy, NGINX, or Apache HTTP Server in front of legacy SOAP or HTTP services to add TLS, modern auth, rate limiting, and observability without rewriting the backend. |
| API Migration and Strangler Pattern | Use a reverse proxy to gradually route traffic from a legacy monolith API to new microservice APIs based on path or header rules. |

## Integrations

| Name | Description |
|------|-------------|
| Envoy | CNCF L7 proxy used as the data plane for Istio, Consul Connect, Envoy Gateway, Ambassador, and Emissary, with an xDS configuration API. |
| NGINX | Widely deployed open-source web server and reverse proxy with HTTP/2, HTTP/3, load balancing, caching, and Lua-based extension via OpenResty. |
| HAProxy | High-performance TCP and HTTP reverse proxy and load balancer with a runtime Data Plane API for dynamic configuration. |
| Traefik | Cloud-native reverse proxy and ingress controller with automatic service discovery for Kubernetes, Docker, and Consul. |
| Caddy | HTTP/2 reverse proxy with automatic HTTPS via ACME, a JSON config API, and a plugin architecture. |
| Istio | Service mesh that uses Envoy sidecars to provide mTLS, traffic management, and policy for Kubernetes APIs. |
| Linkerd | Lightweight CNCF service mesh built around a purpose-built Rust micro-proxy (linkerd2-proxy) for east-west API traffic. |
| Cloudflare | Global edge proxy and CDN providing TLS termination, WAF, bot management, and caching in front of APIs and websites. |

## Artifacts

Machine-readable API specifications organized by format.

### JSON Schema

- [Proxy Route Schema](json-schema/api-proxies-proxy-route-schema.json)
- [Upstream Cluster Schema](json-schema/api-proxies-upstream-cluster-schema.json)

### JSON Structure

- [Proxy Route Structure](json-structure/api-proxies-proxy-route-structure.json)
- [Upstream Cluster Structure](json-structure/api-proxies-upstream-cluster-structure.json)

### JSON-LD

- [API Proxies Context](json-ld/api-proxies-context.jsonld)

## Vocabulary

- [API Proxies Vocabulary](vocabulary/api-proxies-vocabulary.yaml) — Unified taxonomy mapping resources, actions, workflows, and personas across reverse proxies, edge proxies, and service mesh sidecars

## Network

This index references the following API proxy and edge-proxy repositories:

- [Akamai](https://github.com/api-evangelist/akamai)
- [Ambassador](https://github.com/api-evangelist/ambassador)
- [Apache APISIX](https://github.com/api-evangelist/apache-apisix)
- [Apache HTTP Server](https://github.com/api-evangelist/apache-httpd)
- [Apache Tomcat](https://github.com/api-evangelist/apache-tomcat)
- [AWS App Mesh](https://github.com/api-evangelist/aws-app-mesh)
- [Azure Application Gateway](https://github.com/api-evangelist/microsoft-azure-application-gateway)
- [Caddy](https://github.com/api-evangelist/caddy)
- [Cloudflare](https://github.com/api-evangelist/cloudflare)
- [Consul Connect](https://github.com/api-evangelist/consul-connect)
- [Emissary-Ingress](https://github.com/api-evangelist/emissary-ingress)
- [Envoy](https://github.com/api-evangelist/envoy)
- [Envoy Gateway](https://github.com/api-evangelist/envoy-gateway)
- [F5 Networks](https://github.com/api-evangelist/f5-networks)
- [Fastly](https://github.com/api-evangelist/fastly)
- [frp](https://github.com/api-evangelist/frp)
- [HAProxy](https://github.com/api-evangelist/haproxy)
- [Istio](https://github.com/api-evangelist/istio)
- [Kong](https://github.com/api-evangelist/kong)
- [KrakenD](https://github.com/api-evangelist/krakend)
- [Linkerd](https://github.com/api-evangelist/linkerd)
- [NGINX](https://github.com/api-evangelist/nginx)
- [NGINX Service Mesh](https://github.com/api-evangelist/nginx-service-mesh)
- [Sozu](https://github.com/api-evangelist/sozu)
- [Squid](https://github.com/api-evangelist/squid)
- [Traefik Labs](https://github.com/api-evangelist/traefik)
- [Tyk](https://github.com/api-evangelist/tyk)
- [Varnish Cache](https://github.com/api-evangelist/varnish)

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
