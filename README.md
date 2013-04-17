Solar Inverter polling script for the Ginlong GCI-3k inverter. 

I am just using a generic no-name bluetooth adaptor off of ebay. Try using the "official" software first to test: http://www.ginlong.com/Ginlong-technolgoies-download-Grid-Tie-Inverter-Manuals.htm

It'll probably work with other Ginlong based inverters - try it out and let me know!

This is a really basic script, essentially a hacked down version of the scripts here: http://www.solarfreaks.com/cms2000-inverter-rs232-serial-port-hack-cms-2000-rs232-t271-240.html#p3410

I originally cut out all of the pvoutput and rrd related stuff since I use this script with Cacti, I also removed the config items I was not using since I didn't see a reason I needed to keep them. Then I added a new config item called "flip" - some of the data within the response needs to be flipped (be12 becomes 12be) and other parts do not.

I've now re-added some basic pvouput funcitonality - in the config.ini file you should add in your API key and System ID, flip the pvouput option to 1, and set up a cron job to run every minute (or however many times you want to send updates per hour - the maximum is 60 per hour according to the pvoutput API documentation (http://pvoutput.org/help.html#api-ratelimit)

In the inverter Bluetooth settings, make sure it is configured as #1 - or just modify the script.
