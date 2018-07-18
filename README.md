# Redmine-War-Board

Redmine war board using the built in redmine API, jQuery and datatables.net

# Docker setup

For testing I spun up two docker containers, an older version 2 and a new version 3. The shell script for this is here:

https://github.com/charleyza/DockerDemo/tree/master/Docker%20(Linux)/Ubuntu/redmine

For help setting up docker: https://carlpaton.co.za/category/docker/

# Enable API

Version 3.4.6; Administration -> Settings -> API
Check: 'Enable REST web service'
Check: 'Enable JSONP support'

For older versions:

Version 2.6.6; Administration -> Settings -> Authentication
Check: 'Enable REST web service'
Check: 'Enable JSONP support'

# API access key
pass as ?key=82d03d58d59c5eae4a2f8560646e329c9644f619

# Resource 'issues'

Example: http://192.168.0.106:3001/issues.json?key=ca9dd590bd031d0c77b6a5dd83464bff313a3593&sort=id%3Adesc&tracker_id=6

* issues.json
This is the resource

* ?key=ca9dd590bd031d0c77b6a5dd83464bff313a3593
This is the authentication key created in redmine

* Resource Filters

This will sort the on the given column desc:

&sort=id%3Adesc

This will filter on the project:

&project_id=1

# References

* https://www.redmine.org/projects/redmine/wiki/Rest_Issues
* https://www.redmine.org/projects/redmine/wiki/Rest_api#Authentication
* https://www.redmine.org/projects/redmine/wiki/Rest_api
* https://tomassetti.me/using-the-redmine-api-to-create-a-page-where-to-quickly-add-and-edit-tasks/
* http://json.parser.online.fr/
* https://stackoverflow.com/questions/1215392/how-to-quickly-and-conveniently-disable-all-console-log-statements-in-my-code
* http://api.jquery.com/jquery.ajax/
* http://api.jquery.com/append/
* https://datatables.net/
* https://datatables.net/manual/tech-notes/3
