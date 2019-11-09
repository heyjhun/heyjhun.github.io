---
layout: post
title: "How to Set Up a Virtual Host?"
author: "HeyJhun"
categories: web-dev-world
description: I am working with localhost for almost a year now but I recently learned from a colleague how to set up a virtual host that is convenient to use instead of using localhost URL.
tags: [documentation,sample]
image: how-to-set-up-a-virtual-host.jpg
---


## Setting Up Virtual Host as Learned from a Colleague

When I was checking out a colleague setting up his localhost environment for the system project he is working on, I noticed on his address bar that it was like a normal URL. It was like xxx.com like a live one.

I said "I thought you were working on localhost, how come your URL is like a live one?" That's when I learned the word "Virtual Host" (Haha such a noob)

So I asked him how he did that. (Thanks Erald!)

Based on what I remember, this is the step how to create your virtual host instead of using "localhost/projectname"

This will serve as my cheat sheet so I won't forget. haha

### Step 1:

Open httpd.conf file present in C:\xampp\apache\conf\httpd.conf
Remove the #(hash) sign before "#Include conf/extra/httpd-vhosts.conf" to include the “httpd-vhosts.conf” file in httpd.conf file.

From

```
# Virtual hosts
#Include conf/extra/httpd-vhosts.conf
```

To

```
# Virtual hosts
Include conf/extra/httpd-vhosts.conf
```

### Step 2:

Create a virtualhost file. To do this, just Open “httpd-vhosts.conf” on this location conf/extra/httpd-vhosts.conf. Copy and add the code below:

```
<VirtualHost *:80>
ServerAdmin webmaster@localhost.com
DocumentRoot <PATH_TO_PROJECT_DIRECTORY_HERE>
ServerName <SERVER_NAME like local.pos.com>
</VirtualHost>
```

Replace ```<PATH_TO_PROJECT_DIRECTORY_HERE & SERVER_NAME>``` with appropriate path directory of your project, Save the file.

### Step 3:

Go to C:\Windows\System32\drivers\etc\hosts

You need to open this file as an Administrator.

Add the line below at the end of the file.

```
127.0.0.1      <SERVER_NAME like local.pos.com>
```

Restart apache server and visit the site URL.