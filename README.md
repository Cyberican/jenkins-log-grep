Jenkins Log Grep
================

Greps for expressions in Jenkins logs.

Usage
-----
Run by providing a regular expression and one or more Jenkins URLs:

    $ ./jgrep.py 'Building in workspace' http://jenkins/
    http://jenkins/job/first_job/3/consoleText:2: Building in workspace /var/lib/jenkins/workspace/first_job
    http://jenkins/job/first_job/2/consoleText:2: Building in workspace /var/lib/jenkins/workspace/first_job
    http://jenkins/job/first_job/1/consoleText:2: Building in workspace /var/lib/jenkins/workspace/first_job
    http://jenkins/job/second_job/2/consoleText:2: Building in workspace /var/lib/jenkins/workspace/second_job
    http://jenkins/job/second_job/1/consoleText:2: Building in workspace /var/lib/jenkins/workspace/second_job

Full usage:

    Usage: ./jgrep.py [options] <pattern> <url> ...

    <pattern>       A regular expression to look for in the logs.
    <url>           The URL of a Job or a View in Jenkins.

    Options:
    --urls-only     Write only the urls of logs containing selected lines.
    --builds-only   Write only the urls of builds having logs containing selected lines.
    --jobs-only     Write only the urls of jobs having logs containing selected lines.
    --no-urls       Suppress the prefixing of urls on output.
