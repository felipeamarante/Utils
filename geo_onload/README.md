# geo_onload

Example of HTML file with Javascript that request for location access and pushes to a http endpoint, on load. Please use this at your OWN risk.

![image](https://user-images.githubusercontent.com/14998326/153460475-c8c58873-42e1-4e7d-be01-3c616b67806a.png)


## Resources Needed
 * S3 Bucket with Public READ Access
 * index.html w/ your listener ip address and port
 * Public Reachable Listener (VPS or through Ngrok)
 * Target (User)


## How To
 * Clone index.html and add your Listener IP and Port address at Line 17.
 * Create an S3 Bucket, Upload the index.html and [grant public read to index.html](https://aws.amazon.com/premiumsupport/knowledge-center/read-access-objects-s3-bucket/)
 ![image](https://user-images.githubusercontent.com/14998326/153462342-ac89a1e8-ca1b-4761-8363-531343e10929.png)
 * Get the index.html Object URL (with https) 
 ![image](https://user-images.githubusercontent.com/14998326/153463080-586777fc-3e3f-4f47-97ce-49e6116cec33.png)
 * Start listening using netcat, example to listen on port 5555 `sudo nc -klv 5555`
 * Send the Object URL to the target. If the target open the link and accept to share locations you will see something like this
 ![image](https://user-images.githubusercontent.com/14998326/153466555-3b11ad38-5f71-464a-9822-21e2462c1dcf.png)
 * You can search the Coordinates in Google Map and get the results on the map! 
 ![image](https://user-images.githubusercontent.com/14998326/153466825-bfc25d1f-9985-4eba-abdc-b59c14a8c3ff.png)

