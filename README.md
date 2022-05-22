![CREATE A LAMP STACK](https://user-images.githubusercontent.com/84424434/169676451-3ead7bf2-c235-4da6-a383-686d7963eeea.png)

WEB STACK IMPLEMENTATION (LAMP STACK) IN GCP

What is a LAMP stack?

LAMP is an acronym denoting one of the most common solution stacks for many of the web's most popular
applications. However, LAMP now refers to a generic software stack model and its components are largely
interchangeable. -Wiki

L - Linux(operating system)
A - Apache(web server software)
M - MySQL(database)
P - PHP(a general purpose scripting language)

*Some examples of websites that utilize a LAMP Stack are Wordpress & Drupal*

Read more on LAMP here https://www.ibm.com/cloud/learn/lamp-stack-explained

Here are the steps:

Step 1 — installing apache and updating the firewall

Step 2 — installing mysql

Step 3 — installing php

Step 4 — creating a virtual host for your website using apache

Step 5 — enable php on the website

Create a Linux base GCP Instance
(I'm using a RHEL8 image)

<img width="954" alt="image" src="https://user-images.githubusercontent.com/84424434/169677204-bba829a1-5acd-4296-ad70-c631c6d2db41.png">

On the Command Line

<img width="645" alt="image" src="https://user-images.githubusercontent.com/84424434/169677335-dfca2d8c-c6d6-4bc5-9031-1775ac2a17a9.png">


``` sudo yum install httpd -y ```

<img width="508" alt="image" src="https://user-images.githubusercontent.com/84424434/169677946-237cc50b-eaf4-4843-ae64-656ddbb2c992.png">

``` sudo yum systemctl enable --now httpd ```

``` sudo yum status httpd                 ```

<img width="668" alt="image" src="https://user-images.githubusercontent.com/84424434/169678081-d89bb303-b28b-45cb-b8f0-3a13315adba1.png">

``` curl http://localhost:80              ```

<img width="731" alt="image" src="https://user-images.githubusercontent.com/84424434/169678225-9e7b3a86-8145-417b-b37a-6a0d513f06ab.png">

<img width="889" alt="image" src="https://user-images.githubusercontent.com/84424434/169678721-8291df3e-95ac-4021-a825-23dc1e6001d9.png">

``` http://<Public-IP-Address>:80         ```  

<img width="947" alt="image" src="https://user-images.githubusercontent.com/84424434/169678754-9861bcf8-084c-4b88-a73e-46646689820d.png">

MYSQL Installation

```
    sudo yum install @mysql -y            

    sudo systemctl enable --now mysqld
    
    sudo systemctl status mysqld
```

<img width="662" alt="image" src="https://user-images.githubusercontent.com/84424434/169679145-d4982e99-608f-4eec-ad94-f356307443f9.png">

``` sudo sql                              ```

<img width="591" alt="image" src="https://user-images.githubusercontent.com/84424434/169679256-f213414c-c279-449f-b008-4fa64ea3c6e3.png">
