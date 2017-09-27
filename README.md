ChangeIP AutoUpdate
===================

I use this script to update my dynamic IP address on ChangeIP.com automatically. The free plan works great for me. So, all goes together 100% free.

As long as you run Python 2 and the according libraries, you can use whatever device and operating system you desire. I currently run it on a single board computer.


Usage
=====

You just need to enter your ChangeIP data in the according section. Meaning the URL to update the IP for, your username and your password. 

Since the username and password are in the file in clear text, make sure to use adequate security settings or if necessary add the according modifications. Also, before you run it, don't forget to make 
sure your permissions are set properly (chmod +x changeip). Once done just run the script with Python 2.

For automation I suggest using a cron job or say the TaskManager in Windows. Due to the IP lifetime, ChangeIP suggests to run the cron job at a max of every 5 minutes.


What It Does
============

The script fetches the external IP address of the host it's running on, as well as the IP address of the URL it's supposed to update. It compares the 2 URLs and in case they are different, it updates 
the IP for the according URL on ChangeIP.com.


Update Multiple URLs
====================

I only update one URL, since for me that's enough for one Internet connection. If you want to update more than 1 URL, i suggest using sets. For my free account ChangeIP.com supports 2 sets. So, in your 
account you need to add the according URLs to one of the 2 sets, then update the whole set. In this case, at the end of the udurl string change '&host=' to '&set=1' (for set 1 or 2 for set 2) and 
remove the rest of the line after the last quotation mark (+ iphost). And yes, despite updating a whole set, do provide one URL for the comparison. That should do the trick ;)
