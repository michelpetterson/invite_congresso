## Steps ##

1. Clone repository
2. Change parameters in vars.yaml file
3. Populate data.csv with your informations.
4. Run playbook using the command:
   ansible-playbook  congresso_online_invite.yaml
5. Go have a coffe... :-D

* Using Docker Image

1. Pull and run the container using the cmmand:
```
docker container run -ti --mount type=bind,source="$(pwd)/data.csv",target=/ansible-congresso/data.csv michelpetterson/congresso_invite_sender:1.5 /bin/bash 
```

or
```
docker container run -ti --mount type=bind,source="$(pwd)/data.csv",target=/ansible-con    gresso/data.csv michelpetterson/congresso_invite_sender:1.5 ansible-playbook congresso_online_invite.yaml
```

* The command above must be executed in current directory from data.csv.
* Need edit vars.yaml and change smtp parameters.
