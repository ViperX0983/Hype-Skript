# Hype-Skript

first you want to install all the sk addons that I gave here and after that make a skript and paste this, enjoy!:

on rightclick:
	if player's tool is iron sword named "&6Hyperion" with lore " &7Damage: &c+260 || &7Streangth: &c+150 || || &7Intelligence: &a+350 || &7Ferocity: &a+30 || &7Deals +&a50 &7damage to || &Withers. Grants &c+1 Damage || &7and &a+2 &bIntelligence || &7per &cCatacombs &7level. || &7Your Catacombs level: &c0 || &6&lLEGENDARY":
		set {_spawnLock} to location of player
		if block 8 in front of player is not a air:
			cancel event
			play "ENDERMAN_TELEPORT" to player at volume 1
			damage all entities in radius 3 of player by 100
			drawSphere style 1, particle "explosion", center player, id "%player%.sphere", rainbowMode true, radius 2.5, density 500, visibleRange 100, pulseDelay 1
			wait 0.2 seconds
			stopEffect id "%player%.sphere"
			
		else:
			set {_Block} to block 8 in front of player
			play "ENDERMAN_TELEPORT" to player at volume 1
			teleport player above {_Block}
			damage all entities in radius 3 of player by 100
			drawSphere style 1, particle "explosion", center player, id "%player%.sphere", rainbowMode true, radius 2.5, density 500, visibleRange 100, pulseDelay 1
			wait 0.2 seconds
			stopEffect id "%player%.sphere"
command /hype:
	trigger:
		give iron sword named "&6Hyperion" with lore " &7Damage: &c+260 || &7Streangth: &c+150 || || &7Intelligence: &a+350 || &7Ferocity: &a+30 || &7Deals +&a50 &7damage to || &Withers. Grants &c+1 Damage || &7and &a+2 &bIntelligence || &7per &cCatacombs &7level. || &7Your Catacombs level: &c0 || &6&lLEGENDARY" to player
