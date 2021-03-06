# Usage

```
Usage: treehouses [command] ...


Commands:

help [command]                           gives you a more detailed info about the command or will output this
expandfs                                 expands the partition of the RPI image to the maximum of the SDcard
rename <hostname>                        changes hostname
password <password>                      changes the password for 'pi' user
sshkeyadd <public_key>                   adds a public key to 'pi' and 'root' user's authorized_keys
version                                  returns the version of cli.sh command
image                                    returns version of the system image installed
detectrpi                                detects the hardware version of a raspberry pi
ethernet <ip> <mask> <gateway> <dns>     configures rpi network interface to a static ip address
wifi <ESSID> [password]                  connects to a wifi network
staticwifi <ip> <mask> <gateway> <dns>   configures rpi wifi interface to a static ip address
          <ESSID> [password]
bridge <ESSID> <hotspotESSID>            configures the rpi to bridge the wlan interface over a hotspot
      [password] [hotspotPassword]
container <none|docker|balena>           enables (and start) the desired container
bluetooth <on|off>                       switches between bluetooth hotspot mode / regular bluetooth and starts the service
ap <local|internet> <ESSID> [password]   creates a mobile ap, which has two modes: local (no eth0 bridging), internet (eth0 bridging)
timezone <timezone>                      sets the timezone of the system
locale <locale>                          sets the system locale
ssh <on|off>                             enables or disables the ssh service
vnc <on|off>                             enables or disables the vnc server service
default                                  sets a raspbian back to default configuration
wificountry <country>                    sets the wifi country
upgrade                                  upgrades cli.sh package using npm
sshtunnel <add|remove|show>              helps adding an sshtunnel
          <portinterval> [user@host]
led [green|red] [mode]                   sets the led mode
rtc <on|off> [rasclock|ds3231]           sets up the rtc clock specified
ntp <local|internet>                     enables or disables time through ntp servers
```

# Additional Notes
```
wifi - ESSID is the SSID or the network name of your wireless network and password is the password 
       for the corresponding network.

rename - The hostname is a label assigned to the RPI device for identification on a network and 
         is useful for communication amongst different devices. The default hostname is raspberrypi.

ethernet and staticwifi - before using these command, I checked that my network follows the ip range from 
                     192.168.0.1 to 192.168.0.254. To change my ip address to 192.168.0.251, I can 
                     issue the command below given that my router is found at 192.168.0.1 and 
                     that it is also a dns server. Alternatively, you can use Quad9 or CloudFlare's dns server, 
                     which is 9.9.9.9 or 1.1.1.1.
                       > ethernet 192.168.0.251 255.255.255.0 192.168.0.1 192.168.0.1 
```
