Lert - High reliability systems monitoring
====

Golang load balanced server/client monitoring. Escalation service support with PagerDuty. Easy setup, sane defaults, simple configuration.

Get Started
-----------

    joel@freyr:~> ./lert # Server mode by default
    ***
    Starting up ... Monitoring 1 server (myself)! No remote clients.
    Couldn't log to /var/log/lert/server.log Please create /var/log/lert directory, and set permissions!
    Logging to /Users/joel/.lert/server.log instead
    ***
    Monitoring: disk space, cpu, free memory
    Plugins loaded: None
    Alerting ... no one!
    Archiving ... nowhere!
    ***
    Run a lert client on another server: ./lert --server=192.168.0.1:11912
    Control URL: http://127.0.0.1:11811
    Monitoring URL: http://127.0.0.1:11911
    ***
    
Add a client on another node.

    joel@tyr:~> ./lert --server=192.168.0.1:11912 # Change the IP address to match your system
    ***
    Starting up ... Client mode!
    Couldn't log to /var/log/lert/client.log Please create /var/log/lert directory, and set permissions!
    Logging to /Users/joel/.lert/client.log instead
    ***
    Server on 192.168.0.1:11912
    Monitoring: disk space, cpu, free memory
    Plugins loaded: None
    ***
