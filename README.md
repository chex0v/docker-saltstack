# Example for [saltstack](https://docs.saltproject.io/salt/install-guide/en/latest/) in docker

For start run `docker compose up -d`.
After start you must set key for minion from master. 

For this call

`docker container exec -it master salt-key -A`

After this you can check work

`docker container exec -it master salt '*' test.version`

You must see like this

```
docker container exec -it master salt '*' test.version

slave2:
    3006.3
slave1:
    3006.3
```
