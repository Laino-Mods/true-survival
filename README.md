True Survival
=============

Turns Conan Exiles into a hardcore survival game.

Most sources of easily accessible instantanious healing are removed,
debuffs last longer and should be removed with an appropriate item.

Players have a chance of receiving a bleeding debuff upon being hit and of
getting a fracture upon taking fall damage.

Players will heal naturally over time, at the cost of depleting their hunger and thirst gauges
more quickly. This effect is greatly accelerated while sheltered and reduced while bleeding.

Changes to the Base Game
------------------------

Legend: * means modified, + means added, and - means removed

#### Players
- +Natural Healing: Player heal naturally over time, reduced when bleeding, increased when sheltered.

#### Perks
- \*Fierce Vitality: grants *increased* passive health regeneration.

#### Buffs/Debuffs
- \*Bleeding: lasts 5 minutes, causes 1 damage / 3 seconds, max 20 stacks
- \*Gouged: lasts 5 minutes, causes 1 damage / 3 seconds, max 10 stacks
- \*Sated: no longer provides any healing, natural regeneration uses no food/drink
- +Internal Bleeding: lasts 5 minutes, causes 1 damage / 3 seconds, max 10 stacks
- +Fracture: reduces movement speed by 35%, can cause internal bleeding, max 2 stacks
- +Improvised Splint: lasts 10 minutes, reduces movement speed by 10%, max 2 stacks
- +Hemostasis: prevents damage from bleeding and internal bleeding

#### Items
- \*Rough Wraps: don't heal but remove 5 stacks of bleeding
- \*Healing Wraps: don't heal but remove 10 stacks of bleeding
- \*Numbing Wraps: don't heal but remove 15 stacks of bleeding (planned: provide buff)
- \*Stutter Wraps: don't heal but remove 20 stacks of bleeding (planned: provide buff)
- \*Infused Wraps: don't heal but remove 20 stacks of bleeding (planned: provide buff)
- \*Weak Aloe Extract: doesn't heal but gives hemostasis (2 minutes)
- \*Aloe Extract: doesn't heal but gives hemostasis (5 minutes)
- \*Concentrated Aloe Extract: doesn't heal but gives hemostasis (10 minutes)
- \*Pure Aloe Extract: doesn't heal but gives hemostasis (20 minutes)
- \*Infused Aloe Extract: doesn't heal but gives hemostasis (30 minutes)
- +Improvised Splint: removes a fracture but causes improvised splint
- +Splint: removes a fracture or improvised splint
- +Potion of Bleeding: causes bleeding (for testing purposes)

#### Misc (oddities)
- \*Activated Trap: lasts 5 minutes, causes 2 damage / 3 seconds, max 10 stacks
- \*Bone Shrapnel: lasts 5 minutes, causes 2 damage / 3 seconds, max 10 stacks
- \*Bleeding (non stacking): lasts 5 minutes, causes 3 damage / 3 seconds
- \*Gouged (never ends): causes 1 damage / 3 seconds, max 10 stacks

#### Fixes
- BP_AC_Buff_GenericPoison: displayed incorrect damage numbers for poisons

For Modders
-----------

Uses Item IDs: 888999001 - 889000000

Disables Vitality_30 perk and replaces it with a custom one.

Overrides the following vanilla files:

```
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_Bleeding_CantCleanse.uasset
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_Bleeding_NeverEnds.uasset
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_Bleeding_NonStackingProc.uasset
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_Bleeding_ShrapnelGrenade.uasset
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_Bleeding_SpikedTrap.uasset
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_Bleeding_WeaponProc.uasset
Content/Systems/Buffs/Damage_OverTime/BP_AC_Buff_GenericPoison.uasset
Content/Systems/Buffs/HealthRegen/BP_AC_Buff_SatedBonusHealthRegen.uasset
Content/Systems/Buffs/Heal_OverTime/BP_AC_Buff_Healing_From_Food.uasset
```