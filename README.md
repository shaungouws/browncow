# browncow


NGINX API Gateway - Work in progress
Updated api_backends.conf - added to include


HTTPS consistently seems to be a problem in the browser, despite specifying a port... complete bullshit

POSTMAN
made some changes to the headers in the browncow.com/ api requests to include application/xml and accept image/jpeg when accessing root. This returns the full API request instead of the basic URL being specified.

2022-05-02 20:27

Made changes to nginx.conf --old screenie below:



## Notes on API Gateway deployment
- All NGINX configuration starts with the main configuration file, nginx.conf
- use *include* directive in **http** block that references the GW config 
- **api_gateway.conf**

    include /etc/nginx/api_gateway.conf; # All API gateway configuration'
    
    api_gateway.conf defines the virtual server

    include /etc/nginx/conf.d/*.conf;    # Regular web traffic'


### Progress
touch api_backends.conf

    upstream warehouse_inventory changed to 

configured to backend docker hosting httpbin on 3 ports - 172.31.10.251:80/81/82  
Pickup from *Single-Service vs. Microservice API Backends*