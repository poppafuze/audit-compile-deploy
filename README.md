# audit-compile-deploy

this is just to get the latest copy stored somewhere no matter what.

Instructions:

- Download the tarball somewhere (even /etc/audit is OK)
- be root
- tar -xzvf audit-compile-deploy.tar.gz
- cd audit-compile-deploy
- ./audit-compile-deploy

...it will:
- run some safety checks, 
- - run a find / for SUIDs
- create the rule for SUIDs, 
- move the old rules aside
- copy the rules to /etc/audit/rules
- inject them into the kernel

Caveat:  this version does not maange /etc/audit/auditd.conf.  If that file is malformed, your run will bomb out.
