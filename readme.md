# **Welcome to the CIE**

This is a simple webpage to Welcome users to the CIE.
It includes the bootstrap and css files.  Ideally, we would want to put the bootstrap stuff outside in case we want to update to a newer version of bootstrap, but for this demo it is fine to keep it inside.
All of the editable information for content of the webpage is in the index.html file

I used an nginx server to run this webpage locally.
After nginx is installed (ie sudo apt-get install nginx), point the nginx server to your website location (see below as "/var/www/site/welcome-to-cie) by editing /etc/nginx/sites-available/default
```
server {
        listen 80;
        listen [::]:80;

        root /var/www/site/welcome-to-cie;
        index index.html index.htm index.nginx-debian.html;

        server_name _;

        location / {
                try_files $uri $uri/ =404;
        }
}
```
