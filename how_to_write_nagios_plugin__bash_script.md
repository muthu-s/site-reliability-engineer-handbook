# How To Write Nagios Plugin – Bash Script

Nagios is IT Infrastructure Monitoring Tool. Nagios is designed as a client/server model application and therefore needs two components to work – Nagios server and Nagios client or agent (NRPE for linux or NSClient++ for Windows). Nagios server is the one who connects to Nagios client and triggers a Nagios plugin to get information from Nagios client. Nagios plugin can be any script which can execute on the Nagios client machine (usually perl or bash script). Of course Nagios plugin scripts must be written to output the correct responses and exit codes Nagios server can understand. In this post we will learn how to write bash Nagios plugin script with correct response and exit codes.

###Let’s write a Nagios Plugin Bash Script!
Prerequisites:
* Working Nagios Server Instance (Read more here for Ubuntu or CentOS)
* Working Nagios NRPE Client Instance

###Important:
* Exit Code 0 = OK
If Nagios plugin script is successfully executed and exits with an exit code 0 then Nagios server will show this check as OK and color it with GREEN color.

* Exit Code 1 = WARNING
If Nagios plugin script is successfully executed and exits with an exit code 1 then Nagios server will show this check as a WARNING and color it with ORANGE color.

* Exit Code 2 = CRITICAL
If Nagios plugin script is successfully executed and exits with an exit code 2 then Nagios server will show this check as CRITICAL and color it with RED color.