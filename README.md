# Nginx-FancyIndex-Theme
My personnal theme of Nginx-FancyIndex.
![screenshot](https://github.com/ArtyumX/Nginx-FancyIndex-Theme/raw/master/screenshot.PNG)

# Requirements
1. nginx
2. fancyindex module (nginx-extras)

# Installation
1. `git clone https://github.com/ArtyumX/Nginx-FancyIndex-Theme.git /etc/nginx/fancyindex_theme`.
2. Edit your virtual host as follow :
```bash
location /  {
    fancyindex on;
    fancyindex_header "/fancyindex_theme/header.html";
    fancyindex_ignore "/fancyindex_theme";
}

location /fancyindex_theme {
    alias /etc/nginx/fancyindex_theme;
    try_files $uri $uri/ =404;
}

```
3. Done!
