# Dynamic Oregen Plugin Minecraft Server

Advance dynamic ore generator common use for skyblock spigot/paper

## Config

```yml
# Global configuration
global:
  # Source block should be liquid
  source: WATER

  # React block triggered create new block when touch by source block
  reacts:
    - ANY_FENCE
    - LAVA

  # Calculate spawn type of block
  mode: percent

  # Global generator apply for any world
  # ONLY IF local generator not set
  generator:

    # Enable global generator? true/false
    enable: false

    # Disable for custom world
    disallow:
      - world_non_generator

    # If generator block not found 
    # fallback block will be given
    fallback: COBBLESTONE

    # Generator config see all material here:
    # https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/Material.html
    generator:
      COBBLESTONE: 30.0
      GOLD_ORE: 20.0
      IRON_ORE: 10.0

# Local world generators
generators:

  # Group default worlds generator
  # DON'T DELETE THIS
  default:

    # List of world name to enable generator
    worlds:
      skyblock:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

      custom_world_name:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

  # Custom another group for worlds generator
  # If player has permission of this group,
  # Worlds generator will be override default group
  custom_group_1:

    # permission of group
    permission: "vinaore.generator.group1"
    worlds:
      world:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 20.0
          GOLD_BLOCK: 30.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

      world_nether:
        fallback: COBBLESTONE
        generator:
          COBBLESTONE: 30.0
          GOLD_BLOCK: 20.0
          IRON_BLOCK: 15.0
          LAPIS_BLOCK: 2.0

  # Next group will override all previous groups
  # If permission set to player
  vip:
    permission: "vinaore.generator.vip"
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
