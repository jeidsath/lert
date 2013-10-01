Lert - High reliability systems monitoring
====

Golang load balanced server/client monitoring. 

*Escalation service support.
*Easy setup.
*Sane defaults.
*Simple configuration.

Get Started
-----------

### Server node

    joel@freyr:~> ./lert # Server mode by default

#### Server output:

    Starting up ... No config found in /etc/lert/ /Users/joel/.lert/
    Monitoring 1 server (myself). No remote clients.
    Couldn't log to /var/log/lert/server.log Please create /var/log/lert directory, and set permissions!
    Logging to /Users/joel/.lert/logs/server.log instead
    Monitoring: disk space, cpu, free memory
    Plugins loaded: None
    Alerting ... no one!
    Archiving ... nowhere!
    Specify a key in config for increased security
    Run a lert client on another server: ./lert --server=192.168.0.1:11912
    Control URL: http://127.0.0.1:11811
    Monitoring URL: http://127.0.0.1:11911
    >
    
### Client node(s)

    joel@tyr:~> ./lert --server=192.168.0.1:11912

#### Client output:
    
    Starting up ... Client mode!
    Couldn't log to /var/log/lert/client.log Please create /var/log/lert directory, and set permissions!
    Logging to /Users/joel/.lert/logs/client.log instead
    Server on 192.168.0.1:11912
    Monitoring: disk space, cpu, free memory
    Plugins loaded: None
    >

#### Server output:

    Client connected <tyr:192.168.0.2>. Type "approve tyr" to monitor.
    >

The Lert Command Line
---------------------

Remote control, etc. Uses existing monitoring system to track command completion.

Plugins
-------

Existing nrpe plugins work.
