Current Cost Munin plugin
==========================
	
This directory contains a plugin for munin <http://munin-monitoring.org/> to monitor the output of a Current Cost EnviR meter.

Usage:
------

 * Install the files from this repo somewhere sensible
 * Link to the file from /etc/munin/plugins as normal
	cd /etc/munin/plugins
	ln -s /path/to/plugins/currentcost_ currentcost_watts
	ln -s /path/to/plugins/currentcost_ currentcost_temp
 * Set an environment variables. You need to set 'env.path' in your settings top point to the location of current-cost.py (with trailing slash), also you need to run the command as a user with read access to the port (usually root) e.g.

```
echo "[currentcost*]
user root
env.path /path/to/my/plugins/
" > /etc/munin/plugin-conf.d/currentcost
```

 * Restart munin-node

Environment variables:
----------------------

 * env.path: Configure the location of the current-cost.py script
 * env.port: Serial port to connect to (default /dev/ttyUSB0)
 * env.baud: Baud rate (default 57600)

See
---

 * Marcus Povey <http://www.marcus-povey.co.uk>
 * Current Cost <http://www.currentcost.com/>
	 
