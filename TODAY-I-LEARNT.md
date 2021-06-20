### increase upload max limit in Wordpress, PHP8.0-fpm and Nginx

Settings form `location /` and `location /wp-admin` there aren't cascading and nginx
processes them separetly.

### some hosts in Zabbix aren't visible

If you have a monitored host try "Full clone" instead of create a new one.

### how to cut a last X characters from various size of strings input

If you want cut, for example, an extension of files, try `rev` twice, i.e.

```bash
ls *.mp4 | rev | cut -c 5- | rev
```

### how to make bash history stick and searchable

First, make a directory `mkdir ~/.logs`

Second, add to `~/.bashrc` this entry 
```bash
export PROMPT_COMMAND='if [ "$(id -u)" -ne 0 ]; then echo "$(date "+%Y-%m-%d.%H:%M:%S") $(pwd) $(history 1)" >> ~/.logs/bash-history-$(date "+%Y-%m-%d").log; fi'
```

After restart bash shell, you will have a daily log of all shell commands like this:

```bash
$ cat ~/.logs/bash-history-2021-06-20.log
(...)
2021-06-20.11:28:52 /home/tom   500  cat ~/.bashrc
(...)
```
