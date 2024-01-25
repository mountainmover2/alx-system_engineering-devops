Server Application Deployment for AirBnB Clone

This project focused on deploying our AirBnB clone, involving the configuration of Nginx on ALX-provided web servers to serve a WSGI Flask app through Gunicorn. Additionally, an Upstart script was implemented to ensure the application's persistence through server reboots.

Tasks 📃

1. **Development Setup with Python**
   - Configured the `web_flask/0-hello_route.py` file from the AirBnB_clone_v2 to serve content at `/airbnb-onepage/` on port 5000.

2. **Production Setup with Gunicorn**
   - Established a production environment, installing and configuring Gunicorn to serve the content from task 1.

3. **Nginx Page Serving Configuration**
   - Configured `2-app_server-nginx_config`, an Nginx configuration file directing requests at `/airbnb-onepage/` to the Gunicorn app on port 5000.

4. **Dynamic Routing with Nginx**
   - Configured `3-app_server-nginx_config`, an Nginx configuration file directing requests at `/airbnb-dynamic/number_odd_or_even/<int:num>` to the Gunicorn app on port 5000.

5. **API Configuration**
   - Configured the API from AirBnB_clone_v3 to run on Gunicorn, with `4-app_server-nginx_config` serving as the Nginx configuration file for proxying requests to the corresponding Gunicorn app.

6. **Complete AirBnB App Setup**
   - Configured the complete AirBnB app from AirBnB_clone_v4 to run on Gunicorn, with `5-app_server-nginx_config` serving as the Nginx configuration file for static assets from `web_dynamic/static/`.

7. **Deployment Configuration**
   - Created `gunicorn.conf`, an Upstart script configuration file initiating a Gunicorn process on port 5003, serving the content from task 5. The Gunicorn process includes three worker processes and logs errors to `/tmp/airbnb-error.log` and access to `/tmp/airbnb-access.log`.

8. **Graceful Gunicorn Reload**
   - Implemented `4-reload_gunicorn_no_downtime`, a Bash script facilitating the graceful reloading of Gunicorn to ensure no service interruption.
