# Automated Building Upgrade (CK3)

A quality-of-life mod that adds **Decisions** entries to upgrade buildings in your personal domain in one click.

## Requirements

- Crusader Kings III **1.19.x**
- No DLC required

## Installation

1. Copy `automated_building_upgrade.mod` to your CK3 mod folder:
   - **Windows:** `Documents\Paradox Interactive\Crusader Kings III\mod\`
   - **Linux:** `~/.local/share/Paradox Interactive/Crusader Kings III/mod/`
2. Copy the `automated_building_upgrade` folder to:
   - **Windows:** `Documents\Paradox Interactive\Crusader Kings III\mod\automated_building_upgrade\`
   - **Linux:** `~/.local/share/Paradox Interactive/Crusader Kings III/mod/automated_building_upgrade/`
3. Enable the mod in the CK3 launcher.

## Decisions

All upgrade decisions are **always visible** in the Decisions menu while you are a landed player. They appear greyed out when nothing can be upgraded or you lack gold.

| Decision | What it upgrades |
|----------|------------------|
| **Upgrade All Domain Buildings** | Main holdings + all slot buildings |
| **Upgrade Main Holdings** | Castles, cities, temples, tribal holdings only |
| **Upgrade Economic Buildings** | Farms, mills, tradeports, and other economic slots |
| **Upgrade Military Buildings** | Fortifications and recruitment buildings |
| **Upgrade Capital County Only** | All building types in your capital county only |
| **Upgrade Current Duchy** | All building types in holdings where you stand |
| **Fill Empty Slots Only** | Construct tier-01 slot buildings; no upgrades |
| **Upgrade One Tier** | Raise each eligible building by one tier |
| **Upgrade to Tier Cap** | Raise buildings up to your configured tier cap |
| **Set Tier Cap** | Configure the max tier for tier-cap upgrades (default 4) |
| **Set Gold Reserve** | Set minimum gold to keep when upgrading |
| **Toggle Passive Auto-Upgrade** | Auto-upgrade on new building innovations (see below) |
| **Toggle Detailed Upgrade Reports** | Show per-building detail in completion messages |
| **Include Duchy Capital Buildings** | Opt in to upgrading existing duchy capital buildings |

Each use constructs new buildings in empty slots when affordable, then raises buildings to the **highest tier your innovations and main holding level allow**, spending gold until no further upgrades are possible. In each province, main holdings are maxed before slot buildings beneath them. Your capital county is processed first.

### Duchy capital buildings

By default, duchy capital buildings are **excluded**. Use **Include Duchy Capital Buildings** to opt in. When enabled:

- Upgrades **existing** duchy buildings only (no auto-construction or building choice)
- Requires you to hold the relevant **duchy title** and own the province directly
- Follows the same mode filters (All / Economic / Military), depth, tier cap, and gold reserve as other upgrades
- Included in passive auto-upgrade when enabled

### Passive auto-upgrade

Enable **Toggle Passive Auto-Upgrade** for hands-off building management after research. When your culture unlocks a new building innovation, the mod automatically runs **Upgrade All Domain Buildings** if you have gold above your reserve — no confirmation popup, no decision click.

- Checks run on **quarterly** and **yearly** pulses (within a few months of an innovation unlocking)
- Also triggers when your culture **advances to a new era**
- Respects your **gold reserve** setting
- Still sends the normal completion report when upgrades happen

### Scope

- **Included:** Buildings in your **direct holdings** only
- **Excluded by default:** Vassal holdings, duchy capital buildings, special buildings, nomadic yurts
- **Opt-in:** Duchy capital buildings via **Include Duchy Capital Buildings**
- Provinces with ongoing construction are skipped

## Version

**1.5.0** — Add opt-in duchy capital building upgrades

**1.4.0** — Add optional passive auto-upgrade on building innovation unlock

**1.3.0** — Add capital county, current duchy, fill empty slots, one tier, and tier cap decision modes
