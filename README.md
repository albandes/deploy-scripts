# deploy-scripts
Scripts de deploy com git




mkdir /home/workdir/repos

chown -R apache.apache repos

git clone -b <branch> <remote_repo>

git clone  https://<user>:<token>@github.com/<user>/<remote_repo> .

sudo -u apache composer install
    
    
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

To create .netrc file do next

Fire up Terminal
cd ~ (go to the home directory)
touch .netrc (create file)
open .netrc (open .netrc)
Set required data.
Save
.netrc file should be like this

machine api.mapbox.com
login mapbox
password <secret_key_created_from_your_mapbox_account>
    
