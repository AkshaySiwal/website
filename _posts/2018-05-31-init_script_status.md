---
layout: post
title:  "Linux StatUp script exit status codes"
date:   2018-06-24
desc:   "Test01"
keywords: "aws,cloud,easy,cloudformation,uname,kernel,kernel,iam,lambda,initrdram,initrd,rolebased,rolebasespermissions,ec2permissions,permissions,ec2policy,siwal,adobe,radcom,orange,automation"
categories: [Linux]
tags: [Init,Startup,Linux,Unix,Redhat,CentOS]
icon: fa-linux
---

# **A short note on init scripts exit codes**

```
service <your service> status
```
If the **status** action is requested, the init script will return the following exit status codes.

- **0**	program is running or service is OK
- **1**	program is dead and /var/run pid file exists
- **2**	program is dead and /var/lock lock file exists
- **3**	program is not running
- **4**	program or service status is unknown
- **5-99**	reserved for future LSB use
- **100-149**	reserved for distribution use
- **150-199**	reserved for application use
- **200-254**	reserved


```
service <your service> start 
#or
service <your service> stop
```


In case of an error while processing any init-script action **except for status**, the init script shall print an error message and exit with a non-zero status code:

- **1**	generic or unspecified error (current practice)
- **2**	invalid or excess argument(s)
- **3**	unimplemented feature (for example, "reload")
- **4**	user had insufficient privilege
- **5**	program is not installed
- **6**	program is not configured
- **7**	program is not running
- **8-99**	reserved for future LSB use
- **100-149**	reserved for distribution use
- **150-199**	reserved for application use
- **200-254**	reserved


<br>
<br>
<br>
<br>
### References -
linuxbase.org
