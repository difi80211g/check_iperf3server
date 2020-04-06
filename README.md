# check_iperf3server
Nagios Plugin for Librenms to test iperf3.

Use the nagios plugin to add a service to librenms to test iperf3 throughput and graph results.  Alerts can be setup for failing test results.

The librenms instance will act as the client and the monitored endpoint that you setup the service under in LibreNMS needs to be running as the iperf3 server.  

Librenms Requirements
pip install iperf3

Install check_iperf3server in the nagios plugin directory.  Typically (/usr/lib/nagios/plugins).  make sure to set permissions: chmod +x check_iperf3server

Usage:
Add the iperf3server as a service under a monitoring endpoint.
Enter the IP Address if different than the host
Arguments:
-p iperf3 Server Port
-w Warning level (in MB)
-c Critical level (in MB)
-l Length of iPerf Test (in seconds)
-debug enter 2 for debug output

example:
-w 800 -c 500 -l 10
