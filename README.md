# Zabbix template Rocket Chat statistics
Template using Zabbix for monitoring Rocket Chat Statistics via API.

# Versions
I tested this using zabbix 4.4.10 and Rocket Chat 3.5.0, but maybe it works with different versions.

# Requirements
Zabbix version> 4.2 because template is using HTTP agent and JSON Path. 
* If you need using it in late zabbix version, I recommend https://github.com/tristanlt/zabbix-rocketchat-stats

# Installation
* Download Zabbix template
  * https://github.com/felipemvieira/zbx-rocketchat-template/blob/master/Rocket_chat_template.xml
* Import the template on Zabbix
* Add a Rocket Chat user which contains permissions to view-statistics
* Create a rocketchat api keypair
  * Login user
  * Profile -> My Account -> Personal Access Tokens
* Create a Personal Token
  * Save the ID and Token, you will need this
* Create host on Zabbix and apply the template
* On host configuration, modify macros{$USERAPI_ID} and {$USERAPI_TOKEN} with the information you saved.

