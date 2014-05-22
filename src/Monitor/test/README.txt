This directory contains a generator for fake input JSON files for the reporter, for
stress-testing it. It runs under the LifeCycle agent, which needs to be installed on
your system and in your PATH. Then...

Lifecycle.pl --config fake-monitor.conf --log fake-monitor.log

You will need to modify the config file to set the input 'dropbox' for the Monitor,
and may wish to change other fields too.

In particular, 'CycleTime' and 'nFiles' govern the interval between new JSON files
and the number of files in the FTS job. The defaults are set to fake about 100% of
the expected rate. Note that the number of FTS jobs is arbitrary, the Submitter can
wait longer or shorter intervals to bundle users' files as it likes.
