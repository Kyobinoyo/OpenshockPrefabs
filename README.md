# Openshock Prefabs
Here you'll find some prefabs I created in Unity for [VRChat](https://store.steampowered.com/app/438100/VRChat/) and [ChilloutVR](https://store.steampowered.com/app/661130/ChilloutVR/) to utilize the [Openshock](https://github.com/OpenShock) project in either of those games.

All of the [VRChat](https://store.steampowered.com/app/438100/VRChat/) prefabs use [VRCFury](https://vrcfury.com/).

To use [ShockOSC](https://github.com/OpenShock/ShockOsc) in ChilloutVR you'll need a OSC mod. One of the most popular ones are [OSC by kafeijao](https://github.com/kafeijao/Kafe_CVR_Mods?tab=readme-ov-file).

When multiple Prefabs are used together it should combine into one single sub menu.
  
  
  
## List of Prefabs
| Name              |Parameters| Description   |
| -------------     | :-------------: |---------------|
| [Shocker](https://github.com/Kyobinoyo/OpenshockPrefabs/releases/tag/Shocker)                         |3| A Shocker model inclusive trigger prefab to make it possible to shock you in VR by touching the Shocker using [ShockOSC](https://github.com/OpenShock/ShockOsc)|
| [Remote-Trigger](https://github.com/Kyobinoyo/OpenshockPrefabs/releases/tag/RemoteTrigger)            |1| A combination of prefabs to make it possible to shock you over distance like using a remote utilizing contacts and [ShockOSC](https://github.com/OpenShock/ShockOsc)|
|[Settings Menu](https://github.com/Kyobinoyo/OpenshockPrefabs/releases/tag/SettingsMenu)               |0 |A Menu for editing [ShockOSC](https://github.com/OpenShock/ShockOsc) settings from within the game. __**Needs ShockOsc v2.0 or newer**__|

## Tips
### Move the Menu into another Sub menu:
By default the ShockOsc Submenu get's created in the main menu page, if you need to move the ShockOsc submenu, just click on your avatars main object, then add the "VRCFury | Move Menu Item" component to it and configure it like this:  
![MoveMenu](Images/MoveMenu.png)  
After that it should be where you want it to be.  

## FAQ
### Q: VRCFury is throwing some error.
A: Make sure you have enough parameter memory slots free for the prefab you want to use.  
if this doesn't help contact me on the [Openshock Discord](https://discord.gg/OpenShock).  

### Q: Why is ShockOsc not reacting to my Shocker being touched?
A: First make sure [OSC](https://docs.vrchat.com/docs/osc-overview#how-do-i-use-it) is active, if that's not the problem, then is being funny VRChat when updating an Avatar, most of the time it does not update the parameters for OSC, to fix that go to  
```
C:\Users\%USERPROFILE%\AppData\LocalLow\VRChat\VRChat\OSC
```  
and delete the files there, it'll not damage your game after you change back in to your avatar it should generate new files with your parameters updated.  

### Q: Why is my friend getting shocked every time my Avatar is loaded in?
A: Make sure the **Sender** object is disabled while uploading the Avatar, otherwise the Sender object is active when you load in and get's disabled when the parameter sync kicks in, resulting in a shock.  

### Q: Why can't I shock myself? I have the Sender and Receiver on my avatar!
A: In the *Receiver* script enable **Allow Self**