# Practical-infrastructure-installation-and-configuration-exercise

**Student Network Login Number** : 705349

## Configuration Implemented
* **Docker Installation:**
    * Installed Docker and verified it using the `hello world` container.
    * Confingured Docker to handle the application process.

* **Nginx Installation and Configuration:**
    * Installed and configured Nginx as a reverse proxy server.
    * Created a directory `/srv/www/student` to serve the web content.
    * Configured the `default` Nginx site file to serve the application from `/srv/www/student`.

* **Wed Application Deployment:**
  * Developed and deployed a simple "Hello, World!" web application.
  * Confirmed the application is avaible via the URL: `http://student-705349-vm1.net.dcs.hull.ac.uk/student/`

* **File Permissions:**
    * Adjusted ownership and permissions for `/srv/www/student`:
        * Owned by `www-data` user and group.
        * Permissions set to allow Nginx to serve file securely.
     
---
## Maintenance Instructions 
* ** Update and Upgrade the Server **
  * Run regular updates to keep the server secure and software up to date:
    ``` sudo apt update && sudo apt upgrade -y ```

* **Restart Nginx**
  * Restart Nginx if configured changes are made:
    ``` sudo systemctl restart nginx ```
  * Test Nginx configurations after editing:
      ``` sudo nginx -t```
    
  * **Docker Status**
      * Ensure Docker is running correctly:
        ``` sudo systemctl status docker```

  * **Monitor server logs**
      * Check Nginx error logs for troubleshooting:
        ``` sudo tail -f /var/log/nginx/error.log ```
      * Review Docker container logs:
        ``` sudo docker logs da3b84a7e702 ```

  * **Backups**
      * Regularly back up the server data and configurations:
        ``` sudo tar -czvf backup.tar.gz /srv/www/student ```

        
    

    
