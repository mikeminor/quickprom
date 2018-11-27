Simple prometheus stack that adds in the Traefik proxy to redirect http to https
as well as provide basic authentication for Prometheus. Provides default method
for service discovery and live rule updates for both prometheus and traefik. 
Includes cadvisor for docker metrics, node exporter for node metrics, grafana
for graphing the data.

Installation:

Clone the repo<br>
Edit .env to supply your own domain, ACME e-mail, and authentication string.<br>
Make sure to enable ACME in .env or you won't be able to access sites.<br>
Make sure traefik/acme.json has chmod 600 and correct ownership.<br>
You can generate your auth with htpasswd -nb user pass<br>
docker-compose up -d<br>



