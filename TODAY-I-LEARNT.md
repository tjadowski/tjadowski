### increase upload max limit in Wordpress, PHP8.0-fpm and Nginx

Settings form `location /` and `location /wp-admin` there aren't cascading and Nginx
processes them separetly.

### some hosts in Zabbix aren't visible

If you have a monitored host try "Full clone" instead of create a new one.

### how to cut a last X characters from various size of strings input

If you want cut, for example, an extension of files, try `rev` twice, i.e.

`ls *.mp4 | rev | cut -c 5- | rev`
