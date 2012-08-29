Solar Inverter polling script for the Ginlong GCI-3k inverter. 

It'll probably work with other Ginlong based inverters - try it out and let me know!

This is a really basic script, essentially a hacked down version of the scripts here: http://www.solarfreaks.com/cms2000-inverter-rs232-serial-port-hack-cms-2000-rs232-t271-240.html#p3410

I cut out all of the pvoutput and rrd related stuff since I use this script with Cacti, I also removed the config items I was not using since I didn't see a reason I needed to keep them. Then I added a new config item called "flip" - some of the data within the response needs to be flipped (be12 becomes 12be) and other parts do not.
