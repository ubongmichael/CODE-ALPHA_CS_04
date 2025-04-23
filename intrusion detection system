Stepts for suricata install on kali

Update Kali Linux Update your system to make sure everything is up to date: sudo apt update
sudo apt upgrade -y

Install Suricata Install Suricata with the following command: sudo apt install suricata -y

Verify Suricata Installation Check the Suricata version to confirm installation: suricata --version

Configure Suricata

a. Edit Configuration Edit Suricata's main configuration file: sudo nano /etc/suricata/suricata.yaml

b. Set Network Interface Find the af-packet section and replace eth0 with your network interface name: af-packet:

interface: eth0
c. Set HOME_NET Variable Update the HOME_NET variable to your local IP range (e.g., 192.168.1.32/24): home-net:

192.168.1.143/24
Enable JSON Output Enable logging in JSON format by uncommenting and configuring the following: outputs:
eve-log: enabled: yes filetype: regular filename: /var/log/suricata/eve.json
Update Suricata Rules Update the default detection rules: sudo suricata-update

Create Custom Rules Create a custom rule file (local.rules) in the rules directory: sudo nano /etc/suricata/rules/local.rules

Include Custom Rules in Configuration Make sure your custom rules file is included in the Suricata config: rule-files:

/etc/suricata/rules/local.rules
Start Suricata in IDS Mode Run Suricata in IDS mode to monitor traffic: sudo suricata -c /etc/suricata/suricata.yaml -i eth0

Check Suricata Logs View Suricata logs (in JSON format) to monitor alerts: cat /var/log/suricata/eve.json Now, Suricata is running in IDS mode and logging events to /var/log/suricata/eve.json.
