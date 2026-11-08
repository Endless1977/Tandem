# Tandem

A two-player online co-op shooter in pixel-art 3D. One player is the **pilot**, the other is the **gunner**, and you share one ship through 70 levels across seven themed worlds.

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
| Pilot | Space (or left click when online) | Prow lasers (forward only) |
| Pilot | Right click (online) | Barrier field |
| Gunner | Mouse | Aim the 360° turret |
| Gunner | Left click | Rapid-fire laser turret |
| Gunner | Right click | Heavy weapon (Seekers, Rail Lance, EMP) |
| Gunner | 1–3, wheel | Switch heavy weapon |
| Gunner | G / middle click | Launch or recall the dome |
| Both | F / Shift | Barrier field |
| Both | X | Detonate the Omega charge (if bought) |
| Both | C | Cycle your own camera |
| Both | + / − (or Ctrl + wheel) | Zoom your camera in or out |
| Both | M | Music on/off |

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

## Bonus jellyfish and gunner guns

Golden jellyfish drift through now and then. Shoot one and it drops a bonus block for the pilot to fly into:

- **Gunner gun blocks** cycle through colours and letters: **S** Spread, **W** Wave, **D** Side, **F** Forward, **H** Hail (shotgun bursts every 2–3 s). The gunner keeps that gun into the next levels until a different block is taken. Three of the same block in a row upgrades it to Mk II, three more to Mk III. These guns only come from blocks; the shop upgrades the standard turret (dome size, bolt thickness, twin barrels, side guns).
- **General blocks**: C credits, + repair, S shields, O Omega charge.

**Detachable dome**: the gunner can launch the turret dome on an indestructible platform (G or middle click). It flies to the mouse cursor and keeps shooting, and it rams anything it touches: two passes kill an ordinary creature. It stays out 10 seconds, then flies home and recharges. **Dome Link** in the drydock adds 10 seconds per purchase (up to 60 s) and costs at least half of your credits. The dome rides a small armoured copy of your ship. If the ship is destroyed, the dome goes with it.

Weapon modules click onto the hull and onto each other, with no frame: Side Beam cannons against the hull, then the square AA boxes, then the Seeker Pods, then the wing emitters, with the round EMP cylinder on the left end. Shield emitters are small studs on the back. The **Tesla Coil** (Pilot, 4 levels) sits on the tail and, while the prow fires, zaps the nearest enemy within a short range; each level adds range and damage, and the lightning chains to up to 4 enemies. The ship gets wider with each module, but only the hull itself can be hit.

**Sonic Shield** (Defense, 3 levels) passively bounces 50%, 65% or 80% of enemy shots off the hull; the bounced shots turn cyan and hurt enemies. **Side Beams** (Auto, 5 levels) are two wing cannons that fire thin laser beams forward every few seconds; each level makes them thicker, stronger and more frequent.

The walls also hold seaweed, geysers that erupt every few seconds, and grabbing kelp that reaches for the ship, holds it and drains it until you shoot it.

The drydock shows your ship turning in the hangar with everything you have bolted on, and every upgrade card has its own icon.

## Arcade bonuses

- Every kill shows its points. Kills in quick succession build a combo; every 5 in a row raises the score multiplier (up to ×4).
- Destroy a whole formation before any of it escapes: **Wave wiped**, bonus credits.
- Finish a level without taking a hit: **No damage**, +300 credits.
- Every 10,000 points is announced; every 50,000 earns an extra ship.

## Music

Commodore 64 style chiptune, generated in the browser. Each sector has its own song, the minor bosses, big bosses and the Null Sovereign (both forms) have their own themes, and the music adds drums, snare, lead and faster hi-hats as the screen gets busier.

## Worlds

Every world has its own theme, with its own ground, wall shape, decorations, obstacles, creatures, music and boss:

| World | Theme | You meet | Boss |
|---|---|---|---|
| I | Coral Deep (water) | squid, jellyfish, urchins, eels, mantas | Tide Warden, a giant crab |
| II | Valley of Ra (Egypt) | scarabs, eyes of Horus, sun disks, Bastet cats, falcons, cobras; pyramids, obelisks, ankhs | Sphinx of Ra with two Bastet cats |
| III | Bleached Dunes (desert) | vultures, tumbleweeds, tortoises, rattlesnakes, sandworms; cacti, horse skeletons, wells | Dune Scorpion |
| IV | Magma Rift (lava) | fire bats, flame wisps, phoenixes, crystal eyes; volcanoes, stalagmites, stalactites, crystals | Magma Colossus with crystal pods |
| V | Emerald Canopy (jungle) | dragonflies, dart frogs, long-tailed monkeys, chameleons, anacondas; lianas, poison flowers | Corpse Bloom, a giant carnivorous flower |
| VI | Silicon Grid (digital) | cursors, floppies, CPU fans, virus bugs, a snake from the snake game; RAM, CPUs, RGB strips | Mainframe Argus with cooling fans |
| VII | Sovereign's Throne | all worlds torn together | Null Sovereign, pharaoh mask and Ascendant form |

## Difficulty

Pick **Normal**, **Hard** or **Extreme** next to the start level. On Hard and Extreme the further you get, the more often enemies dodge your shots (a blue MISS) and the harder their weapons hit. Your own ship stays the same.

## Structure

- Seven worlds of ten levels each (70 levels). A mini-boss waits at level 5 of every world, the world's end boss at level 10; only after beating the end boss does the next theme begin.
- End bosses have far more stamina than before; the big ones still need their shield pods destroyed first.
- The road winds: it curves across the screen and rises and falls like a roller coaster, and the camera follows and tilts with it. The game logic stays straight, so hitboxes are unaffected.
- Boss fights flatten the road and swing the default camera behind the ship: boss at the top of the screen, ship at the bottom. In that view W/S move forward/back. Every other camera view still works.
- Level 70 is the Null Sovereign: two lives, a frozen transformation, then a faster and harder second form.
- After every boss there is a drydock where both players spend shared credits. On game over you retry from the last drydock, keeping upgrades and credits.

Solo practice and the host lobby can start at any boss level (with starting credits).

## About the art

All ships and enemies are pixel sprites drawn in code and extruded into voxels. The game renders at 960×400; every sprite is doubled with edge smoothing (Scale2x) and lit per voxel from the upper left, and the player ship is drawn at double pixel density with its own height map. GLB models are not needed. If you want your own ship designs, they can be converted into the same voxel style.
