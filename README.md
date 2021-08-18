# Dynamic Oregen Plugin Minecraft Server
Advance dynamic ore generator common use for skyblock spigot/paper

# Config
```yml
version: 0.0.1

global:
  source: WATER

  reacts:
    - ANY_FENCE
    - LAVA

  generator:
    enable: false
     fallback: COBBLESTONE
     mode: percent
     # mode: count
     random:
        COBBLESTONE: 30.0
        GOLD_ORE: 20.0
        IRON_ORE: 10.0

generators:

  default:
    permission: "vinaore.generator.default"
    worlds:
      world:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

      world_nether:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

  vip:
    permission: "vinaore.generator.mvip"
    worlds:
      world:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

      world_nether:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0
```
