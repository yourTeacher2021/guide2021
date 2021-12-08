# guide2021





sudo adduser --ingroup admin "username" 
sudo usermod -aG sudo "username" (ajouter au groupe sudoers)
getent group sudo | cut -d: -f4
getent group admin (afficher les admins)
sudo groupadd -g 99999 "groupename"
getent group | grep "groupename"

sudo adduser --ingroup "groupename" "username"
-su -l user
-chmod 700 .ssh
-touch .ssh/authorized_keys 
-nano .ssh/authorized_keys

sudo nano /etc/ssh/sshd_config 
#Authentication
AuthenticationMethods "publickey,password"
PubKeyAuthentication yes
sudo service ssh restart

sudo apt install fail2ban
sudo service fail2ban start
sudo nano /etc/fail2ban/jail.d/custom.conf

sur custom.conf'''[Default]
ignoreip=15.188.81.213(your ip adress to test)
bantime=120	
maxentry=3'''
sudo service fail2ban restart
sudo service fail2ban status
https://aonyx.fr/pdf/notices/procedure-installation-serveur-web.pdf
https://www.digitalocean.com/community/tutorials/how-to-install-the-latest-mysql-on-debian-10
https://debian-facile.org/doc:programmation:mysql
mysql -u root -p
[17:44]
show Databases;
https://drive.google.com/file/d/1thmiwHByfLL1MfW9z0azHIU68Ojqab_4/view?usp=sharing
