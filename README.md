# mc-java Stack
This is going to be a nice readme for the stack deployment on a swarm for a minecraft java server using quilt, with the explanation of the env variables.

## Current configuration
The current configuration is based on a Quilt server using [itzg docker image](https://github.com/itzg/docker-minecraft-server). This let me install a number of Quilt/Fabric mods to optimize a number of performance and redstone-heavy worlds compared to Vanilla/Bukkit/Spigot/Paper server.  

### Suggested server mods are:  
- [Ferritecore](https://modrinth.com/mod/ferrite-core)
- [Krypton](https://modrinth.com/mod/krypton)
- [Lithium](https://modrinth.com/mod/lithium)
- [Starlight](https://modrinth.com/mod/starlight)
- [LazyDFU](https://modrinth.com/mod/lazydfu)
- [SmoothBoot](https://modrinth.com/mod/smoothboot-fabric)
- [FastLoad](https://modrinth.com/mod/fastload)

## ENV List
`WORLD_NAME = "NAME"` A simple world name that will be used for the server name too.  
`HOST_FOLDER_PATH = "/absolute/host/path"` Where minecraft will allocate the files and world saves.  
`NODE_PLACEMENT = [node.hostname == HOSTNAME]` To define on witch node the server will be placed.  

## FAQ
**Q:** Why am I defining where to place the container istance?  
**A:** Since I'm deploying them on a swarm without shared storage, defining on which node the container will be run on prevents from losing its folder and world saves.
## To-Do
- [x] ~~Credits to itzg docker image~~
- [x] ~~FAQ on node placement inside a swarm~~
- [ ] a file browser to make easier for backing/restoring the world?
- [ ] caveats?
- [ ] a more readable FAQ