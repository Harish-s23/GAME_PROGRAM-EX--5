# GAME_PROGRAM-EX--5

Making Player to collect the ammo and increase the bullet spawn count.

## Aim

To implement a gameplay feature where the player collects ammo pickups in the game world. Upon collecting ammo, the player's ammo count increases, enabling more bullet spawns (shots).

## Procedure

Setup Player Character

Open your PlayerCharacter Blueprint.s
Add a new Integer variable named AmmoCount.
Set an initial default value (e.g., AmmoCount = 10).
Ensure you have a shooting mechanism in place that uses AmmoCount to determine if a bullet can be fired.
Create Ammo Pickup Blueprint

Go to the Content Browser → Right-click → Blueprint Class → Select Actor → Name it BP_AmmoPickup.
Add components: * Static Mesh: Representing the ammo (e.g., a bullet or crate). * Sphere Collision: To detect overlap with the player.
In the Event Graph of BP_AmmoPickup:
Use OnComponentBeginOverlap on the Sphere Collision.
Cast to PlayerCharacter.
Increase the player’s AmmoCount (e.g., AmmoCount += 5).
Optionally, play a pickup sound or effect.
Destroy the ammo pickup actor.
Update Shooting Logic (Optional)
In your player’s shooting logic:
Before spawning a bullet, check if AmmoCount > 0.
If true:
Spawn bullet.
Decrease AmmoCount by 1.
Place Ammo in the World
Drag instances of BP_AmmoPickup into your level from the Content Browser.

## OUTPUT:
<img width="1043" height="462" alt="Screenshot 2026-10-05 203000" src="https://github.com/user-attachments/assets/fa8ad84d-7ac0-43df-93dc-6fa8dfebb844" />
<img width="1041" height="650" alt="Screenshot 2026-10-05 203015" src="https://github.com/user-attachments/assets/3eeaf76b-c9da-40b3-9bbe-038dc7565b90" />

<img width="1040" height="546" alt="Screenshot 2026-10-05 203027" src="https://github.com/user-attachments/assets/5b54443c-6e55-4cbb-af31-6e22209f9bc0" />

<img width="1038" height="687" alt="Screenshot 2026-10-05 203040" src="https://github.com/user-attachments/assets/1d0df3d1-45cc-4c3a-9c21-16b0f1d27e86" />



## RESULT:

The player starts with a limited number of bullets.

When the player overlaps with an ammo pickup:

The ammo is collected.

The player's AmmoCount increases.

The player can now fire additional bullets based on the updated ammo count.


