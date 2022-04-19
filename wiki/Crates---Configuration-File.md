# Crates - Configuration File

It is possible to configure the crates from the configuration file. You can view an example crates configuration file [here](https://pastebin.com/uDhvmkxS) to also help you.

All crates that are created will have the following format in the crates.yml file:

```yml
test:
  enabled: true
  display-name: Test
  block-material: ENDER_CHEST
  rarity: COMMON
  animation:
    standby-effects:
    - 'WHITE_ASH, #FF0000, 0.0, 0.0, 0.0, 1.0, 0.1, DEFAULT, 2'
    - 'PORTAL, #FFFFFF, 0.0, -1.0, 0.0, 0.0, 0.0, SPIRAL, 2'
    - 'REDSTONE, #9933FF, 0.0, -0.1, 0.0, 0.0, 0.0, CIRCLE, 1'
    - 'SPELL_MOB_AMBIENT, #FF00FF, 0.0, 0.0, 0.0, 1.0, 0.0, DEFAULT, 4'
    opening-type: KEY_OPENER
  item:
    material: TRIPWIRE_HOOK
    display-name: '&aTeste1 Key'
    lore:
    - '&7This is a lore line!'
    - '&7Rarity: {rarity}'
    - ''
    - '&eUse this key in &6{crate}&e!'
  rewards:
  ...
```

Below you can also see the meaning of each field:

* **enabled** - This field has the function of activating and deactivating a create, so if it is disabled, no crate of this type will be available for the players.

* **display-name** - This field has the function of naming this crate that will be used to represent the crate (e.g. will change the hologram name).

* **block-material** - This field will define the block material itself for all crates of this type. Usually the common is a normal chest or an end chest.

* **rarity** - This field has no specific functionality, is only used to categorize a crate. If you don't want to have a rarity for each crate, you can ignore this field and leave it in "COMMON".

* **animation** - This group has a set of two fields that are not recommended to be changed by the configuration. (Mainly standby-effects) but if for some reason standby effects is necessary, it follows the following pattern respectively:

  > Particle name, Particle hex color, Offset x, Offset y, Offset z, Radius, Effect type, Amount of particles.

* **item** - This group has a set of fields responsible for naming the name, lore and material type of the key. It is also possible to use two types of placeholders: {rarity} and {crate}.
