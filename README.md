# OwnCloud_Vagrant_SaltStack


Create a development environment for OwnCloud using Vagrant (for the virtual machine) and SaltStack (for automating provisioning).

----------


# HowTo


This is a ready-to-use vagrant machine (ubuntu/trysty64). In 3 steps you can setup your environment.

Just clone the git repos:

``` BASH
git clone https://github.com/eon01/owncloud_vagrant_saltstack.git
```    

Then:

``` BASH
cd owncloud_vagrant_saltstack
```

Finally:

``` BASH
vagrant up
```

Type http://127.0.0.1:4567/owncloud to access to your local OwnCloud instance.

> **Note:**

> - OwnCloud can work with Sqlite, Mysql or Postgresql databases. In my case, I am working with Mysql.
> - You should change the password, the user and tha database name (Mysql)...etc : Find them in 'Vagrant' file.
> - I am using :
>   - **OwnCloud Formula** https://github.com/saltstack-formulas/owncloud-formula
>   - **Vagrant** https://github.com/mitchellh/vagrant

## Author
Created by [Aymen El Amri](http://eon01.com/blog) as part of  [SaltStack for DevOps](https://leanpub.com/saltstackfordevops/).
