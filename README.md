# headscale-ui-npm

```
version: '3.6'
services:
  headscale:
    container_name: headscale
    image: headscale/headscale:latest
    command: headscale serve
    restart: unless-stopped
    ports:
      - '8089:9090'
      - '8088:8080'
    volumes:
      - ./data:/etc/headscale
      - ./config:/var/lib/headscale      
  headscale-ui:
    image: ghcr.io/gurucomputing/headscale-ui:latest
    restart: unless-stopped
    container_name: headscale-ui
    ports:
      - 8090:80
```

Domain name "hsui.mydomin.net", this would resolve to the NPM server IP

![SCR-20230928-kwqu](https://github.com/ithakaa/headscale-ui-npm/assets/21322369/25282265-77f2-4899-95f9-6597abbb532b)

Leave "Custom Locations" blank

![SCR-20230928-kwsg](https://github.com/ithakaa/headscale-ui-npm/assets/21322369/414435c9-0a6d-403b-af91-6dabe27f1d58)

Select your SSL Cert

![SCR-20230928-kwtt](https://github.com/ithakaa/headscale-ui-npm/assets/21322369/740cf149-73c8-4262-85fc-516b320c908f)

Replace 192.168.0.154 with your headscale server IP address

![SCR-20230928-kwvz](https://github.com/ithakaa/headscale-ui-npm/assets/21322369/fc16bcb7-e451-409e-b882-75f8c81aab42)

