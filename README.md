# Network-Scanner-
Simple Network Scanner Web App (nmap)

This project allows you to create a simple network scanner that is accessible from a web browser on the network.

Essentially with this project we use a Cron Job every 10 minutes to trigger nmap to scan out network and output the results into a text file. We then use a php file to format the text file, add a few things, and present the results for a web browser.

Prerequisites:

Linux – Cron Jobs for Scheduled Tasks (crontab)
Linux – Change Permissions and Ownership for Files and Folders (chmod, chown, members, groups)

