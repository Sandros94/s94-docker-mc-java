# mc-java Stack
This is going to be a nice readme for the deployment on a swarm of a minecraft java via quilt server, with the explanation of the env variables.


# ENV List
`WORLD_NAME = "NAME"` A simple world name that will be used for the server name too
`HOST_FOLDER_PATH = "/absolute/host/path"` where minecraft will allocate the files and world saves
`NODE_PLACEMENT = [node.hostname == HOSTNAME]` to define on witch node the server will be placed


# To-Do
- [ ] Credits to itzg docker image
- [ ] FAQ on node placement inside a swarm
- [ ] a file browser to make easier for backing/restoring the world?
- [ ] caveats?