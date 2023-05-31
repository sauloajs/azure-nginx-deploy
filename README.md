# Configuration 
### WEBSITES_ENABLE_APP_SERVICE_STORAGE=true
- Change this setting in environment variables of your app service.

### PHP 8.2

### Create file "default" (without any extensions, or with any other name), the path will be: /home/default with the nginx settings to be overwritten 
- To run a laravel application without route indexing problems you should rewrite the location rules and the root path of your application to be like this: (https://github.com/sauloajs/azure-nginx-deploy/blob/master/nginx.conf).
# source: https://laravel.com/docs/10.x/deployment#nginx

### Custom Startup Command: cp /home/default /etc/nginx/sites-enabled/default; service nginx restart
- This will also be configurated inside the settings of your app, you must place this command in Startup Command inside "General Settings" tab.
