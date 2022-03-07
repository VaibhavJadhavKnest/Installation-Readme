https://www.youtube.com/watch?v=K4kYnLC5ddM
sudo apt install apache2
sudo systemctl stop apache2.service
sudo systemctl start apache2.service
sudo systemctl enable apache2.service
sudo apt-get install mariadb-server mariadb-client
sudo systemctl stop mariadb.service
sudo systemctl start mariadb.service
sudo systemctl enable mariadb.service
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php7.2libapache2-mod-php7.2php7.2-common
sudo apt install php7.2 libapache2-mod-php7.2php7.2-common
sudo apt-get install php7.2 php7.2-cli php7.2-common

sudo apt install php7.3 libapache2-mod-php7.3 php7.3-common
sudo apt install php7.3-mysql php7.3-gmp php7.3-curl php7.3-intl
sudo apt install php7.3-mbstring php7.3-xmlrpc php7.3-gd php7.3-bcmath
sudo apt install php7.3-imap php7.3-xml php7.3-cli php7.3-zip

sudo apt install php7.4 libapache2-mod-php7.4 php7.4-common
sudo apt install php7.4-mysql php7.4-gmp php7.4-curl php7.4-intl
sudo apt install php7.4-mbstring php7.4-xmlrpc php7.4-gd php7.4-bcmath
sudo apt install php7.4-imap php7.4-xml php7.4-cli php7.4-zip

sudo apt install php7.4 libapache2-mod-php8.0 php8.0-common
sudo apt install php8.0-mysql php8.0-gmp php8.0-curl php8.0-intl
sudo apt install php8.0-mbstring php8.0-xmlrpc php8.0-gd php8.0-bcmath
sudo apt install php8.0-imap php8.0-xml php8.0-cli php8.0-zip

sudo nano /etc/php/7.3/apache2/php.ini
sudo nano /etc/php/8.0/apache2/php.ini
sudo systemctl restart apache2.service
sudo systemctl status apache2.service

sudo mysql -u root -p
sudo apt install curl git
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
cd /var/www/html/

git clone https://github.com/salesagility/SuiteCRM.git
composer --version



ls
cd SuiteCRM/
ls
sudo composer install --no-dev
ls
cd ..
ls
cd SuiteCRM/
ls

sudo mysql -u root -p
CREATE DATABASE suitecrm;
CREATE USER 'suitecrm'@'localhost' IDENTIFIED BY 'comsats1234';
GRANT ALL ON suitecrm.* TO 'suitecrm'@'localhost' IDENTIFIED BY 'comsats1234';
FLUSH PRIVILEGES;
EXIT;

sudo chown -R www-data:www-data /var/www/html
sudo chmod -R 755 /var/www/html

http://35.154.18.227/SuiteCRM/install.php
http://35.154.18.227/SuiteCRM/index.php

localhost
suitcrm
comsats1234
sudo systemctl status apache2.service
cd
cd /var/www/html/
ls
sudo systemctl restart  httpd
sudo systemctl restart  apache2.service
sudo systemctl status apache2.service
sudo apt upgrade
cd SuiteCRM/
ls
sudo ufw app list
sudo ufw allow OpenSSH
sudo ufw allow 'Apache Full'
sudo ufw status
sudo ufw app list
sudo ufw status
sudo ufw allow 'Apache Full'
sudo systemctl status apache2
sudo ufw status
sudo systemctl status apache2
sudo ufw status
sudo ufw enable
sudo ufw status
sudo systemctl status apache2
cd ..
sudo ufw status
netstat -ant
sudo systemctl restart apache2
sudo systemctl status apache2
sudo ps aux | grep -E 'apache2|httpd'
sudo killall apache2
sudo ps aux | grep -E 'apache2|httpd'
sudo systemctl status apache2
sudo apache2ctl -t
sudo apache2ctl -S
sudo nano /etc/apache2/sites-enabled/000-default.conf
sudo systemctl reload apache2
sudo systemctl status apache2
sudo systemctl start apache2.service2
sudo systemctl start apache2.service
sudo systemctl restart apache2.service
sudo systemctl status apache2
sudo ls /var/log/apache2/
sudo grep -i -r error /var/log/apache2/
sudo zgrep error /var/log/apache2/error.log.2.gz
sudo nano /etc/apache2/apache2.conf
exit


sudo systemctl status apache2
cd /etc/
ls
sudo apt install php-cli
netstat -plunt | grep "443 \|80 "
apt install net-tools
netstat -plunt | grep "443 \|80 "
curl -I http://localhost
netstat -plunt | grep "443 \|80 "
history
sudo apt-get install php-gd
sudo apt-get install php-intl
sudo apt-get install php-simplexml
sudo apt-get install php-dom

<!-- Start generic footer -->
<footer>
<div id="copyright_data" class="footer_left">
	<div id="dialog2" title="{$APP.LBL_SUITE_SUPERCHARGED}" style="display: none">
	</div>
	<div id="dialog" title="&copy; {$APP.LBL_SUITE_POWERED_BY}" style="display: none">
	</div>
	<div id="copyrightbuttons">
		<a id="admin_options">&copy; {$APP.LBL_SUITE_SUPERCHARGED}</a>
		<a id="powered_by">&copy; {$APP.LBL_SUITE_POWERED_BY}</a>
	</div>
</div>
{if $STATISTICS}
<div class="serverstats">
	<span class="glyphicon glyphicon-globe"></span> {$STATISTICS}
</div>
{/if}
<div class="footer_right">

		<a onclick="SUGAR.util.top();" href="javascript:void(0)">{$APP.LBL_SUITE_TOP}<span class="suitepicon suitepicon-action-above"></span> </a>
</div>
</footer>
<!-- END Generic Footer -->


sudo certbot --apache --agree-tos --redirect --uir --hsts --staple-ocsp --must-staple -d *.knestcrm.com,knestcrm.com --email vaibhav.jadhav@knestaluform.in

sudo certbot --authenticator standalone --installer nginx -d knestcrm.com --pre-hook “service nginx stop” --post-hook “service nginx start”

sudo certbot --authenticator standalone --installer apache -d knestcrm.com --pre-hook "systemctl stop a

apache2" --post-hook "systemctl start apache2"

curl  https://www.knestcrm.com/

grep -Eri 'serveralias|servername' /etc/apache2 | grep -i incipio.it


RewriteEngine on
RewriteCond %{SERVER_NAME} =www.knestcrm.com
RewriteRule ^ https://knestcrm.com%{REQUEST_URI} [END,NE,R=permanent]
RewriteCond %{HTTP_HOST} ^www.knestcrm.com [NC]
RewriteRule ^(.*)$ https://knestcrm.com/$1 [L,R=301]

sudo scp -i Knest-Suit-CRM.pem suger_icon.ico ec2-user@ec2-35-154-18-227.ap-south-1.compute.amazonaws.com:/home/ec2-user
=====================
github token
sudo git clone https://github.com/VaibhavJadhavKnest/crmdeploy.git


VaibhavJadhavKnest
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
=============================

sudo chown -R www-data:www-data .
sudo chmod -R 750 .

sudo chmod -R 770 cache custom modules themes data upload
sudo chmod 770 config_override.php 2>/dev/null

sudo chown -R www-data:www-data .
sudo chmod -R 644 .
sudo chmod -R 644 cache custom modules themes data upload
sudo chmod 644 config_override.php 2>/dev/null


'default_permissions' =>
array (
'dir_mode' => 1528,
'file_mode' => 493,
'user' => '',
'group' => '',
),


'default_permissions' =>
array (
'dir_mode' => 02750,
'file_mode' => 0750,
'user' => 'www-data',
'group' => 'www-data',
),


===========CRM8 server installation=======================
cd crm8
grep -r "Generate Inquiry Receipt/" /var/www/html/
grep -r "<title>SuiteCRM</title>" /var/www/html/
$midnight-blue: #534d64;

grep -r "php.ini" /etc/

find . -type f -exec sed -i 's/Supercharged by SuiteCRM/Developed by Knest/' {} \;
find . -type f -exec sed -i 's/#534d64/#24568C/' {} \;
find . -type f -exec sed -i 's/534d64/24568C/' {} \;

find . -type f -exec sed -i 's/<title>SuiteCRM/<title>Knest CRM/' {} \;
find . -type f -exec sed -i 's/534d64/#24568C/' {} \;
find . -type f -exec sed -i 's/##24568C/#24568C/' {} \;

find . -type f -exec sed -i 's/original/change/' {} \;



find . -type f -exec sed -i 's/navbar{background-color:#534d64/navbar{background-color:#24568C/' {} \;


##24568C
sudo apt install apache2
sudo systemctl enable apache2.service
sudo systemctl stop apache2.service
sudo systemctl restart apache2.service

sudo systemctl status apache2.service

sudo apt-get install mariadb-server mariadb-client
sudo systemctl stop mariadb.service
sudo systemctl start mariadb.service
sudo systemctl enable mariadb.service
sudo systemctl status mariadb.service
sudo apt-get install software-properties-common
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install -y php7.4 libapache2-mod-php7.4 php7.4-common
sudo apt install -y php7.4-mysql php7.4-gmp php7.4-curl php7.4-intl
sudo apt install -y php7.4-mbstring php7.4-xmlrpc php7.4-gd php7.4-bcmath
sudo apt install -y php7.4-imap php7.4-xml php7.4-cli php7.4-zip
sudo nano /etc/php/7.4/apache2/php.ini
file_uploads=On
allow_url_fopen=On
short_open_tag=On
memory_limit=256M
upload_max_filesize=100M
max_execution_time=360
sudo systemctl restart apache2.service
sudo systemctl status apache2.service
sudo apt-get purge php*
sudo apt-get remove php7.4



sudo nano /etc/php/7.3/apache2/php.ini

sudo nano /etc/php/7.3/cli/
sudo mysql -u root -p
CREATE DATABASE suitecrm;
CREATE USER 'suitecrm'@'localhost' IDENTIFIED BY 'comsats1234';
GRANT ALL ON suitecrm.* TO 'suitecrm'@'localhost' IDENTIFIED BY 'comsats1234';
FLUSH PRIVILEGES;
EXIT;
http://version8.knestcrm.com/
sudo apt-get install php7.3-soap 


sudo apt install curl git
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
cd /var/www/html/
sudo git clone https://github.com/salesagility/SuiteCRM-Core.git
https://github.com/salesagility/SuiteCRM-Core.git

sudo git clone https://github.com/VaibhavJadhavKnest/crmdeploy.git

sudo git clone https://github.com/VaibhavJadhavKnest/crmdeploy.git

mv * /var/www/html/
ls
cd SuiteCRM/
ls
sudo composer install --no-dev
ls
cd ..
ls
cd SuiteCRM/
ls
apt-get install php7.4-intl
sudo apt-get purge php8.*
sudo apt-get autoclean
sudo apt-get autoremove

/etc/init.d/php7.4-fpm restart
service php7.4-fpm restart
restart php7.4-fpm
systemctl restart php8.0-fpm.service
sudo chown -R www-data:www-data 
sudo chmod -R 755 /var/www/html/


DocumentRoot /var/www/html/public
<Directory /var/www/html/public>
AllowOverride All
Order Allow,Deny
Allow from All
</Directory>
sudo apt install php-imagick php7.4-fpm php7.4-mysql php7.4-common php7.4-gd php7.4-imap php7.4-json php7.4-curl php7.4-zip php7.4-xml php7.4-mbstring php7.4-bz2 php7.4-intl php7.4-gmp	

sudo apt-get purge php7.3-mysql

sudo apt install php7.3 libapache2-mod-php7.3 php7.3-common
sudo apt install php7.3-mysql php7.3-gmp php7.3-curl php7.3-intl
sudo apt install php7.3-mbstring php7.3-xmlrpc php7.3-gd php7.3-bcmath
sudo apt install php7.3-imap php7.3-xml php7.3-cli php7.3-zip
sudo nano /etc/php/7.3/apache2/php.ini	

[Wed Feb 02 09:03:55.811857 2022] [php7:error] [pid 988] [client 103.139.242.111:53591] PHP Fatal error:  require(): Failed opening required '/var/www/html/vendor/autoload.php' (include_pade_path='.:/usr/share/php') in /var/www/html/config/bootstrap.php on line 35
>

composer install ./vendor/bin/pscss





sudo systemctl restart apache2
sudo a2enmod rewrite
<VirtualHost *:80>
ServerName domain.tld
ServerAlias www.domain.tld

DocumentRoot /var/www/project/public
<Directory /var/www/project/public>
AllowOverride All
Order Allow,Deny
Allow from All
</Directory>
</VirtualHost>

sudo nano /etc/apache2/sites-available/knestcrm.conf

<VirtualHost *:80>
ServerAdmin webmaster@localhost
ServerName knestcrm.com
ServerAlias www.knestcrm.com
DocumentRoot /var/www/knestcrm.com
ErrorLog ${APACHE_LOG_DIR}/error.log
CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
sudo a2dismod php7.3

sudo apt install php-imagick php7.3-fpm php7.3-mysql php7.3-common php7.3-gd php7.3-imap php7.3-json php7.3-curl php7.3-zip php7.3-xml php7.3-mbstring php7.3-bz2 php7.3-intl php7.3-gmp
sudo apt-get install php7.3-


<div class="modal-footer">
		<button class="btn btn-default" type="button" data-dismiss="modal">{$APP.LBL_CANCEL}</button>
		<button id="btn-generic" class="btn btn-danger" type="button">{$APP.LBL_OK}</button>
	</div>


<?php
$GLOBALS['dictionary']['{"Opportunity"}']['fields']['filename'] = array (
'name' => 'filename',
'vname' => 'LBL_FILENAME',
'type' => 'file',
'dbType' => 'varchar',
'len' => '255',
'reportable' => true,
'comment' => 'File name associated with the note (attachment)',
'importable' => false,
);
$GLOBALS['dictionary']['{"Opportunity"}']['fields']['file_mime_type'] = array(
'name' => 'file_mime_type',
'vname' => 'LBL_FILE_MIME_TYPE',
'type' => 'varchar',
'len' => '100',
'comment' => 'Attachment MIME type',
'importable' => false,
);
$GLOBALS['dictionary']['{"Opportunity"}']['fields']['file_url'] = array (
'name' => 'file_url',
'vname' => 'LBL_FILE_URL',
'type' => 'varchar',
'source' => 'non-db',
'reportable' => false,
'comment' => 'Path to file (can be URL)',
'importable' => false,
);
?>

===================================
Content-Type: multipart/mixed; boundary="//"
MIME-Version: 1.0
--//
Content-Type: text/cloud-config; charset="us-ascii"
MIME-Version: 1.0
Content-Transfer-Encoding: 7bit
Content-Disposition: attachment; filename="cloud-config.txt"
#cloud-config
cloud_final_modules:
- [scripts-user, always]
--//
Content-Type: text/x-shellscript; charset="us-ascii"
MIME-Version: 1.0
Content-Transfer-Encoding: 7bit
Content-Disposition: attachment; filename="userdata.txt"
#!/bin/bash
ufw disable
iptables -L
iptables -F
--//
====================================

./vendor/bin/robo upgrade:suite SuiteCRM-8.0.3 upgradeLog.log . admin

nvm install v16

