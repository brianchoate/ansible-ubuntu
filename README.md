# ansible-ubuntu
Battle school for ubuntu based systems

```
mkdir ~/.battleschool/cache -p

source /opt/battleschool/bin/activate ; battle --config-file https://raw.githubusercontent.com/brianchoate/ansible-ubuntu/master/config.yml
```

## Possible issues.
If you see something like:
```
Fatal Task: localhost => Authentication or permission failure.  In some cases, you may have been able to authenticate and did not have permissions on the remote directory. Consider changing the remote temp path in ansible.cfg to a path rooted in "/tmp". 
```
Do this:
```
sudo chown -R USERNAME:USERNAME ~/.ansible/
```

If you see something like:
```
Task FAILED: get_url Destination /tmp/downloaded_config.yml not writable
```
Do this:
```
sudo rm /tmp/downloaded_config.yml
```


