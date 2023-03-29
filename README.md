# deploy-scripts
Scripts de deploy com git


/home/workdir/scripts/pull-github -d /home/workdir/repos/homologa-hdk-v1 -r  albandes/ituran -b develop


/home/workdir/scripts/deploy-github -d /var/www/html/homologa/ -r /home/workdir/repos/homologa-hdk-v1/ -e /home/workdir/scripts/exclude-homologa-hdk-v1.txt -c /dev/null

```bash
/var/log/deploy.log {
    missingok
    notifempty
    compress
    size 20k
    daily
    create 0600 apache apache
}
```


.netrc
machine github.com login seu-login-no-github password sua-senha-no-github
