# Ubuntu WordPress LAMP

sudo mysql

CREATE DATABASE wordpress DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci;

CREATE USER 'wordpressuser'@'%' IDENTIFIED WITH mysql_native_password BY 'password';

GRANT ALL ON wordpress.* TO 'wordpressuser'@'%';

FLUSH PRIVILEGES;

EXIT;

![Create a User](create-user.png)

# PHP Extensions

sudo apt update

sudo apt install php-curl php-gd php-mbstring php-xml php-xmlrpc php-soap php-intl php-zip

sudo systemctl restart apache2

# wordpress Virtual Host

create a virtual host called 'wordpress'.