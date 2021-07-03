---
id: jetpack-json
title: Jetpack JSON
sidebar_label: Jetpack JSON
---

## Adding a jetpack
Jetpacks are added via JSON files placed in `/config/ironjetpacks/jetpacks/`. Each file represents a new jetpack to be added.

## Editing a jetpack
After initial load all of the default jetpack JSON files will be generated. You can then edit the values as you see fit.

## The jetpack file
This section will go over the values available to use in jetpack file. Syntax can be inferred from the example json below.

**Tip:** Use the stats of the default jetpacks to decide what the values should be for your custom jetpacks, since the values themselves are quite cryptic.

**Note:** Any field below marked with a '*' is required.

### Name*
The name of the jetpack. This name must be all lower case and have underscores for spaces. This will be used for registry names as well as localized names. The name will be formatted automatically for localized names.
```json
{
  "name": "emerald"
}
```

### Disable*
Should this jetpack be disabled?
```json
{
  "disable": false
}
```

### Tier*
The crafting tier of the jetpack. Make sure there is at least 1 jetpack per tier, in succession (ex 1, 2, 3 all have at least one jetpack). Tier -1 is creative.
```json
{
  "tier": 5
}
```

### Color*
The color of the jetpack and related items as an integer. This color should be a HEX value.
```json
{
  "color": "41f384"
}
```

### Armor points*
The amount of armor the jetpack should give when worn.
```json
{
  "armorPoints": 4
}
```

### Enchantability*
How enchantable the armor should be.
```json
{
  "enchantability": 15
}
```

### Crafting material*
The material used to craft the jetpack and its components. Syntax is `modid:itemid` for items and `tag:modid:tagid` for tag entries.
```json
{
  "craftingMaterial": "tag:forge:gems/emerald"
}
```

### Creative
Is the jetpack a creative tier jetpack?
```json
{
  "creative": false
}
```
Omitting this field will default to `false`.

### Rarity
The item rarity of this jetpack. This is basically just used to change the color of the tooltip. Valid values are 0-3.
```json
{
  "rarity": 0
}
```
Omitting this field will default to `0`.

### Toughness (4.2.1+)
The amount of armor toughness this jetpack should give when worn.
```json
{
  "toughness": 0
}
```

### Knockback Resistance (4.2.1+)
The amount of knockback resistance this jetpack should give when worn.
```json
{
  "knockbackResistance": 0
}
```

### Capacity*
How much FE this jetpack can hold.
```json
{
  "capacity": 48000000
}
```

### Usage*
How much FE this jetpack should use when flying/hovering.
```json
{
  "usage": 880
}
```

### Vertical speed*
How fast the jetpack should fly upwards.
```json
{
  "speedVertical": 1.03
}
```

### Vertical acceleration*
How fast the initial takeoff is.
```json
{
  "accelVertical": 0.17
}
```

### Sideways speed*
How fast the jetpack should make you move forwards (when holding forwards).
```json
{
  "speedSideways": 0.21
}
```

### Descending hover speed*
How fast the jetpack should descend when hover mode is on and you're sneaking.
```json
{
  "speedHoverDescend": 0.45
}
```

### Hover speed*
How fast the jetpack should descend when hovering.
```json
{
  "speedHover": 0.0
}
```

### Sprint speed multiplier*
How much faster the player should fly when sprinting while flying forwards.
```json
{
  "sprintSpeedMulti": 2.0
}
```

### Sprint speed vertical multiplier (v4.2.0+)
How much faster the player should fly when sprinting while flying upwards.
```json
{
  "sprintSpeedMultiVertical": 2.0
}
```
Omitting this field will default to `1.0`

### Sprint fuel multiplier*
How much more fuel should the jetpack use while sprinting.
```json
{
  "sprintFuelMulti": 4.0
}
```

## Exmaple file
```json
{
  "name": "emerald",
  "disable": false,
  "tier": 5,
  "color": "41f384",
  "armorPoints": 4,
  "enchantability": 15,
  "craftingMaterial": "tag:forge:gems/emerald",
  "rarity": 0,
  "toughness": 0,
  "knockbackResistance": 0,
  "capacity": 48000000,
  "usage": 880,
  "speedVertical": 1.03,
  "accelVertical": 0.17,
  "speedSideways": 0.21,
  "speedHoverDescend": 0.45,
  "speedHover": 0.0,
  "sprintSpeedMulti": 2.0,
  "sprintSpeedMultiVertical": 1.0,
  "sprintFuelMulti": 4.0
}
```
