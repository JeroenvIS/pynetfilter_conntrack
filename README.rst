=====================
pynetfilter_conntrack
=====================

libnetfilter_conntrack is a library to manage Linux firewall NetFilter.
pynetfilter_conntrack is a Python binding of this library.  The binding is the
file pynetfilter_conntrack.py and you have also a clone of conntrack program:
conntrack.py.

differences in this fork
========================

This fork contains several python3 fixes. More specifically:

- fixes for python 3.6+
- fix to use correct pointer type to prevent segfault on alpine linux docker containers (and other platforms where the same issue happens)

conntrack.py
============

conntrack.py is a clone of conntrack C program. Features:

 * List connections ;
 * Export connections to XML document ;
 * Delete connection.

For all commands, you can filter connections with:

 * source/destination address from original/reply destination ;
 * layer 3 and 4 protocols ;
 * source/destination port from original/reply destination (protocols tcp,
   udp and sctp).

