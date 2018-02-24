# vRP_itemdrop
The module for vRP, which when throwing an object on the ground creates a package on the ground, in which the discarded objects will be stored.

# Install
Unpack the module in the folder vRP_itemdrops, connect to the server.сfg through the `start vRP_itemdrops`.
Also add to the vrp/modules/inventory.lua

line 87
uner vRPclient.notify(player,{lang.inventory.trash.done({vRP.getItemName(idname),amount})})
```lua
TriggerClientEvent("DropSystem:drop", player, idname, amount) 
```

line 94
under vRPclient.playAnim(player,{true,{{"pickup_object","pickup_low",1}},false})
```lua
TriggerClientEvent("DropSystem:drop", player, idname, amount) 
```
