# Tandem

A two-player online co-op shooter in pixel-art 3D. One player is the **pilot**, the other is the **gunner**, and you share one ship through 35 levels across seven sectors.

Play it on GitHub Pages: put `index.html` in a repo, enable Pages (Settings → Pages → deploy from `main`), and open the page link.

## Playing online

1. The host clicks **Host online game**, picks a seat (pilot or gunner) and clicks **Open room**.
2. The host shares the five-letter code, or the invite link (`…/?join=CODE`).
3. The other player clicks **Join with a code** (or opens the link) and joins.
4. The host clicks **Launch**.

The two browsers connect directly (PeerJS / WebRTC). The host's browser runs the game, so the host should keep the tab open and in front. Hosting as the pilot gives the smoothest flying; a guest pilot also flies with no input lag, because the guest's ship movement is predicted locally.

If a partner drops out, the host can continue solo with both seats.

## Controls

| Seat | Control | Action |
|---|---|---|
| Pilot | WASD / arrows | Fly |
| Pilot | Space | Prow lasers (forward only) |
| Gunner | Mouse | Aim the 360° turret |
| Gunner | Left click | Rapid-fire laser turret |
| Gunner | Right click | Heavy weapon (Seekers, Rail Lance, EMP) |
| Gunner | 1–3, Q/E, wheel | Switch heavy weapon |
| Gunner | F / Shift | Barrier field |
| Both | X | Detonate the Omega charge (if bought) |
| Both | C | Cycle your own camera |
| Both | + / − (or Ctrl + wheel) | Zoom your camera in or out |

### Cameras

Each player picks a view independently: **Anamorphic** (default, the classic 2.4:1 top view), **Chase** (behind the ship), **Hull top**, **Cockpit**, and **Gunner seat** (looks along the turret; click to lock the mouse, then move it to turn). In every view except Anamorphic, W/S move forward/back and A/D move sideways.

## Weapons and upgrades

Every upgrade bolts a visible part onto the ship, so it grows as you buy more. The hitbox stays the small hull.

- **Prow Lasers Mk II–V** (pilot): thicker beams, heavier hits; Mk V pierces.
- **Wing Emitters** (pilot): extra side and angled lasers.
- **Turret Core**, **Seeker Pods**, **Rail Lance**, **EMP Burst** (gunner).
- **Nova Orbs** (automatic): slow orbs that destroy any creature or shot they touch. Sides first, then front and back, up to 12 firing points.
- **AA Battery** (automatic): homing missiles that launch on their own.
- **Omega Charge**: everything on screen explodes. One use, then buy it again.
- Barrier, Deflectors, Hull Plating, Wing Drones, Field Repair, Spare Hull.

Credits come from kills, so the more you destroy the more you can buy. Every cleared level also pays a fixed bonus, so you never get stuck.

## Structure

- The enemies are sea creatures: squid, jellyfish, urchins, eels, pufferfish, mantas, anglers, nautiluses and corals. They fly circles, hexagons, squares, figure-eights and zigzags through the screen before leaving.
- Levels run through a winding corridor with walls, tentacles, antennas and pillars that block the ship and stop shots. Corals on the walls fire slow, light spores.
- Levels 5, 15 and 25 end with a minor boss; levels 10, 20 and 30 with a big boss that has shield pods to destroy first.
- Level 35 is the Null Sovereign: two lives. When the first is gone, time freezes while it transforms, and its second form attacks faster and harder.
- After every fifth level there is a drydock where both players spend shared credits on upgrades. Both players press Ready to continue.
- On game over you retry from the start of the current five-level block, keeping upgrades and credits.

Solo practice and the host lobby can start at any boss level (with starting credits) to try the bosses.

## About the art

All ships and enemies are pixel sprites drawn in code and extruded into voxels. GLB models are not needed. If you want your own ship designs, they can be converted into the same voxel style.
