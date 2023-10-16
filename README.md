# hcpp-mqtt-server
A plugin for Hestia Control Panel (via [hestiacp-pluginable](https://github.com/virtuosoft-dev/hestiacp-pluginable)) that installs the Mosquitto MQTT server and furnishes a UI to manage users. With this plugin installed, a new tab will appear in HestiaCP (adjacent to Web, Database, etc.) called MQTT. The MQTT tab allows one to add username and password authentication MQTT users. A user can be designated as a publisher, subscriber, or both. The username is prefixed with the HestiaCP account username not unlike MySQL/MariaDB databases; this enables a shared MQTT service with unique credentials for all HestiaCP users. 

&nbsp;
## Installation
HCPP-MQTT-Server requires an Ubuntu or Debian based installation of [Hestia Control Panel](https://hestiacp.com) in addition to an installation of [HestiaCP-Pluginable](https://github.com/virtuosoft-dev/hestiacp-pluginable) to function; please ensure that you have first installed pluginable on your Hestia Control Panel before proceeding. Switch to a root user and simply clone this project to the /usr/local/hestia/plugins folder. It should appear as a subfolder with the name `nodeapp`, i.e. `/usr/local/hestia/plugins/mqtt-server`.

First, switch to root user:
```
sudo -s
```

Then simply clone the repo to your plugins folder, with the name `mqtt-server`:

```
cd /usr/local/hestia/plugins
git clone https://github.com/virtuosoft-dev/hcpp-mqtt-server mqtt-server
```

Note: It is important that the destination plugin folder name is `mqtt-server`.

Be sure to logout and login again to your Hestia Control Panel as the admin user or, as admin, visit Server (gear icon) -> Configure -> Plugins -> Save; the plugin will immediately start installing the Mosquitto server and depedencies in the background. 

<!--<br><img src='images/mqtt-server-notify.jpg' width='50%'><br>
<sub>Figure 1 - MQTT Server plugin install notification</sub>-->

A notification will appear under the admin user account indicating *"MQTT Server plugin has finished installing"* when complete. This may take awhile before the options appear in Hestia. You can force manual installation via:

```
cd /usr/local/hestia/plugins/mqtt-server
./install
touch "/usr/local/hestia/data/hcpp/installed/mqtt-server"
```

&nbsp;
## Using MQTT Server
The HCPP-MQTT-Server will automatically create an MQTT Service reachable at the prefixed 'mqtt-' domain (i.e. mqtt-cp.example.com, if your domain/HestiaCP is at cp.example.com). The service will leverage TLS/SSL via Let's Encrypt for live servers or the dev.cc certificate for (CodeGarden PWS)[https://code.gdn/pws] installations.

TBD

## Support the creator
You can help this author's open source development endeavors by donating any amount to Stephen J. Carnam @ Virtuosoft. Your donation, no matter how large or small helps pay for essential time and resources to create MIT and GPL licensed projects that you and the world can benefit from. Click the link below to donate today :)
<div>
         

[<kbd> <br> Donate to this Project <br> </kbd>][KBD]


</div>


<!---------------------------------------------------------------------------->

[KBD]: https://virtuosoft.com/donate

https://virtuosoft.com/donate
