.. contents::

Introduction
============

Use zc.monitor and additional plugins to fetch probes via another thread than the one defined in Zope.

Currently supported probes:
  cache_size -- cache sizes informations
  conflictcount -- number of all conflict errors since startup
  dbactivity -- number of load, store and connections on database (default=main) for the last x minutes (default=5)
  dbinfo -- Get database statistics
  dbsize -- size of the database (default=main) in Ko
  errorcount -- number of error present in error_log (default in the root).
  help -- Get help about server commands
  interactive -- Turn on monitor's interactive mode
  monitor -- Get general process info
  objectcount -- number of object in the database (default=main)
  quit -- Quit the monitor
  refcount -- the total amount of object reference counts
  threads -- Dump current threads execution stack
  unresolved_conflictcount -- number of all unresolved conflict errors since startup
  uptime -- uptime of the zope instance in seconds
  zeocache -- Get ZEO client cache statistics
  zeostatus -- Get ZEO client status information

Once the instance is running zc.monitor thread listen to another port (127.0.0.1:8888 in this buildout). You can query values using
simple python script or nc.

Example:

  echo 'uptime' | nc -i 1 localhost 8888


TODO
====

 - write simple zc.monitor client
