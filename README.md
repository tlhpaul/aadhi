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
   
# How to Record and Playback

  1. Point your Native/web app to addhi
     - Lets assume that your machine ip address is 10.12.100.12 and addhi is running your machine, then we need to configure the app in such way that it hits the aadhi which is running in a particular ip address and each request of your app should have the actual host and query param details.
        Example: https://10.12.100.12/testhost.com/?format=json&appkey=testkey
  2. Go to config tab in aadhi and enable Proxy Mode and navigate to View Request page to view the request and responses fired through the app
  3. Once you done with the recording, store it under particular feature->flow->scenario
  4. Now switch the aadhi's mode to Server Mode to playback the stubbed response.
  

# Troubleshooting

      To start the apache server - sudo apachectl -k start
      
      To start the mysql server - mysql.server start
      
      To view the log run - (tail -f -n+100 /var/log/apache2/error_log)
      
      To stop the apache server - (sudo apachectl stop)
      
      To restart the apache server in debug mode - (sudo apachectl -k restart)
