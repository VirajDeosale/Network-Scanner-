# Network-Scanner-
Simple Network Scanner Web App (nmap)

This project allows you to create a simple network scanner that is accessible from a web browser on the network.

Essentially with this project we use a Cron Job every 10 minutes to trigger nmap to scan out network and output the results into a text file. We then use a php file to format the text file, add a few things, and present the results for a web browser.

Prerequisites:

Linux – Cron Jobs for Scheduled Tasks (crontab)
Linux – Change Permissions and Ownership for Files and Folders (chmod, chown, members, groups)


Install Apache2, PHP and nmap

sudo apt-get install apache2

sudo apt-get install php

sudo apt-get install nmap


Configure Ownership and Permissions (This is a Bad Idea)

sudo chown ubuntu /var/www/html

sudo chmod 777 /var/www/html




Cron Job Configuration

sudo crontab -e

*/10 * * * * nmap 192.168.1.0/24 -oN /var/www/html/nmap.html




network.php

<?php

echo "Server Timestamp: ";
echo date("h:i:sa");

echo "<pre>";
include("nmap.html");
echo "</pre>";

?>
