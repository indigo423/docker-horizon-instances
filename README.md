# docker-horizon-instances

Run multiple instances of OpenNMS Horizon

Replace in the `192.168.178.46` address with the IP address of your DockerHost in the NGINX site configuration files in ingress/site-conf.d`.

    proxy_pass http://192.168.178.46:8001
    
To distinguish the instances you can use a custom version number by creating a `version.properties` in each instance `horizon-etc/opennms.properties.d/version.properties` with the following content:

```
version.display=23.0.0-customer-1
```

To access the customer instances add the following entries to your local `/etc/hosts` file and resolve to the IP of your DockerHost.

When you run all locally then just add

```
127.0.0.1   customer-1.example.de customer-2.example.de customer-3.example.de customer-4.example.de
```
