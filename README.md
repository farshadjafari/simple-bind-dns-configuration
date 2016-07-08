#Ubuntu Bind service sample configuration

- if you are using ubuntu, and need to set your dns server with bind or bind9, this script is may help you to do it well.

- change example.com with your domain. and 111.222.333.44 with your server IP.

- save it on a file at /etc/bind/db.yourdomain.com 

- add this to /etc/bind/named.conf.local

zone "yourdomain.com" {
        type master;
        file "/etc/bind/db.yourdomain.com";
};

- finally restart bind

* if you are going to have mail server, you should get your domain key and put it on that line, if not, remove it.