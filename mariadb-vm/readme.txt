Set new password for root account
# mysql_secure_installation

Set DB name and users.
# mysql -u root -p<password>
mysql> create database accounts;
mysql> grant all privileges on accounts TO root identified by '<password>' ;
mysql> FLUSH PRIVILEGES;
mysql> exit;

Download Source code & Initialize Database.
# git clone -b local-setup https://github.com/devopshydclub/vprofile-project.git
# cd vprofile-project
# mysql -u root -p<password> accounts < src/main/resources/db_backup.sql
# mysql -u root -p<password> accounts
mysql> show tables;

Starting the firewall and allowing the mariadb to access from port no. 3306
# systemctl start firewalld
# systemctl enable firewalld
# firewall-cmd --get-active-zones
# firewall-cmd --zone=public --add-port=3306/tcp --permanent
# firewall-cmd --reload
# systemctl restart mariadb
