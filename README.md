![SteamMultiplayer](https://cdn.discordapp.com/attachments/943100967199571988/959473877266886706/unknown.png)
# UE4-Steam-Multiplayer-Plugin
Unreal Engine 4 Steam Advanced Session Plugins

> Tutorial
- Add C++ Class to Your Project
- Restart Engine
- Extract All Plugins
- Copy AdvancedSession and AdvancedSteamSession to Your Project Plugin Folder
- Restart Engine
- After Rebuild Plugin Check if Enabled
- Create New Game Instance
- Add Game Instance to Your Project Settings Default Game Instance
- Create Custom Events and Add Nodes ( Create Advanced Session , Find Advanced Session , Join Session , Destroy Session )
- Connect Custom Events To Your Widget
- Go to Your Project File Location and Find DefaultEngine.ini
- Add This Codes to It
```
[/Script/Engine.GameEngine]
+NetDriverDefinitions=(DefName="GameNetDriver",DriverClassName="OnlineSubsystemSteam.SteamNetDriver",DriverClassNameFallback="OnlineSubsystemUtils.IpNetDriver")

[OnlineSubsystem]
DefaultPlatformService=Steam

[OnlineSubsystemSteam]
bEnabled=true
SteamDevAppId=480

[/Script/OnlineSubsystemSteam.SteamNetDriver]
NetConnectionClassName="OnlineSubsystemSteam.SteamNetConnection"

```
- Save and Close DefaultEngine.ini
- Restart Engine
- Rebuild and Package Game
- Open Steam
- [Download Spacewar on Steam](steam://install/480)
- Enjoy Multiplayer
