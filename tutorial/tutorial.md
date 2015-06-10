# Hybrid Cloud Tutorial (Part 1): Create a Secure Gateway 
See how easy it is to unlock your data for use in mobile and web applications, or for more flexible analysis and reporting. Bluemix Secure Gateway service lets you move data from on-prem to the cloud in a secure manner. This is a multi-part tutorial which shows how to set up a gateway and then build an app on top of it. Here, in Part 1, we’ll cover:

- Secure gateway architecture overview
- How to set up a secure gateway client

## Why use a secure gateway?

Lots of enterprises have valuable data they need to protect. To keep sensitive data secure, databases are often stored on-premise within an organization’s physical location, where staff can protect it more easily. But more and more, organizations also want to host data in the cloud, for fast access and interaction.

Secure gateway lets you safely connect to an on-premise database. It’s like a secure tunnel through which you can access protected data. The gateway encrypts and authenticates user connections, to prohibit unauthorized access.  It’s a way to open your on-premise data to the cloud (and enjoy the flexibility that offers), without actually putting that data in the cloud.

## How secure gateway works

--text and diagram--

## Set up a secure gateway

In this tutorial, we’ll set up a secure gateway for access a sample CouchDB database. Of course, the whole point of a secure gateway is to provide secure, protected access, but here in Part 1, we won’t yet configure specific security settings. First things first: for now, we’ll just set up the basic connection.

## Install Docker client

Docker Engine is a lightweight runtime and packaging tool for apps.  Docker works best on Linux OS. If you want to use Docker on Mac or Windows, just install the helper app, Boot2Docker.  You’ll find all the details and instructions at  https://docs.docker.com/installation/#installation. Just choose your operating system and follow the  instructions.

## Add Bluemix secure gateway service and connect
Now we’re ready to set up the gateway.

1. Go to the Bluemix site: https://console.ng.bluemix.net/
2.  Sign up or sign in.

   If you’re new to Bluemix, you can sign up for a free trial. 

3. Within the left-hand menu, click **Services**.

4. Click **+ Add a service or API**.
5. Scroll down to **Integration** and click **Secure Gateway**.
6. On the upper right of the screen, click the **APP** dropdown and choose **Leave unbound**.
7. Click **Create**.

   The Secure Gateway page opens. 

> **Note:** If you haven’t yet installed the Docker client, you must go do so now (see previous section).

8. Click **Add Gateway**.
9. Enter any name you want for the gateway.
10. Click **Connect it**.

   You now have a secure gateway established. This gateway is an empty tunnel. Next, we’ll send some traffic through it.

11. Under How would you like to connect this gateway? choose Docker.
12. Copy the text and, if you’re on Mac or Windows, add additional text.

   If you’re on Linux, this command works fine as-is. But for Mac and Windows, you need to insert the following additional text, right after `docker run`

   ``` --net=host ```

   Insert spaces on either side. So the beginning of the line looks like this:

   ``` docker run --net=host -it ibmcom/secure-gateway-client… ```

13. Go to your computer’s command line, paste in the text, and press Enter.

   Your gateway client is now connected to Bluemix. 

<p align="center">:--pic--:</p>
<p align="center"><i><strong>Connected!</strong> If you go back and open the gateway in Bluemix, 
status in the upper right corner shows as Connected.</i></p>

   Leave your terminal command line window open. You’ll return to it in a few minutes.


## Set destination

Next, we must set the data source endpoint. This will be the on-premise source database we want to share out to the cloud. For the purposes of this tutorial, we’ll use a simple CouchDB database, which you can download…? ….

On the on-premise machine, install CouchDB.
Visit http://couchdb.apache.org/, then download and installCouchDB.
Return to the Terminal command line you used to connect to Docker.



