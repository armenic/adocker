# WordPress with docker

## Steps  
1. setup a server 
1. install docker and compose from docker site  
1. clone this repo  
1. in Bell router port forwar 80 and 443 to this new server's same ports 
1. up the compose file  
1. use CTRL+Z if you want to send the logs to a background  
1. `docker-compose logs -f` will take you back to the logs 
1. let the wp to be installed, ~5 minutes  
1. navigate to englishrealm.ca  
1. create a site and login  
1. install `wp all in one migrate` add-on 
1. change the `.htaccess` file in both site's volume paths with the following
   content. Comment it later once the importing is done.  
1. change the `proxy/conf.d/custom_proxy_settings.conf` to have 200m. Restore it
   later once the importing is done. 
1. in `wp all in one migrate` import the previously exported backup file  
1. follow the instructions, especially the one that tells that the permalink
   setting need to be opened and saved twice.  
1. revert/comment changes made to .htaccess and custom_proxy_settings  
