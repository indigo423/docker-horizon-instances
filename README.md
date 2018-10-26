# docker-horizon-instances

Run multiple instances of OpenNMS Horizon

Replace in the `192.168.178.46` address with the IP address of your DockerHost in the NGINX site configuration files in ingress/site-conf.d`.

    proxy_pass http://192.168.178.46:8001
    
To distinguish the instances you can use a custom version number by creating a `version.properties` in each instance `horizon-etc/opennms.properties.d/version.properties` with the following content:

```
version.display=23.0.0-customer-1
```
