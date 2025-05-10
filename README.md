# Helix Proxy
This is a proxy to enable Helix RESTAPI to be accessable from view fields and to be able to send data from iframe to parent form

# 1. Container
Build the container and make sure that you can connect to the port you have set up for the proxy in "nginx.conf" (default 8081)
Also replace the url:s with yours (example: http://pingvin:8080)
    "listen 8081" - Your new Proxy (This container)
    http://<URL>:8080 - Midtier

# 2. Deploy application
Deploy the application to your Helix Innovation Suite environment using Developer Studio

# 3. Test
You can test from the form "HELIX-PROXY:Demo".

    Set up a url for REST-API in URL-field and press the "JS Fetch"-button
    If all is set up correct you will be able to see json result in "RestResult"-field



# Podman commands
podman build -t helix-proxy-nginx .
podman run -d --name helix-proxy --add-host=pingvin:host-gateway -p 8081:8081   helix-proxy-nginx
