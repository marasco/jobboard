# jobboard
==========

=description:
	# jobboard werbsite for AU #

=migration information
	
	# create user in mysql
	mysql> CREATE USER jobboard@127.0.0.1 IDENTIFIED BY 'secr3t.job.b';
	
	# create vhost
	<VirtualHost *:80>
        ServerName local.jobboard.com
        DocumentRoot "/Library/WebServer/Documents/jobboard/public/"
        <Directory /Library/WebServer/Documents/jobboard/>
                Options FollowSymLinks
                AllowOverride All
                Require all granted
        </Directory>
	</VirtualHost>