# FiveM Infinite-Ammo [Standalone]
A simple Infinite Ammo Script for all who need it. [Standalone]

#            ---Installation---
1. Download the .zip
2. Put the InfiniteAmmo-matser in your Resource folder
3. Rename InfiniteAmmo-master to InfiniteAmmo
4. Add enure InfiniteAmmo to your server.cfg
5. Start your Server

# Command Guide
- Enable InfiniteAmmo for the whole server: /infiniteOn
- Disable InfiniteAmmo for the whole server: /infiniteOff

- Enable InfiniteAmmo for a specific WeaponHash: /infiniteOnFor [WeaponName]
- Disable InfiniteAmmo for a specific WeaponHash: /infiniteOffFor [WeaponName]
- Weaponnames can be found here: https://www.vespura.com/fivem/weapons/stats/
- Example for usage: "/infiniteOnFor weapon_appistol"

# Use without command

add this to client.lua

````lua
Citizen.CreateThread(function()
    while true do
        Citizen.Wait(1000)
        for i = 1, #weaponStealeableList do
            SetPedInfiniteAmmo(GetPlayerPed(-1), true, tonumber(weaponStealeableList[i]))
        end
    end
end)
````

#
For any questions
Discord: vincent189

