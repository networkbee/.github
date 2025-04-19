# network bee
**network bee** is the core codebase for a modular, high-performance minecraft network.

---

## tech stack
network bee uses the **mmgr** stack:

- **mongodb** – a fast nosql database.  
- **minestom** – a lightweight, high-performance minecraft server framework.  
- **gate** – a minimalist, fast, and modular proxy.  
- **rouille** – a rust-based http server used to expose apis for backend services.

### components

| name | description |
|-|-|
| **beekeeper** | the docker orchestrator that manages handles creating, destroying and providing instances for the network. |
| **bee** | a minestom server monorepo for networkbee, contains all of the main server code and the game code. |
| **drone** | a gate proxy for networkbee, handles sending players between bee instances. |
| **queen** | a REST api server for networkbee, handles interfacing with backend systems rabbitmq, mongodb and beekeeper and middleman logic. |
| **hive** | a minestom entrypoint server for networkbee, contains all the code for the entrypoint. |

### libaries

| name | description |
|-|-|
| **pollen** | a display libary for phyiscal display elements. |
| **honey** | a ui libary for minecrafts gui elements. |
| **nectar** | a inventory ui libary for creating and managing inventory-based ui. |

### docker
network bee is fully **docker-contained**, allowing bee, queen and drone to all be scaled dynamically and beekeeper, hive, mongodb and rabbitmq to be isolated from the host.
