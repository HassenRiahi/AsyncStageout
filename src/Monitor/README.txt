Check the monitor.conf file. Read the comments, and adjust values as you see fit.

Then set up your environment. The monitor requires the PHEDEX-micro package,
testing it in standalone (emulated) mode also requires PHEDEX-lifecycle. There's
a 'doc/setup.sh' script that might work out of the box for you, try it and see.

Then run the monitor with:

> ./ASO-monitor.pl --config monitor.conf

The logfile will be written to the location specified in the config file.

If you change the config file while the monitor is running, it will re-read it
and update its parameters. All except for the location of the logfile, that's
fixed on startup and won't change.
