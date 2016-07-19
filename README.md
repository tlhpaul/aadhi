# AADHI
Local Development and Test virtualization environment, which facilitates quick and easy development and UI automation testing, with easy ways to record and store requests/responses.

__Usage:__

 2. Multiple Device support
      - It has the capability to respond multiple devices simultaneously
 3. Export and Import feature
      - Multiple users can work on the same feature without any conflicts
 4. Refreshing the stubs using the AADHI is easy as the model has been designed to capture  all the required data's for         hitting the actual production API.
 5. Displaying the JSON responses in pretty JSON format
 6. Eliminating dependency with actual production/test environment
 
     - Using actual production/test environment for automation would be cumbersome as there are more chances of false failures due to network latency and change in data setup. Aadhi will help us to run the automation in stable environment and would eliminate false failures.
 7. Enabled caching using memcached. All the reqeust url and response would be cached while we regarding the stubs using        proxy mode. This gives excellent performance while responding to automation devices in server mode

# How to Setup Aadhi in Mac OSX machine?

   Please follow the below link to install aadhi using setup script
   
   https://github.com/Nordstrom/aadhi-setup-scripts.git

# Useful commands

      To start the apache server - sudo apachectl -k start
      
      To start the mysql server - mysql.server start
      
      To view the log run - (tail -f -n+100 /var/log/apache2/error_log)
      
      To stop the apache server - (sudo apachectl stop)
      
      To restart the apache server in debug mode - (sudo apachectl -k restart)
