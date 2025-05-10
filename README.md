# Helix Proxy
This is a proxy to enable Helix RESTAPI to be accessable from view fields and to be able to send data from iframe to parent form

# Podman
podman build -t helix-proxy-nginx .
podman run -d --name helix-proxy --add-host=pingvin:host-gateway -p 8081:8081   helix-proxy-nginx
