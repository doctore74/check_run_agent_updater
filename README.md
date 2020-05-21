# check_run_agent_updater
Force a cmk-agent-update attempt without using the configured agent update interval.

checkmk
https://checkmk.com/
Successfully tested on checkmk RAW version 1.6.0 (stable) on CentOS 7

A working Checkmk agent is required.

```
Check https://<cmkserver>/<site>/run_agent_updater.html for my hostname.
```

If hostname found, run /usr/bin/cmk-update-agent.

Requirements
----
```
- User in WATO (minimum requirements: login)
- Place the local check check_run_agent_updater into your Checkmk agent local check folder (i.e. /usr/lib/check_mk_agent/local/)
- Create a file /opt/omd/sites/<SITE>/var/www/run_agent_updater.html

Syntax for run_agent_updater.html
hostname1
hostname2
...
```

Edit/configure check_run_agent_updater
---------
```
- Set user credentials (USER/PASS)
- Set WEBURL to Checkmk site
```

