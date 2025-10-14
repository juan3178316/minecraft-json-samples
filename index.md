---
title: "Testing website with Markdown"
description: "description for my website"
author: juan3178316
ms.author: juan3178
ms.date: 10/14/25
ms.topic: article
---

search new web: [`file_md.md`](file_md.md)

|Title 1 |Title 2| Title 3|
|--------|-------|--------|
|This will |Show a three |column table|

## Hi everyone
```json
{
    "testing": 123,
    "yi": "autumn" // testing comment
}
```
```typescript
import { system, world, EntityComponentTypes, GameMode, ItemStack } from "@minecraft/server";
import { templateBannedId_0x0001 as tBId_0 } from "../lib/ac/register.js";

system.runInterval(() => world.getAllPlayers().forEach(player => {
	if(!player.getDynamicProperty("ac:s_ft")) 0;
	else {
		let slotIndex = player?.getComponent(EntityComponentTypes.Inventory);

		if(player?.getGameMode() == GameMode.Creative) return;
		for(let SlotV = 0; SlotV < 36; SlotV++) getItemSlot(SlotV);
		function getItemSlot(slotV) {
			let gItem = slotIndex.container.getItem(slotV);
			if(typeof gItem == "undefined") return;
			if(tBId_0.includes(gItem.typeId)) {
				if(gItem.getLore()[0] == "ac:found_item") return;
				slotIndex.container.getSlot(slotV).setLore(["ac:found_item"]);
				player.playSound("ac.sound.sfx.notify_1");
				world.sendMessage({translate:"ac_text.success.detect_template",with:["\n",player.name,"\uE110"]});
			};
		}
	}
}), 0x64);
```
