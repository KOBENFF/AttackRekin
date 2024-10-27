if game:IsLoaded() then
	pcall(function()
		repeat wait()
			game:GetService("ReplicatedStorage").Effect.Container.Respawn:Destroy()
			game:GetService("ReplicatedStorage").Effect.Container.Death:Destroy()
		until not game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Death") or not game:GetService("ReplicatedStorage").Effect.Container:FindFirstChild("Respawn")
	end)
end
local placeId = game.PlaceId
if placeId == 2753915549 then
	First_Sea = true
elseif placeId == 4442272183 then
	Second_Sea = true
elseif placeId == 7449423635 then
	Third_Sea = true
end
local placeId = game.PlaceId
if placeId == 2753915549 then
	World1 = true
elseif placeId == 4442272183 then
	World2 = true
elseif placeId == 7449423635 then
	World3 = true
end
local function CheckQuest()
	local Lv = game:GetService("Players").LocalPlayer.Data.Level.Value
	if First_Sea then
		if Lv == 1 or Lv <= 9 or SelectMonster == "Bandit" or SelectArea == '' then -- Bandit
			Ms = "Bandit"
			NameQuest = "BanditQuest1"
			QuestLv = 1
			NameMon = "Bandit"
			CFrameQ = CFrame.new(1060.9383544922, 16.455066680908, 1547.7841796875)
			CFrameMon = CFrame.new(1038.5533447266, 41.296249389648, 1576.5098876953)
		elseif Lv == 10 or Lv <= 14 or SelectMonster == "Monkey" or SelectArea == 'Jungle' then -- Monkey
			Ms = "Monkey"
			NameQuest = "JungleQuest"
			QuestLv = 1
			NameMon = "Monkey"
			CFrameQ = CFrame.new(-1601.6553955078, 36.85213470459, 153.38809204102)
			CFrameMon = CFrame.new(-1448.1446533203, 50.851993560791, 63.60718536377)
		elseif Lv == 15 or Lv <= 29 or SelectMonster == "Gorilla" or SelectArea == 'Jungle' then -- Gorilla
			Ms = "Gorilla"
			NameQuest = "JungleQuest"
			QuestLv = 2
			NameMon = "Gorilla"
			CFrameQ = CFrame.new(-1601.6553955078, 36.85213470459, 153.38809204102)
			CFrameMon = CFrame.new(-1142.6488037109, 40.462348937988, -515.39227294922)
		elseif Lv == 30 or Lv <= 39 or SelectMonster == "Pirate" or SelectArea == 'Buggy' then -- Pirate
			Ms = "Pirate"
			NameQuest = "BuggyQuest1"
			QuestLv = 1
			NameMon = "Pirate"
			CFrameQ = CFrame.new(-1140.1761474609, 4.752049446106, 3827.4057617188)
			CFrameMon = CFrame.new(-1201.0881347656, 40.628940582275, 3857.5966796875)
		elseif Lv == 40 or Lv <= 59 or SelectMonster == "Brute" or SelectArea == 'Buggy' then -- Brute
			Ms = "Brute"
			NameQuest = "BuggyQuest1"
			QuestLv = 2
			NameMon = "Brute"
			CFrameQ = CFrame.new(-1140.1761474609, 4.752049446106, 3827.4057617188)
			CFrameMon = CFrame.new(-1387.5324707031, 24.592035293579, 4100.9575195313)
		elseif Lv == 60 or Lv <= 74 or SelectMonster == "Desert Bandit" or SelectArea == 'Desert' then -- Desert Bandit
			Ms = "Desert Bandit"
			NameQuest = "DesertQuest"
			QuestLv = 1
			NameMon = "Desert Bandit"
			CFrameQ = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
			CFrameMon = CFrame.new(984.99896240234, 16.109552383423, 4417.91015625)
		elseif Lv == 75 or Lv <= 89 or SelectMonster == "Desert Officer" or SelectArea == 'Desert' then -- Desert Officer
			Ms = "Desert Officer"
			NameQuest = "DesertQuest"
			QuestLv = 2
			NameMon = "Desert Officer"
			CFrameQ = CFrame.new(896.51721191406, 6.4384617805481, 4390.1494140625)
			CFrameMon = CFrame.new(1547.1510009766, 14.452038764954, 4381.8002929688)
		elseif Lv == 90 or Lv <= 99 or SelectMonster == "Snow Bandit" or SelectArea == 'Snow' then -- Snow Bandit
			Ms = "Snow Bandit"
			NameQuest = "SnowQuest"
			QuestLv = 1
			NameMon = "Snow Bandit"
			CFrameQ = CFrame.new(1386.8073730469, 87.272789001465, -1298.3576660156)
			CFrameMon = CFrame.new(1356.3028564453, 105.76865386963, -1328.2418212891)
		elseif Lv == 100 or Lv <= 119 or SelectMonster == "Snowman" or SelectArea == 'Snow' then -- Snowman
			Ms = "Snowman"
			NameQuest = "SnowQuest"
			QuestLv = 2
			NameMon = "Snowman"
			CFrameQ = CFrame.new(1386.8073730469, 87.272789001465, -1298.3576660156)
			CFrameMon = CFrame.new(1218.7956542969, 138.01184082031, -1488.0262451172)
		elseif Lv == 120 or Lv <= 149 or SelectMonster == "Chief Petty Officer" or SelectArea == 'Marine' then -- Chief Petty Officer
			Ms = "Chief Petty Officer"
			NameQuest = "MarineQuest2"
			QuestLv = 1
			NameMon = "Chief Petty Officer"
			CFrameQ = CFrame.new(-5035.49609375, 28.677835464478, 4324.1840820313)
			CFrameMon = CFrame.new(-4931.1552734375, 65.793113708496, 4121.8393554688)
		elseif Lv == 150 or Lv <= 174 or SelectMonster == "Sky Bandit" or SelectArea == 'Sky' then -- Sky Bandit
			Ms = "Sky Bandit"
			NameQuest = "SkyQuest"
			QuestLv = 1
			NameMon = "Sky Bandit"
			CFrameQ = CFrame.new(-4842.1372070313, 717.69543457031, -2623.0483398438)
			CFrameMon = CFrame.new(-4955.6411132813, 365.46365356445, -2908.1865234375)
		elseif Lv == 175 or Lv <= 189 or SelectMonster == "Dark Master" or SelectArea == 'Sky' then -- Dark Master
			Ms = "Dark Master"
			NameQuest = "SkyQuest"
			QuestLv = 2
			NameMon = "Dark Master"
			CFrameQ = CFrame.new(-4842.1372070313, 717.69543457031, -2623.0483398438)
			CFrameMon = CFrame.new(-5148.1650390625, 439.04571533203, -2332.9611816406)
		elseif Lv == 190 or Lv <= 209 or SelectMonster == "Prisoner" or SelectArea == 'Prison' then -- Prisoner
			Ms = "Prisoner"
			NameQuest = "PrisonerQuest"
			QuestLv = 1
			NameMon = "Prisoner"
			CFrameQ = CFrame.new(5310.60547, 0.350014925, 474.946594, 0.0175017118, 0, 0.999846935, 0, 1, 0, -0.999846935, 0, 0.0175017118)
			CFrameMon = CFrame.new(4937.31885, 0.332031399, 649.574524, 0.694649816, 0, -0.719348073, 0, 1, 0, 0.719348073, 0, 0.694649816)
		elseif Lv == 210 or Lv <= 249 or SelectMonster == "Dangerous Prisoner" or SelectArea == 'Prison' then -- Dangerous Prisoner
			Ms = "Dangerous Prisoner"
			NameQuest = "PrisonerQuest"
			QuestLv = 2
			NameMon = "Dangerous Prisoner"
			CFrameQ = CFrame.new(5310.60547, 0.350014925, 474.946594, 0.0175017118, 0, 0.999846935, 0, 1, 0, -0.999846935, 0, 0.0175017118)
			CFrameMon = CFrame.new(5099.6626, 0.351562679, 1055.7583, 0.898906827, 0, -0.438139856, 0, 1, 0, 0.438139856, 0, 0.898906827)
		elseif Lv == 250 or Lv <= 299 or SelectMonster == "Toga Warrior" or SelectArea == 'Colosseum' then -- Toga Warrior
			Ms = "Toga Warrior"
			NameQuest = "ColosseumQuest"
			QuestLv = 1
			NameMon = "Toga Warrior"
			CFrameQ = CFrame.new(-1577.7890625, 7.4151420593262, -2984.4838867188)
			CFrameMon = CFrame.new(-1872.5166015625, 49.080215454102, -2913.810546875)
		elseif Lv == 300 or Lv <= 324 or SelectMonster == "Military Soldier" or SelectArea == 'Magma' then -- Military Soldier
			Ms = "Military Soldier"
			NameQuest = "MagmaQuest"
			QuestLv = 1
			NameMon = "Military Soldier"
			CFrameQ = CFrame.new(-5316.1157226563, 12.262831687927, 8517.00390625)
			CFrameMon = CFrame.new(-5369.0004882813, 61.24352645874, 8556.4921875)
		elseif Lv == 325 or Lv <= 374 or SelectMonster == "Military Spy" or SelectArea == 'Magma' then -- Military Spy
			Ms = "Military Spy"
			NameQuest = "MagmaQuest"
			QuestLv = 2
			NameMon = "Military Spy"
			CFrameQ = CFrame.new(-5316.1157226563, 12.262831687927, 8517.00390625)
			CFrameMon = CFrame.new(-5802.8681640625, 86.26241302490234, 8828.859375)
		elseif Lv == 375 or Lv <= 399 or SelectMonster == "Fishman Warrior" or SelectArea == 'Fishman' then -- Fishman Warrior
			Ms = "Fishman Warrior"
			NameQuest = "FishmanQuest"
			QuestLv = 1
			NameMon = "Fishman Warrior"
			CFrameQ = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
			CFrameMon = CFrame.new(60844.10546875, 98.462875366211, 1298.3985595703)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
			end
		elseif Lv == 400 or Lv <= 449 or SelectMonster == "Fishman Commando" or SelectArea == 'Fishman' then -- Fishman Commando
			Ms = "Fishman Commando"
			NameQuest = "FishmanQuest"
			QuestLv = 2
			NameMon = "Fishman Commando"
			CFrameQ = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
			CFrameMon = CFrame.new(61738.3984375, 64.207321166992, 1433.8375244141)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
			end
		elseif Lv == 450 or Lv <= 474 or SelectMonster == "God's Guard" or SelectArea == 'Sky Island' then -- God's Guard
			Ms = "God's Guard"
			NameQuest = "SkyExp1Quest"
			QuestLv = 1
			NameMon = "God's Guard"
			CFrameQ = CFrame.new(-4721.8603515625, 845.30297851563, -1953.8489990234)
			CFrameMon = CFrame.new(-4628.0498046875, 866.92877197266, -1931.2352294922)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
			end
		elseif Lv == 475 or Lv <= 524 or SelectMonster == "Shanda" or SelectArea == 'Sky Island' then -- Shanda
			Ms = "Shanda"
			NameQuest = "SkyExp1Quest"
			QuestLv = 2
			NameMon = "Shanda"
			CFrameQ = CFrame.new(-7863.1596679688, 5545.5190429688, -378.42266845703)
			CFrameMon = CFrame.new(-7685.1474609375, 5601.0751953125, -441.38876342773)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
			end
		elseif Lv == 525 or Lv <= 549 or SelectMonster == "Royal Squad" or SelectArea == 'Sky Island' then -- Royal Squad
			Ms = "Royal Squad"
			NameQuest = "SkyExp2Quest"
			QuestLv = 1
			NameMon = "Royal Squad"
			CFrameQ = CFrame.new(-7903.3828125, 5635.9897460938, -1410.923828125)
			CFrameMon = CFrame.new(-7654.2514648438, 5637.1079101563, -1407.7550048828)
		elseif Lv == 550 or Lv <= 624 or SelectMonster == "Royal Soldier" or SelectArea == 'Sky Island' then -- Royal Soldier
			Ms = "Royal Soldier"
			NameQuest = "SkyExp2Quest"
			QuestLv = 2
			NameMon = "Royal Soldier"
			CFrameQ = CFrame.new(-7903.3828125, 5635.9897460938, -1410.923828125)
			CFrameMon = CFrame.new(-7760.4106445313, 5679.9077148438, -1884.8112792969)
		elseif Lv == 625 or Lv <= 649 or SelectMonster == "Galley Pirate" or SelectArea == 'Fountain' then -- Galley Pirate
			Ms = "Galley Pirate"
			NameQuest = "FountainQuest"
			QuestLv = 1
			NameMon = "Galley Pirate"
			CFrameQ = CFrame.new(5258.2788085938, 38.526931762695, 4050.044921875)
			CFrameMon = CFrame.new(5557.1684570313, 152.32717895508, 3998.7758789063)
		elseif Lv >= 650 or SelectMonster == "Galley Captain" or SelectArea == 'Fountain' then -- Galley Captain
			Ms = "Galley Captain"
			NameQuest = "FountainQuest"
			QuestLv = 2
			NameMon = "Galley Captain"
			CFrameQ = CFrame.new(5258.2788085938, 38.526931762695, 4050.044921875)
			CFrameMon = CFrame.new(5677.6772460938, 92.786109924316, 4966.6323242188)
		end
	end
	if Second_Sea then
		if Lv == 700 or Lv <= 724 or SelectMonster == "Raider" or SelectArea == 'Area 1' then -- Raider
			Ms = "Raider"
			NameQuest = "Area1Quest"
			QuestLv = 1
			NameMon = "Raider"
			CFrameQ = CFrame.new(-427.72567749023, 72.99634552002, 1835.9426269531)
			CFrameMon = CFrame.new(68.874565124512, 93.635643005371, 2429.6752929688)
		elseif Lv == 725 or Lv <= 774 or SelectMonster == "Mercenary" or SelectArea == 'Area 1' then -- Mercenary
			Ms = "Mercenary"
			NameQuest = "Area1Quest"
			QuestLv = 2
			NameMon = "Mercenary"
			CFrameQ = CFrame.new(-427.72567749023, 72.99634552002, 1835.9426269531)
			CFrameMon = CFrame.new(-864.85009765625, 122.47104644775, 1453.1505126953)
		elseif Lv == 775 or Lv <= 799 or SelectMonster == "Swan Pirate" or SelectArea == 'Area 2' then -- Swan Pirate
			Ms = "Swan Pirate"
			NameQuest = "Area2Quest"
			QuestLv = 1
			NameMon = "Swan Pirate"
			CFrameQ = CFrame.new(635.61151123047, 73.096351623535, 917.81298828125)
			CFrameMon = CFrame.new(1065.3669433594, 137.64012145996, 1324.3798828125)
		elseif Lv == 800 or Lv <= 874 or SelectMonster == "Factory Staff" or SelectArea == 'Area 2' then -- Factory Staff
			Ms = "Factory Staff"
			NameQuest = "Area2Quest"
			QuestLv = 2
			NameMon = "Factory Staff"
			CFrameQ = CFrame.new(635.61151123047, 73.096351623535, 917.81298828125)
			CFrameMon = CFrame.new(533.22045898438, 128.46876525879, 355.62615966797)
		elseif Lv == 875 or Lv <= 899 or SelectMonster == "Marine Lieutenan" or SelectArea == 'Marine' then -- Marine Lieutenant
			Ms = "Marine Lieutenant"
			NameQuest = "MarineQuest3"
			QuestLv = 1
			NameMon = "Marine Lieutenant"
			CFrameQ = CFrame.new(-2440.9934082031, 73.04190826416, -3217.7082519531)
			CFrameMon = CFrame.new(-2489.2622070313, 84.613594055176, -3151.8830566406)
		elseif Lv == 900 or Lv <= 949 or SelectMonster == "Marine Captain" or SelectArea == 'Marine' then -- Marine Captain
			Ms = "Marine Captain"
			NameQuest = "MarineQuest3"
			QuestLv = 2
			NameMon = "Marine Captain"
			CFrameQ = CFrame.new(-2440.9934082031, 73.04190826416, -3217.7082519531)
			CFrameMon = CFrame.new(-2335.2026367188, 79.786659240723, -3245.8674316406)
		elseif Lv == 950 or Lv <= 974 or SelectMonster == "Zombie" or SelectArea == 'Zombie' then -- Zombie
			Ms = "Zombie"
			NameQuest = "ZombieQuest"
			QuestLv = 1
			NameMon = "Zombie"
			CFrameQ = CFrame.new(-5494.3413085938, 48.505931854248, -794.59094238281)
			CFrameMon = CFrame.new(-5536.4970703125, 101.08577728271, -835.59075927734)
		elseif Lv == 975 or Lv <= 999 or SelectMonster == "Vampire" or SelectArea == 'Zombie' then -- Vampire
			Ms = "Vampire"
			NameQuest = "ZombieQuest"
			QuestLv = 2
			NameMon = "Vampire"
			CFrameQ = CFrame.new(-5494.3413085938, 48.505931854248, -794.59094238281)
			CFrameMon = CFrame.new(-5806.1098632813, 16.722528457642, -1164.4384765625)
		elseif Lv == 1000 or Lv <= 1049 or SelectMonster == "Snow Trooper" or SelectArea == 'Snow Mountain' then -- Snow Trooper
			Ms = "Snow Trooper"
			NameQuest = "SnowMountainQuest"
			QuestLv = 1
			NameMon = "Snow Trooper"
			CFrameQ = CFrame.new(607.05963134766, 401.44781494141, -5370.5546875)
			CFrameMon = CFrame.new(535.21051025391, 432.74209594727, -5484.9165039063)
		elseif Lv == 1050 or Lv <= 1099 or SelectMonster == "Winter Warrior" or SelectArea == 'Snow Mountain' then -- Winter Warrior
			Ms = "Winter Warrior"
			NameQuest = "SnowMountainQuest"
			QuestLv = 2
			NameMon = "Winter Warrior"
			CFrameQ = CFrame.new(607.05963134766, 401.44781494141, -5370.5546875)
			CFrameMon = CFrame.new(1234.4449462891, 456.95419311523, -5174.130859375)
		elseif Lv == 1100 or Lv <= 1124 or SelectMonster == "Lab Subordinate" or SelectArea == 'Ice Fire' then -- Lab Subordinate
			Ms = "Lab Subordinate"
			NameQuest = "IceSideQuest"
			QuestLv = 1
			NameMon = "Lab Subordinate"
			CFrameQ = CFrame.new(-6061.841796875, 15.926671981812, -4902.0385742188)
			CFrameMon = CFrame.new(-5720.5576171875, 63.309471130371, -4784.6103515625)
		elseif Lv == 1125 or Lv <= 1174 or SelectMonster == "Horned Warrior" or SelectArea == 'Ice Fire' then -- Horned Warrior
			Ms = "Horned Warrior"
			NameQuest = "IceSideQuest"
			QuestLv = 2
			NameMon = "Horned Warrior"
			CFrameQ = CFrame.new(-6061.841796875, 15.926671981812, -4902.0385742188)
			CFrameMon = CFrame.new(-6292.751953125, 91.181983947754, -5502.6499023438)
		elseif Lv == 1175 or Lv <= 1199 or SelectMonster == "Magma Ninja" or SelectArea == 'Ice Fire' then -- Magma Ninja
			Ms = "Magma Ninja"
			NameQuest = "FireSideQuest"
			QuestLv = 1
			NameMon = "Magma Ninja"
			CFrameQ = CFrame.new(-5429.0473632813, 15.977565765381, -5297.9614257813)
			CFrameMon = CFrame.new(-5461.8388671875, 130.36347961426, -5836.4702148438)
		elseif Lv == 1200 or Lv <= 1249 or SelectMonster == "Lava Pirate" or SelectArea == 'Ice Fire' then -- Lava Pirate
			Ms = "Lava Pirate"
			NameQuest = "FireSideQuest"
			QuestLv = 2
			NameMon = "Lava Pirate"
			CFrameQ = CFrame.new(-5429.0473632813, 15.977565765381, -5297.9614257813)
			CFrameMon = CFrame.new(-5251.1889648438, 55.164535522461, -4774.4096679688)
		elseif Lv == 1250 or Lv <= 1274 or SelectMonster == "Ship Deckhand" or SelectArea == 'Ship' then -- Ship Deckhand
			Ms = "Ship Deckhand"
			NameQuest = "ShipQuest1"
			QuestLv = 1
			NameMon = "Ship Deckhand"
			CFrameQ = CFrame.new(1040.2927246094, 125.08293151855, 32911.0390625)
			CFrameMon = CFrame.new(921.12365722656, 125.9839553833, 33088.328125)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
			end
		elseif Lv == 1275 or Lv <= 1299 or SelectMonster == "Ship Engineer" or SelectArea == 'Ship' then -- Ship Engineer
			Ms = "Ship Engineer"
			NameQuest = "ShipQuest1"
			QuestLv = 2
			NameMon = "Ship Engineer"
			CFrameQ = CFrame.new(1040.2927246094, 125.08293151855, 32911.0390625)
			CFrameMon = CFrame.new(886.28179931641, 40.47790145874, 32800.83203125)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
			end
		elseif Lv == 1300 or Lv <= 1324 or SelectMonster == "Ship Steward" or SelectArea == 'Ship' then -- Ship Steward
			Ms = "Ship Steward"
			NameQuest = "ShipQuest2"
			QuestLv = 1
			NameMon = "Ship Steward"
			CFrameQ = CFrame.new(971.42065429688, 125.08293151855, 33245.54296875)
			CFrameMon = CFrame.new(943.85504150391, 129.58183288574, 33444.3671875)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
			end
		elseif Lv == 1325 or Lv <= 1349 or SelectMonster == "Ship Officer" or SelectArea == 'Ship' then -- Ship Officer
			Ms = "Ship Officer"
			NameQuest = "ShipQuest2"
			QuestLv = 2
			NameMon = "Ship Officer"
			CFrameQ = CFrame.new(971.42065429688, 125.08293151855, 33245.54296875)
			CFrameMon = CFrame.new(955.38458251953, 181.08335876465, 33331.890625)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
			end
		elseif Lv == 1350 or Lv <= 1374 or SelectMonster == "Arctic Warrior" or SelectArea == 'Frost' then -- Arctic Warrior
			Ms = "Arctic Warrior"
			NameQuest = "FrostQuest"
			QuestLv = 1
			NameMon = "Arctic Warrior"
			CFrameQ = CFrame.new(5668.1372070313, 28.202531814575, -6484.6005859375)
			CFrameMon = CFrame.new(5935.4541015625, 77.26016998291, -6472.7568359375)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422))
			end
		elseif Lv == 1375 or Lv <= 1424 or SelectMonster == "Snow Lurker" or SelectArea == 'Frost' then -- Snow Lurker
			Ms = "Snow Lurker"
			NameQuest = "FrostQuest"
			QuestLv = 2
			NameMon = "Snow Lurker"
			CFrameQ = CFrame.new(5668.1372070313, 28.202531814575, -6484.6005859375)
			CFrameMon = CFrame.new(5628.482421875, 57.574996948242, -6618.3481445313)
		elseif Lv == 1425 or Lv <= 1449 or SelectMonster == "Sea Soldier" or SelectArea == 'Forgotten' then -- Sea Soldier
			Ms = "Sea Soldier"
			NameQuest = "ForgottenQuest"
			QuestLv = 1
			NameMon = "Sea Soldier"
			CFrameQ = CFrame.new(-3054.5827636719, 236.87213134766, -10147.790039063)
			CFrameMon = CFrame.new(-3185.0153808594, 58.789089202881, -9663.6064453125)
		elseif Lv >= 1450 or SelectMonster == "Water Fighter" or SelectArea == 'Forgotten' then -- Water Fighter
			Ms = "Water Fighter"
			NameQuest = "ForgottenQuest"
			QuestLv = 2
			NameMon = "Water Fighter"
			CFrameQ = CFrame.new(-3054.5827636719, 236.87213134766, -10147.790039063)
			CFrameMon = CFrame.new(-3262.9301757813, 298.69036865234, -10552.529296875)
		end
	end
	if Third_Sea then
		if Lv == 1500 or Lv <= 1524 or SelectMonster == "Pirate Millionaire" or SelectArea == 'Pirate Port' then -- Pirate Millionaire
			Ms = "Pirate Millionaire"
			NameQuest = "PiratePortQuest"
			QuestLv = 1
			NameMon = "Pirate Millionaire"
			CFrameQ = CFrame.new(-289.61752319336, 43.819011688232, 5580.0903320313)
			CFrameMon = CFrame.new(-435.68109130859, 189.69866943359, 5551.0756835938)
		elseif Lv == 1525 or Lv <= 1574 or SelectMonster == "Pistol Billionaire" or SelectArea == 'Pirate Port' then -- Pistol Billoonaire
			Ms = "Pistol Billionaire"
			NameQuest = "PiratePortQuest"
			QuestLv = 2
			NameMon = "Pistol Billionaire"
			CFrameQ = CFrame.new(-289.61752319336, 43.819011688232, 5580.0903320313)
			CFrameMon = CFrame.new(-236.53652954102, 217.46676635742, 6006.0883789063)
		elseif Lv == 1575 or Lv <= 1599 or SelectMonster == "Dragon Crew Warrior" or SelectArea == 'Amazon' then -- Dragon Crew Warrior
			Ms = "Dragon Crew Warrior"
			NameQuest = "AmazonQuest"
			QuestLv = 1
			NameMon = "Dragon Crew Warrior"
			CFrameQ = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
			CFrameMon = CFrame.new(6301.9975585938, 104.77153015137, -1082.6075439453)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				local args = {
					[1] = "requestEntrance",
					[2] = Vector3.new(5314.58203125, 25.419387817382812, -125.94227600097656)
				}

				game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))                
			end
		elseif Lv == 1600 or Lv <= 1624 or SelectMonster == "Dragon Crew Archer" or SelectArea == 'Amazon' then -- Dragon Crew Archer
			Ms = "Dragon Crew Archer"
			NameQuest = "AmazonQuest"
			QuestLv = 2
			NameMon = "Dragon Crew Archer"
			CFrameQ = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
			CFrameMon = CFrame.new(6831.1171875, 441.76708984375, 446.58615112305)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				local args = {
					[1] = "requestEntrance",
					[2] = Vector3.new(5314.58203125, 25.419387817382812, -125.94227600097656)
				}

				game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))                
			end
		elseif Lv == 1625 or Lv <= 1649 or SelectMonster == "Female Islander" or SelectArea == 'Amazon' then -- Female Islander
			Ms = "Female Islander"
			NameQuest = "AmazonQuest2"
			QuestLv = 1
			NameMon = "Female Islander"
			CFrameQ = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
			CFrameMon = CFrame.new(5792.5166015625, 848.14392089844, 1084.1818847656)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				local args = {
					[1] = "requestEntrance",
					[2] = Vector3.new(5742.9599609375, 613.9691772460938, -283.685546875)
				}

				game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))
			end
		elseif Lv == 1650 or Lv <= 1699 or SelectMonster == "Giant Islander" or SelectArea == 'Amazon' then -- Giant Islander
			Ms = "Giant Islander"
			NameQuest = "AmazonQuest2"
			QuestLv = 2
			NameMon = "Giant Islander"
			CFrameQ = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
			CFrameMon = CFrame.new(5009.5068359375, 664.11071777344, -40.960144042969)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				local args = {
					[1] = "requestEntrance",
					[2] = Vector3.new(5742.9599609375, 613.9691772460938, -283.685546875)
				}

				game:GetService("ReplicatedStorage"):WaitForChild("Remotes"):WaitForChild("CommF_"):InvokeServer(unpack(args))
			end
		elseif Lv == 1700 or Lv <= 1724 or SelectMonster == "Marine Commodore" or SelectArea == 'Marine Tree' then -- Marine Commodore
			Ms = "Marine Commodore"
			NameQuest = "MarineTreeIsland"
			QuestLv = 1
			NameMon = "Marine Commodore"
			CFrameQ = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
			CFrameMon = CFrame.new(2198.0063476563, 128.71075439453, -7109.5043945313)
		elseif Lv == 1725 or Lv <= 1774 or SelectMonster == "Marine Rear Admiral" or SelectArea == 'Marine Tree' then -- Marine Rear Admiral
			LevelFarm = 8
			Ms = "Marine Rear Admiral"
			NameQuest = "MarineTreeIsland"
			QuestLv = 2
			NameMon = "Marine Rear Admiral"
			CFrameQ = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
			CFrameMon = CFrame.new(3294.3142089844, 385.41125488281, -7048.6342773438)
		elseif Lv == 1775 or Lv <= 1799 or SelectMonster == "Fishman Raider" or SelectArea == 'Deep Forest' then -- Fishman Raide
			Ms = "Fishman Raider"
			NameQuest = "DeepForestIsland3"
			QuestLv = 1
			NameMon = "Fishman Raider"
			CFrameQ = CFrame.new(-10582.759765625, 331.78845214844, -8757.666015625)
			CFrameMon = CFrame.new(-10553.268554688, 521.38439941406, -8176.9458007813)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-11993.580078125, 334.7812805175781, -8844.1826171875))
			end
		elseif Lv == 1800 or Lv <= 1824 or SelectMonster == "Fishman Captain" or SelectArea == 'Deep Forest' then -- Fishman Captain
			Ms = "Fishman Captain"
			NameQuest = "DeepForestIsland3"
			QuestLv = 2
			NameMon = "Fishman Captain"
			CFrameQ = CFrame.new(-10583.099609375, 331.78845214844, -8759.4638671875)
			CFrameMon = CFrame.new(-10789.401367188, 427.18637084961, -9131.4423828125)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-11993.580078125, 334.7812805175781, -8844.1826171875))
			end
		elseif Lv == 1825 or Lv <= 1849 or SelectMonster == "Forest Pirate" or SelectArea == 'Deep Forest' then -- Forest Pirate
			Ms = "Forest Pirate"
			NameQuest = "DeepForestIsland"
			QuestLv = 1
			NameMon = "Forest Pirate"
			CFrameQ = CFrame.new(-13232.662109375, 332.40396118164, -7626.4819335938)
			CFrameMon = CFrame.new(-13489.397460938, 400.30349731445, -7770.251953125)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-12463.6025390625, 378.3270568847656, -7566.0830078125))
			end
		elseif Lv == 1850 or Lv <= 1899 or SelectMonster == "Mythological Pirate" or SelectArea == 'Deep Forest' then -- Mythological Pirate
			Ms = "Mythological Pirate"
			NameQuest = "DeepForestIsland"
			QuestLv = 2
			NameMon = "Mythological Pirate"
			CFrameQ = CFrame.new(-13232.662109375, 332.40396118164, -7626.4819335938)
			CFrameMon = CFrame.new(-13508.616210938, 582.46228027344, -6985.3037109375)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-12463.6025390625, 378.3270568847656, -7566.0830078125))
			end
		elseif Lv == 1900 or Lv <= 1924 or SelectMonster == "Jungle Pirate" or SelectArea == 'Deep Forest' then -- Jungle Pirate
			Ms = "Jungle Pirate"
			NameQuest = "DeepForestIsland2"
			QuestLv = 1
			NameMon = "Jungle Pirate"
			CFrameQ = CFrame.new(-12682.096679688, 390.88653564453, -9902.1240234375)
			CFrameMon = CFrame.new(-12267.103515625, 459.75262451172, -10277.200195313)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-11993.580078125, 334.7812805175781, -8844.1826171875))
			end
		elseif Lv == 1925 or Lv <= 1974 or SelectMonster == "Musketeer Pirate" or SelectArea == 'Deep Forest' then -- Musketeer Pirate
			Ms = "Musketeer Pirate"
			NameQuest = "DeepForestIsland2"
			QuestLv = 2
			NameMon = "Musketeer Pirate"
			CFrameQ = CFrame.new(-12682.096679688, 390.88653564453, -9902.1240234375)
			CFrameMon = CFrame.new(-13291.5078125, 520.47338867188, -9904.638671875)
			if _G.Auto_Farm_Level and (CFrameMon.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 20000 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-11993.580078125, 334.7812805175781, -8844.1826171875))
			end
		elseif Lv == 1975 or Lv <= 1999 or SelectMonster == "Reborn Skeleton" or SelectArea == 'Haunted Castle' then
			Ms = "Reborn Skeleton"
			NameQuest = "HauntedQuest1"
			QuestLv = 1
			NameMon = "Reborn Skeleton"
			CFrameQ = CFrame.new(-9480.80762, 142.130661, 5566.37305, -0.00655503059, 4.52954225e-08, -0.999978542, 2.04920472e-08, 1, 4.51620679e-08, 0.999978542, -2.01955679e-08, -0.00655503059)
			CFrameMon = CFrame.new(-8761.77148, 183.431747, 6168.33301, 0.978073597, -1.3950732e-05, -0.208259016, -1.08073925e-06, 1, -7.20630269e-05, 0.208259016, 7.07080399e-05, 0.978073597)
		elseif Lv == 2000 or Lv <= 2024 or SelectMonster == "Living Zombie" or SelectArea == 'Haunted Castle' then
			Ms = "Living Zombie"
			NameQuest = "HauntedQuest1"
			QuestLv = 2
			NameMon = "Living Zombie"
			CFrameQ = CFrame.new(-9480.80762, 142.130661, 5566.37305, -0.00655503059, 4.52954225e-08, -0.999978542, 2.04920472e-08, 1, 4.51620679e-08, 0.999978542, -2.01955679e-08, -0.00655503059)
			CFrameMon = CFrame.new(-10103.7529, 238.565979, 6179.75977, 0.999474227, 2.77547141e-08, 0.0324240364, -2.58006327e-08, 1, -6.06848474e-08, -0.0324240364, 5.98163865e-08, 0.999474227)
		elseif Lv == 2025 or Lv <= 2049 or SelectMonster == "Demonic Soul" or SelectArea == 'Haunted Castle' then
			Ms = "Demonic Soul"
			NameQuest = "HauntedQuest2"
			QuestLv = 1
			NameMon = "Demonic Soul"
			CFrameQ = CFrame.new(-9516.9931640625, 178.00651550293, 6078.4653320313)
			CFrameMon = CFrame.new(-9712.03125, 204.69589233398, 6193.322265625)
		elseif Lv == 2050 or Lv <= 2074 or SelectMonster == "Posessed Mummy" or SelectArea == 'Haunted Castle' then
			Ms = "Posessed Mummy"
			NameQuest = "HauntedQuest2"
			QuestLv = 2
			NameMon = "Posessed Mummy"
			CFrameQ = CFrame.new(-9516.9931640625, 178.00651550293, 6078.4653320313)
			CFrameMon = CFrame.new(-9545.7763671875, 69.619895935059, 6339.5615234375)
		elseif Lv == 2075 or Lv <= 2099 or SelectMonster == "Peanut Scout" or SelectArea == 'Nut Island' then
			Ms = "Peanut Scout"
			NameQuest = "NutsIslandQuest"
			QuestLv = 1
			NameMon = "Peanut Scout"
			CFrameQ = CFrame.new(-2105.53198, 37.2495995, -10195.5088, -0.766061664, 0, -0.642767608, 0, 1, 0, 0.642767608, 0, -0.766061664)
			CFrameMon = CFrame.new(-2150.587890625, 122.49767303467, -10358.994140625)
		elseif Lv == 2100 or Lv <= 2124 or SelectMonster == "Peanut President" or SelectArea == 'Nut Island' then
			Ms = "Peanut President"
			NameQuest = "NutsIslandQuest"
			QuestLv = 2
			NameMon = "Peanut President"
			CFrameQ = CFrame.new(-2105.53198, 37.2495995, -10195.5088, -0.766061664, 0, -0.642767608, 0, 1, 0, 0.642767608, 0, -0.766061664)
			CFrameMon = CFrame.new(-2150.587890625, 122.49767303467, -10358.994140625)
		elseif Lv == 2125 or Lv <= 2149 or SelectMonster == "Ice Cream Chef" or SelectArea == 'Ice Cream Island' then
			Ms = "Ice Cream Chef"
			NameQuest = "IceCreamIslandQuest"
			QuestLv = 1
			NameMon = "Ice Cream Chef"
			CFrameQ = CFrame.new(-819.376709, 64.9259796, -10967.2832, -0.766061664, 0, 0.642767608, 0, 1, 0, -0.642767608, 0, -0.766061664)
			CFrameMon = CFrame.new(-789.941528, 209.382889, -11009.9805, -0.0703101531, -0, -0.997525156, -0, 1.00000012, -0, 0.997525275, 0, -0.0703101456)
		elseif Lv == 2150 or Lv <= 2199 or SelectMonster == "Ice Cream Commander" or SelectArea == 'Ice Cream Island' then
			Ms = "Ice Cream Commander"
			NameQuest = "IceCreamIslandQuest"
			QuestLv = 2
			NameMon = "Ice Cream Commander"
			CFrameQ = CFrame.new(-819.376709, 64.9259796, -10967.2832, -0.766061664, 0, 0.642767608, 0, 1, 0, -0.642767608, 0, -0.766061664)
			CFrameMon = CFrame.new(-789.941528, 209.382889, -11009.9805, -0.0703101531, -0, -0.997525156, -0, 1.00000012, -0, 0.997525275, 0, -0.0703101456)
		elseif Lv == 2200 or Lv <= 2224 or SelectMonster == "Cookie Crafter" or SelectArea == 'Cake Island' then
			Ms = "Cookie Crafter"
			NameQuest = "CakeQuest1"
			QuestLv = 1
			NameMon = "Cookie Crafter"
			CFrameQ = CFrame.new(-2022.29858, 36.9275894, -12030.9766, -0.961273909, 0, -0.275594592, 0, 1, 0, 0.275594592, 0, -0.961273909)
			CFrameMon = CFrame.new(-2321.71216, 36.699482, -12216.7871, -0.780074954, 0, 0.625686109, 0, 1, 0, -0.625686109, 0, -0.780074954)
		elseif Lv == 2225 or Lv <= 2249 or SelectMonster == "Cake Guard" or SelectArea == 'Cake Island' then
			Ms = "Cake Guard"
			NameQuest = "CakeQuest1"
			QuestLv = 2
			NameMon = "Cake Guard"
			CFrameQ = CFrame.new(-2022.29858, 36.9275894, -12030.9766, -0.961273909, 0, -0.275594592, 0, 1, 0, 0.275594592, 0, -0.961273909)
			CFrameMon = CFrame.new(-1418.11011, 36.6718941, -12255.7324, 0.0677844882, 0, 0.997700036, 0, 1, 0, -0.997700036, 0, 0.0677844882)
		elseif Lv == 2250 or Lv <= 2274 or SelectMonster == "Baking Staff" or SelectArea == 'Cake Island' then
			Ms = "Baking Staff"
			NameQuest = "CakeQuest2"
			QuestLv = 1
			NameMon = "Baking Staff"
			CFrameQ = CFrame.new(-1928.31763, 37.7296638, -12840.626, 0.951068401, -0, -0.308980465, 0, 1, -0, 0.308980465, 0, 0.951068401)
			CFrameMon = CFrame.new(-1980.43848, 36.6716766, -12983.8418, -0.254443765, 0, -0.967087567, 0, 1, 0, 0.967087567, 0, -0.254443765)
		elseif Lv == 2275 or Lv <= 2299 or SelectMonster == "Head Baker" or SelectArea == 'Cake Island' then
			Ms = "Head Baker"
			NameQuest = "CakeQuest2"
			QuestLv = 2
			NameMon = "Head Baker"
			CFrameQ = CFrame.new(-1928.31763, 37.7296638, -12840.626, 0.951068401, -0, -0.308980465, 0, 1, -0, 0.308980465, 0, 0.951068401)
			CFrameMon = CFrame.new(-2251.5791, 52.2714615, -13033.3965, -0.991971016, 0, -0.126466095, 0, 1, 0, 0.126466095, 0, -0.991971016)
		elseif Lv == 2300 or Lv <= 2324 or SelectMonster == "Cocoa Warrior" or SelectArea == 'Choco Island' then
			Ms = "Cocoa Warrior"
			NameQuest = "ChocQuest1"
			QuestLv = 1
			NameMon = "Cocoa Warrior"
			CFrameQ = CFrame.new(231.75, 23.9003029, -12200.292, -1, 0, 0, 0, 1, 0, 0, 0, -1)
			CFrameMon = CFrame.new(167.978516, 26.2254658, -12238.874, -0.939700961, 0, 0.341998369, 0, 1, 0, -0.341998369, 0, -0.939700961)
		elseif Lv == 2325 or Lv <= 2349 or SelectMonster == "Chocolate Bar Battler" or SelectArea == 'Choco Island' then
			Ms = "Chocolate Bar Battler"
			NameQuest = "ChocQuest1"
			QuestLv = 2
			NameMon = "Chocolate Bar Battler"
			CFrameQ = CFrame.new(231.75, 23.9003029, -12200.292, -1, 0, 0, 0, 1, 0, 0, 0, -1)
			CFrameMon = CFrame.new(701.312073, 25.5824986, -12708.2148, -0.342042685, 0, -0.939684391, 0, 1, 0, 0.939684391, 0, -0.342042685)
		elseif Lv == 2350 or Lv <= 2374 or SelectMonster == "Sweet Thief" or SelectArea == 'Choco Island' then
			Ms = "Sweet Thief"
			NameQuest = "ChocQuest2"
			QuestLv = 1
			NameMon = "Sweet Thief"
			CFrameQ = CFrame.new(151.198242, 23.8907146, -12774.6172, 0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, 0.422592998)
			CFrameMon = CFrame.new(-140.258301, 25.5824986, -12652.3115, 0.173624337, -0, -0.984811902, 0, 1, -0, 0.984811902, 0, 0.173624337)
		elseif Lv == 2375 or Lv <= 2400 or SelectMonster == "Candy Rebel" or SelectArea == 'Choco Island' then
			Ms = "Candy Rebel"
			NameQuest = "ChocQuest2"
			QuestLv = 2
			NameMon = "Candy Rebel"
			CFrameQ = CFrame.new(151.198242, 23.8907146, -12774.6172, 0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, 0.422592998)
			CFrameMon = CFrame.new(47.9231453, 25.5824986, -13029.2402, -0.819156051, 0, -0.573571265, 0, 1, 0, 0.573571265, 0, -0.819156051)
		elseif Lv == 2400 or Lv <= 2424 or SelectMonster == "Candy Pirate" or SelectArea == 'Candy Island' then
			Ms = "Candy Pirate"
			NameQuest = "CandyQuest1"
			QuestLv = 1
			NameMon = "Candy Pirate"
			CFrameQ = CFrame.new(-1149.328, 13.5759039, -14445.6143, -0.156446099, 0, -0.987686574, 0, 1, 0, 0.987686574, 0, -0.156446099)
			CFrameMon = CFrame.new(-1437.56348, 17.1481285, -14385.6934, 0.173624337, -0, -0.984811902, 0, 1, -0, 0.984811902, 0, 0.173624337)
		elseif Lv == 2425 or Lv <= 2449 or SelectMonster == "Snow Demon" or SelectArea == 'Candy Island' then
			Ms = "Snow Demon"
			NameQuest = "CandyQuest1"
			QuestLv = 2
			NameMon = "Snow Demon"
			CFrameQ = CFrame.new(-1149.328, 13.5759039, -14445.6143, -0.156446099, 0, -0.987686574, 0, 1, 0, 0.987686574, 0, -0.156446099)
			CFrameMon = CFrame.new(-916.222656, 17.1481285, -14638.8125, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
		elseif Lv == 2450 or Lv <= 2474 or SelectMonster == "Isle Outlaw" or SelectArea == 'Tiki Outpost' then
			Ms = "Isle Outlaw"
			NameQuest = "TikiQuest1"
			QuestLv = 1
			NameMon = "Isle Outlaw"
			CFrameQ = CFrame.new(-16549.890625, 55.68635559082031, -179.91360473632812)
			CFrameMon = CFrame.new(-16162.8193359375, 11.6863374710083, -96.45481872558594)
		elseif Lv == 2475 or Lv <= 2524 or SelectMonster == "Island Boy" or SelectArea == 'Tiki Outpost' then
			Ms = "Island Boy"
			NameQuest = "TikiQuest1"
			QuestLv = 2
			NameMon = "Island Boy"
			CFrameQ = CFrame.new(-16549.890625, 55.68635559082031, -179.91360473632812)
			CFrameMon = CFrame.new(-16912.130859375, 11.787443161010742, -133.0850830078125)
		elseif Lv >= 2525 or SelectMonster == "Isle Champion" or SelectArea == 'Tiki Outpost' then
			Ms = "Isle Champion"
			NameQuest = "TikiQuest2"
			QuestLv = 2
			NameMon = "Isle Champion"
			CFrameQ = CFrame.new(-16542.447265625, 55.68632888793945, 1044.41650390625)
			CFrameMon = CFrame.new(-16848.94140625, 21.68633460998535, 1041.4490966796875)
		end
	end
end

function CheckBossQuest()
    if _G.Select_Boss == "Saber Expert" then 
        MsBoss = "Saber Expert"
        NameBoss = "Saber Expert"
        CFrameBoss = CFrame.new(-1458.89502, 29.8870335, -50.633564, 0.858821094, 1.13848939e-08, 0.512275636, -4.85649254e-09, 1, -1.40823326e-08, -0.512275636, 9.6063415e-09, 0.858821094)
    elseif _G.Select_Boss == "The Saw" then 
        MsBoss = "The Saw"
        NameBoss = "The Saw"
        CFrameBoss = CFrame.new(-683.519897, 13.8534927, 1610.87854, -0.290192783, 6.88365773e-08, 0.956968188, 6.98413629e-08, 1, -5.07531119e-08, -0.956968188, 5.21077759e-08, -0.290192783)
    elseif _G.Select_Boss == "Greybeard" then
        MsBoss = "Greybeard"
        NameBoss = "Greybeard"
        CFrameBoss = CFrame.new(-4955.72949, 80.8163834, 4305.82666, -0.433646321, -1.03394289e-08, 0.901083171, -3.0443168e-08, 1, -3.17633075e-09, -0.901083171, -2.88092288e-08, -0.433646321)
    elseif _G.Select_Boss == "The Gorilla King" then
        MsBoss = "The Gorilla King"
        NameBoss = "The Gorilla King"
        NameQuestBoss = "JungleQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-1604.12012, 36.8521118, 154.23732, 0.0648873374, -4.70858913e-06, -0.997892559, 1.41431883e-07, 1, -4.70933674e-06, 0.997892559, 1.64442184e-07, 0.0648873374)
        CFrameBoss = CFrame.new(-1223.52808, 6.27936459, -502.292664, 0.310949147, -5.66602516e-08, 0.950426519, -3.37275488e-08, 1, 7.06501808e-08, -0.950426519, -5.40241736e-08, 0.310949147)
    elseif _G.Select_Boss == "Bobby" then
        MsBoss = "Bobby"
        NameBoss = "Bobby"
        NameQuestBoss = "BuggyQuest1"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-1139.59717, 4.75205183, 3825.16211, -0.959730506, -7.5857054e-09, 0.280922383, -4.06310328e-08, 1, -1.11807175e-07, -0.280922383, -1.18718916e-07, -0.959730506)
        CFrameBoss = CFrame.new(-1147.65173, 32.5966301, 4156.02588, 0.956680477, -1.77109952e-10, -0.29113996, 5.16530874e-10, 1, 1.08897802e-09, 0.29113996, -1.19218679e-09, 0.956680477)
    elseif _G.Select_Boss == "Yeti" then
        MsBoss = "Yeti"
        NameBoss = "Yeti"
        NameQuestBoss = "SnowQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(1384.90247, 87.3078308, -1296.6825, 0.280209213, 2.72035177e-08, -0.959938943, -6.75690828e-08, 1, 8.6151708e-09, 0.959938943, 6.24481444e-08, 0.280209213)
        CFrameBoss = CFrame.new(1221.7356, 138.046906, -1488.84082, 0.349343032, -9.49245944e-08, 0.936994851, 6.29478194e-08, 1, 7.7838429e-08, -0.936994851, 3.17894653e-08, 0.349343032)
    elseif _G.Select_Boss == "Mob Leader" then
        MsBoss = "Mob Leader"
        NameBoss = "Mob Leader"
        CFrameBoss = CFrame.new(-2848.59399, 7.4272871, 5342.44043, -0.928248107, -8.7248246e-08, 0.371961564, -7.61816636e-08, 1, 4.44474857e-08, -0.371961564, 1.29216433e-08, -0.92824)
    elseif _G.Select_Boss == "Vice Admiral" then
        MsBoss = "Vice Admiral"
        NameBoss = "Vice Admiral"
        NameQuestBoss = "MarineQuest2"
        LevelQuestBoss = 2
        CFrameQuestBoss = CFrame.new(-5035.42285, 28.6520386, 4324.50293, -0.0611100644, -8.08395768e-08, 0.998130739, -1.57416586e-08, 1, 8.00271849e-08, -0.998130739, -1.08217701e-08, -0.0611100644)
        CFrameBoss = CFrame.new(-5078.45898, 99.6520691, 4402.1665, -0.555574954, -9.88630566e-11, 0.831466436, -6.35508286e-08, 1, -4.23449258e-08, -0.831466436, -7.63661632e-08, -0.555574954)
    elseif _G.Select_Boss == "Warden" then
        MsBoss = "Warden"
        NameBoss = "Warden"
        NameQuestBoss = "ImpelQuest"
        LevelQuestBoss = 1
        CFrameQuestBoss = CFrame.new(4851.35059, 5.68744135, 743.251282, -0.538484037, -6.68303741e-08, -0.842635691, 1.38001752e-08, 1, -8.81300792e-08, 0.842635691, -5.90851599e-08, -0.538484037)
        CFrameBoss = CFrame.new(5232.5625, 5.26856995, 747.506897, 0.943829298, -4.5439414e-08, 0.330433697, 3.47818627e-08, 1, 3.81658154e-08, -0.330433697, -2.45289105e-08, 0.943829298)
    elseif _G.Select_Boss == "Chief Warden" then
        MsBoss = "Chief Warden"
        NameBoss = "Chief Warden"
        NameQuestBoss = "ImpelQuest"
        LevelQuestBoss = 2
        CFrameQuestBoss = CFrame.new(4851.35059, 5.68744135, 743.251282, -0.538484037, -6.68303741e-08, -0.842635691, 1.38001752e-08, 1, -8.81300792e-08, 0.842635691, -5.90851599e-08, -0.538484037)
        CFrameBoss = CFrame.new(5232.5625, 5.26856995, 747.506897, 0.943829298, -4.5439414e-08, 0.330433697, 3.47818627e-08, 1, 3.81658154e-08, -0.330433697, -2.45289105e-08, 0.943829298)
    elseif _G.Select_Boss == "Swan" then
        MsBoss = "Swan"
        NameBoss = "Swan"
        NameQuestBoss = "ImpelQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(4851.35059, 5.68744135, 743.251282, -0.538484037, -6.68303741e-08, -0.842635691, 1.38001752e-08, 1, -8.81300792e-08, 0.842635691, -5.90851599e-08, -0.538484037)
        CFrameBoss = CFrame.new(5232.5625, 5.26856995, 747.506897, 0.943829298, -4.5439414e-08, 0.330433697, 3.47818627e-08, 1, 3.81658154e-08, -0.330433697, -2.45289105e-08, 0.943829298)
    elseif _G.Select_Boss == "Magma Admiral" then
        MsBoss = "Magma Admiral"
        NameBoss = "Magma Admiral"
        NameQuestBoss = "MagmaQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-5317.07666, 12.2721891, 8517.41699, 0.51175487, -2.65508806e-08, -0.859131515, -3.91131572e-08, 1, -5.42026761e-08, 0.859131515, 6.13418294e-08, 0.51175487)
        CFrameBoss = CFrame.new(-5530.12646, 22.8769703, 8859.91309, 0.857838571, 2.23414389e-08, 0.513919294, 1.53689133e-08, 1, -6.91265853e-08, -0.513919294, 6.71978384e-08, 0.857838571)
    elseif _G.Select_Boss == "Fishman Lord" then
        MsBoss = "Fishman Lord"
        NameBoss = "Fishman Lord"
        NameQuestBoss = "FishmanQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(61123.0859, 18.5066795, 1570.18018, 0.927145958, 1.0624845e-07, 0.374700129, -6.98219367e-08, 1, -1.10790765e-07, -0.374700129, 7.65569368e-08, 0.927145958)
        CFrameBoss = CFrame.new(61351.7773, 31.0306778, 1113.31409, 0.999974668, 0, -0.00714713801, 0, 1.00000012, 0, 0.00714714266, 0, 0.999974549)
    elseif _G.Select_Boss == "Wysper" then
        MsBoss = "Wysper"
        NameBoss = "Wysper"
        NameQuestBoss = "SkyExp1Quest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-7862.94629, 5545.52832, -379.833954, 0.462944925, 1.45838088e-08, -0.886386991, 1.0534996e-08, 1, 2.19553424e-08, 0.886386991, -1.95022007e-08, 0.462944925)
        CFrameBoss = CFrame.new(-7925.48389, 5550.76074, -636.178345, 0.716468513, -1.22915289e-09, 0.697619379, 3.37381434e-09, 1, -1.70304748e-09, -0.697619379, 3.57381835e-09, 0.716468513)
    elseif _G.Select_Boss == "Thunder God" then
        MsBoss = "Thunder God"
        NameBoss = "Thunder God"
        NameQuestBoss = "SkyExp2Quest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-7902.78613, 5635.99902, -1411.98706, -0.0361216255, -1.16895912e-07, 0.999347389, 1.44533963e-09, 1, 1.17024491e-07, -0.999347389, 5.6715117e-09, -0.0361216255)
        CFrameBoss = CFrame.new(-7917.53613, 5616.61377, -2277.78564, 0.965189934, 4.80563429e-08, -0.261550069, -6.73089886e-08, 1, -6.46515304e-08, 0.261550069, 8.00056768e-08, 0.965189934)
    elseif _G.Select_Boss == "Cyborg" then
        MsBoss = "Cyborg"
        NameBoss = "Cyborg"
        NameQuestBoss = "FountainQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(5253.54834, 38.5361786, 4050.45166, -0.0112687312, -9.93677887e-08, -0.999936521, 2.55291371e-10, 1, -9.93769547e-08, 0.999936521, -1.37512213e-09, -0.0112687312)
        CFrameBoss = CFrame.new(6041.82813, 52.7112198, 3907.45142, -0.563162148, 1.73805248e-09, -0.826346457, -5.94632716e-08, 1, 4.26280238e-08, 0.826346457, 7.31437524e-08, -0.563162148)
        -- New World
    elseif _G.Select_Boss == "Diamond" then
        MsBoss = "Diamond"
        NameBoss = "Diamond"
        NameQuestBoss = "Area1Quest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-424.080078, 73.0055847, 1836.91589, 0.253544956, -1.42165932e-08, 0.967323601, -6.00147771e-08, 1, 3.04272909e-08, -0.967323601, -6.5768397e-08, 0.253544956)
        CFrameBoss = CFrame.new(-1736.26587, 198.627731, -236.412857, -0.997808516, 0, -0.0661673471, 0, 1, 0, 0.0661673471, 0, -0.997808516)
    elseif _G.Select_Boss == "Jeremy" then
        MsBoss = "Jeremy"
        NameBoss = "Jeremy"
        NameQuestBoss = "Area2Quest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
        CFrameBoss = CFrame.new(2203.76953, 448.966034, 752.731079, -0.0217453763, 0, -0.999763548, 0, 1, 0, 0.999763548, 0, -0.0217453763)
    elseif _G.Select_Boss == "Fajita" then
        MsBoss = "Fajita"
        NameBoss = "Fajita"
        NameQuestBoss = "MarineQuest3"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-2442.65015, 73.0511475, -3219.11523, -0.873540044, 4.2329841e-08, -0.486752301, 5.64383384e-08, 1, -1.43220786e-08, 0.486752301, -3.99823996e-08, -0.873540044)
        CFrameBoss = CFrame.new(-2297.40332, 115.449463, -3946.53833, 0.961227536, -1.46645796e-09, -0.275756449, -2.3212845e-09, 1, -1.34094433e-08, 0.275756449, 1.35296352e-08, 0.961227536)
    elseif _G.Select_Boss == "Don Swan" then
        MsBoss = "Don Swan"
        NameBoss = "Don Swan"
        CFrameBoss = CFrame.new(2288.802, 15.1870775, 863.034607, 0.99974072, -8.41247214e-08, -0.0227668174, 8.4774733e-08, 1, 2.75850098e-08, 0.0227668174, -2.95079072e-08, 0.99974072)
    elseif _G.Select_Boss == "Smoke Admiral" then
        MsBoss = "Smoke Admiral"
        NameBoss = "Smoke Admiral"
        NameQuestBoss = "IceSideQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-6059.96191, 15.9868021, -4904.7373, -0.444992423, -3.0874483e-09, 0.895534337, -3.64098796e-08, 1, -1.4644522e-08, -0.895534337, -3.91229982e-08, -0.444992423)
        CFrameBoss = CFrame.new(-5115.72754, 23.7664986, -5338.2207, 0.251453817, 1.48345061e-08, -0.967869282, 4.02796978e-08, 1, 2.57916977e-08, 0.967869282, -4.54708946e-08, 0.251453817)
    elseif _G.Select_Boss == "Cursed Captain" then
        MsBoss = "Cursed Captain"
        NameBoss = "Cursed Captain"
        CFrameBoss = CFrame.new(916.928589, 181.092773, 33422, -0.999505103, 9.26310495e-09, 0.0314563364, 8.42916226e-09, 1, -2.6643713e-08, -0.0314563364, -2.63653774e-08, -0.999505103)
    elseif _G.Select_Boss == "Darkbeard" then
        MsBoss = "Darkbeard"
        NameBoss = "Darkbeard"
        CFrameBoss = CFrame.new(3876.00366, 24.6882591, -3820.21777, -0.976951957, 4.97356325e-08, 0.213458836, 4.57335361e-08, 1, -2.36868622e-08, -0.213458836, -1.33787044e-08, -0.976951957)
    elseif _G.Select_Boss == "Order" then
        MsBoss = "Order"
        NameBoss = "Order"
        CFrameBoss = CFrame.new(-6221.15039, 16.2351036, -5045.23584, -0.380726993, 7.41463495e-08, 0.924687505, 5.85604774e-08, 1, -5.60738549e-08, -0.924687505, 3.28013137e-08, -0.380726993)
    elseif _G.Select_Boss == "Awakened Ice Admiral" then
        MsBoss = "Awakened Ice Admiral"
        NameBoss = "Awakened Ice Admiral"
        NameQuestBoss = "FrostQuest"
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(5669.33203, 28.2118053, -6481.55908, 0.921275556, -1.25320829e-08, 0.388910472, 4.72230788e-08, 1, -7.96414241e-08, -0.388910472, 9.17372489e-08, 0.921275556)
        CFrameBoss = CFrame.new(6407.33936, 340.223785, -6892.521, 0.49051559, -5.25310213e-08, -0.871432424, -2.76146022e-08, 1, -7.58250565e-08, 0.871432424, 6.12576301e-08, 0.49051559)
    elseif _G.Select_Boss == "Tide Keeper" then
        MsBoss = "Tide Keeper"
        NameBoss = "Tide Keeper"
        NameQuestBoss = "ForgottenQuest"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-3053.89648, 236.881363, -10148.2324, -0.985987961, -3.58504737e-09, 0.16681771, -3.07832915e-09, 1, 3.29612559e-09, -0.16681771, 2.73641976e-09, -0.985987961)
        CFrameBoss = CFrame.new(-3570.18652, 123.328949, -11555.9072, 0.465199202, -1.3857326e-08, 0.885206044, 4.0332897e-09, 1, 1.35347511e-08, -0.885206044, -2.72606271e-09, 0.465199202)
        -- Thire World
    elseif _G.Select_Boss == "Stone" then
        MsBoss = "Stone"
        NameBoss = "Stone"
        NameQuestBoss = "PiratePortQuest"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-290, 44, 5577)
        CFrameBoss = CFrame.new(-1085, 40, 6779)
    elseif _G.Select_Boss == "Island Empress" then
        MsBoss = "Island Empress"
        NameBoss = "Island Empress"
        NameQuestBoss = "AmazonQuest2"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(5443, 602, 752)
        CFrameBoss = CFrame.new(5659, 602, 244)
    elseif _G.Select_Boss == "Kilo Admiral" then
        MsBoss = "Kilo Admiral"
        NameBoss = "Kilo Admiral"
        NameQuestBoss = "MarineTreeIsland"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(2178, 29, -6737)
        CFrameBoss =CFrame.new(2846, 433, -7100)
    elseif _G.Select_Boss == "Captain Elephant" then
        MsBoss = "Captain Elephant"
        NameBoss = "Captain Elephant"
        NameQuestBoss = "DeepForestIsland"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-13232, 333, -7631)
        CFrameBoss = CFrame.new(-13221, 325, -8405)
    elseif _G.Select_Boss == "Beautiful Pirate" then
        MsBoss = "Beautiful Pirate"
        NameBoss = "Beautiful Pirate"
        NameQuestBoss = "DeepForestIsland2"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-12686, 391, -9902)
        CFrameBoss = CFrame.new(5182, 23, -20)
    elseif _G.Select_Boss == "Cake Queen" then
        MsBoss = "Cake Queen"
        NameBoss = "Cake Queen"
        NameQuestBoss = "IceCreamIslandQuest"             
        LevelQuestBoss = 3
        CFrameQuestBoss = CFrame.new(-716, 382, -11010)
        CFrameBoss = CFrame.new(-821, 66, -10965)
    elseif _G.Select_Boss == "rip_indra True Form" then
        MsBoss = "rip_indra True Form"
        NameBoss = "rip_indra True Form"
        CFrameBoss = CFrame.new(-5359, 424, -2735)
    elseif _G.Select_Boss == "Longma" then
        MsBoss = "Longma"
        NameBoss = "Longma"
        CFrameBoss = CFrame.new(-10248.3936, 353.79129, -9306.34473)
    elseif _G.Select_Boss == "Soul Reaper" then
        MsBoss = "Soul Reaper"
        NameBoss = "Soul Reaper"
        CFrameBoss = CFrame.new(-9515.62109, 315.925537, 6691.12012)
    end
end

function AutoHaki()
	if not game:GetService("Players").LocalPlayer.Character:FindFirstChild("HasBuso") then
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
	end
end

function EquipTool(ToolSe)
	if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
		local tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
		wait(0.5)
		game.Players.LocalPlayer.Character.Humanoid:EquipTool(tool)
	end
end
function Tween(p)
	task.spawn(function()
		pcall(function()
			if game:GetService("Players").LocalPlayer:DistanceFromCharacter(p.Position) <= 200 then 
				game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = p
				if game.Players.LocalPlayer.Character:FindFirstChild("Root") then
					game.Players.LocalPlayer.Character:FindFirstChild("Root"):Destroy();
					wait()
					Tween(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
					wait()
					if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
						game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
					end
				end;
				if game.Players.LocalPlayer.Character:FindFirstChild("Root") then
					game.Players.LocalPlayer.Character:FindFirstChild("Root"):Remove();
				end;
			elseif not game.Players.LocalPlayer.Character:FindFirstChild("Root")then 
				local K = Instance.new("Part",game.Players.LocalPlayer.Character)
				local lpc = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
				K.Size = Vector3.new(1,0.5,1)
				K.Name = "Root"
				K.Anchored = true
				K.Transparency = 1
				K.CanCollide = false
				game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(lpc.X, 50, lpc.Z)
			end
			local r = game:GetService("Players").LocalPlayer
			local U = (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude
			local z = game:service("TweenService")
			local B = TweenInfo.new((p.Position-game.Players.LocalPlayer.Character.Root.Position).Magnitude/375,Enum.EasingStyle.Linear)
			local S,g = pcall(function()
				local q = z:Create(game.Players.LocalPlayer.Character.Root,B,{CFrame = p})
				if game.Players.LocalPlayer.Character.Humanoid.Sit == true then 
					game.Players.LocalPlayer.Character.Humanoid.Sit = false;
				end;
				q:Play()
			end)
			if not S then 
				return g
			end
			game.Players.LocalPlayer.Character.Root.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
			if S and game.Players.LocalPlayer.Character:FindFirstChild("Root") then 
				pcall(function()
					if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude >= 50 then 
						task.spawn(function()
							pcall(function()
								if (game.Players.LocalPlayer.Character.Root.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 200 then 
									game.Players.LocalPlayer.Character.Root.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
								else 
									game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=game.Players.LocalPlayer.Character.Root.CFrame
								end
							end)
						end)
					elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude >= 25 and(game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude < 40 then 
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
					elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-p.Position).Magnitude < 25 then 
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = p
					end
				end)
			end
		end)
	end)    
end
task.spawn(function()
	while task.wait() do 
		pcall(function()
			game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.Root.CFrame;
			if (game.Players.LocalPlayer.Character.Root.Position-game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1 then
				game.Players.LocalPlayer.Character.Root.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame;
			end
		end)
	end
end)

function StopTween(target)
    if not target then
        wait()
        Tween(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
        wait()
        if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
            game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
        end
    end
    if game.Players.LocalPlayer.Character:FindFirstChild("Root") then
        game.Players.LocalPlayer.Character:FindFirstChild("Root"):Destroy()
    end
end

function BTP(Position)
	game.Players.LocalPlayer.Character.Head:Destroy()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	wait(1)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
	wait(0.9)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	wait()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	wait(0.9)
	game.Players.LocalPlayer.Character.Head:Destroy()
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	wait(1)
	game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Position
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetSpawnPoint")
end
spawn(function()
	while task.wait() do
		pcall(function()
			if _G.Auto_Farm_Level or _G.NeareastFarm or _G.AutoSecondSea or _G.AutoThirdSea or _G.AutoElitehunter or _G.Auto_Bone or _G.Auto_Fully_Superhuman or _G.Auto_Dungeon_Superhuman or _G.Auto_Fully_Death_Step then
				if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
					local Noclip = Instance.new("BodyVelocity")
					Noclip.Name = "BodyClip"
					Noclip.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
					Noclip.MaxForce = Vector3.new(100000,100000,100000)
					Noclip.Velocity = Vector3.new(0,0,0)
				end
			else
				game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
			end
		end)
	end
end)
spawn(function()
	pcall(function()
		game:GetService("RunService").Stepped:Connect(function()
            if _G.Auto_Farm_Level or _G.NeareastFarm or _G.AutoSecondSea or _G.AutoThirdSea or _G.AutoElitehunter or _G.Auto_Bone or _G.Auto_Fully_Superhuman or _G.Auto_Dungeon_Superhuman or _G.Auto_Fully_Death_Step then
				for i,v in pairs(game:GetService("Players").LocalPlayer.Character:GetDescendants()) do
					if v:IsA("BasePart") then
						v.CanCollide = false
					end
				end
			end
		end)
	end)
end)
spawn(function()
    pcall(function()
        game:GetService("RunService").Stepped:Connect(function()
            if _G.Auto_Farm_Level or _G.AutoObservation or _G.TPNPCDF or _G.Auto_Kill_Player or AutoFarmMaterial or _G.AutoBuddySwords or _G.AutoCavander or _G.Bboat or _G.TPTOBOAT or _G.AutoEvent or _G.QRepairBoat or _G.QRepairBoat2 or _G.WoodPlank or _G.AutoMirageIsland or _G.Auto_Gear or _G.TptoKisuneIsland  or _G.NeareastFarm or _G.TptoKisuneshrine or _G.AutoFarmBossHallow or _G.Auto_Yama or _G.Auto_Sea_King or _G.Auto_Dack_Coat or _G.Auto_Rip_Indar or _G.Auto_Farm_Mastery_Gun or _G.Auto_Farm_All_Sword or _G.Auto_Awakening_One_Quest or _G.Auto_Lever_UnLock or _G.Auto_Complete_Trial or _G.Auto_Farm_Mastery_Fruit or Auto_Mirage_Island or Auto_Gear or _G.Auto_Farm_All_Boss or _G.Auto_New_World or _G.Auto_Third_World or _G.Auto_Farm_Chest or _G.Auto_Farm_Boss or _G.Auto_Castle_Raid or _G.Auto_Elite_Hunter or _G.Auto_Cake_Prince or _G.Auto_Farm_All_Boss or _G.Auto_Saber or _G.Auto_Pole or _G.Auto_Farm_Scrap_and_Leather or _G.Auto_Farm_Angel_Wing or _G.Auto_Factory_Farm or _G.Auto_Farm_Ectoplasm or _G.Auto_Bartilo_Quest or _G.Auto_Rengoku or _G.Auto_Farm_Radioactive or _G.Auto_Farm_Vampire_Fang or _G.Auto_Farm_Mystic_Droplet or _G.Auto_Farm_GunPowder or _G.Auto_Farm_Dragon_Scales or _G.Auto_Evo_Race_V2 or _G.Auto_Swan_Glasses or _G.Auto_Dragon_Trident or _G.Auto_Soul_Reaper or _G.Auto_Farm_Fish_Tail or _G.Auto_Farm_Mini_Tusk or _G.Auto_Farm_Magma_Ore or _G.Auto_Farm_Bone or _G.Auto_Farm_Conjured_Cocoa or _G.Auto_Open_Dough_Dungeon or _G.Auto_Rainbow_Haki or _G.Auto_Musketeer_Hat or _G.Auto_Holy_Torch or _G.Auto_Canvander or _G.Auto_Twin_Hook or _G.Auto_Serpent_Bow or _G.Auto_Fully_Death_Step or _G.Auto_Fully_SharkMan_Karate or _G.Teleport_to_Player or _G.Auto_Kill_Player_Melee or _G.Auto_Kill_Player_Gun or _G.Start_Tween_Island or _G.Auto_Next_Island or _G.Auto_Kill_Law then
                if not game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    local Noclip = Instance.new("BodyVelocity")
                    Noclip.Name = "BodyClip"
                    Noclip.Parent = game.Players.LocalPlayer.Character.HumanoidRootPart
                    Noclip.MaxForce = Vector3.new(100000,100000,100000)
                    Noclip.Velocity = Vector3.new(0,0,0)
                end
            else	
                if game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
                    game.Players.LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
                end
            end
        end)
    end)
end)
spawn(function()
    pcall(function()
        game:GetService("RunService").Stepped:Connect(function()
            if _G.Auto_Farm_Level or _G.AutoObservation or _G.TPNPCDF or _G.Auto_Kill_Player or AutoFarmMaterial or _G.AutoBuddySwords or _G.Bboat or _G.TPTOBOAT or _G.AutoEvent or _G.QRepairBoat or _G.QRepairBoat2 or _G.WoodPlank or _G.AutoCavander or _G.TPNPCDF or _G.AutoMirageIsland or _G.Auto_Gear or _G.TptoKisuneIsland or _G.NeareastFarm or _G.TptoKisuneshrine or _G.AutoFarmBossHallow or _G.Auto_Yama or _G.Auto_Sea_King or _G.Auto_Dack_Coat or _G.Auto_Rip_Indar or _G.Auto_Farm_Mastery_Gun or _G.Auto_Farm_All_Sword or _G.Auto_Awakening_One_Quest or _G.Auto_Farm_Mastery_Fruit or _G.Auto_Lever_UnLock or _G.Auto_Complete_Trial or Auto_Mirage_Island or Auto_Gear or _G.Auto_Farm_All_Boss or _G.Auto_New_World or _G.Auto_Third_World or _G.Auto_Farm_Chest or _G.Auto_Farm_Boss or _G.Auto_Castle_Raid or _G.Auto_Elite_Hunter or _G.Auto_Cake_Prince or _G.Auto_Farm_All_Boss or _G.Auto_Saber or _G.Auto_Pole or _G.Auto_Farm_Scrap_and_Leather or _G.Auto_Farm_Angel_Wing or _G.Auto_Factory_Farm or _G.Auto_Farm_Ectoplasm or _G.Auto_Bartilo_Quest or _G.Auto_Rengoku or _G.Auto_Farm_Radioactive or _G.Auto_Farm_Vampire_Fang or _G.Auto_Farm_Mystic_Droplet or _G.Auto_Farm_GunPowder or _G.Auto_Farm_Dragon_Scales or _G.Auto_Evo_Race_V2 or _G.Auto_Swan_Glasses or _G.Auto_Dragon_Trident or _G.Auto_Soul_Reaper or _G.Auto_Farm_Fish_Tail or _G.Auto_Farm_Mini_Tusk or _G.Auto_Farm_Magma_Ore or _G.Auto_Farm_Bone or _G.Auto_Farm_Conjured_Cocoa or _G.Auto_Open_Dough_Dungeon or _G.Auto_Rainbow_Haki or _G.Auto_Musketeer_Hat or _G.Auto_Holy_Torch or _G.Auto_Canvander or _G.Auto_Twin_Hook or _G.Auto_Serpent_Bow or _G.Auto_Fully_Death_Step or _G.Auto_Fully_SharkMan_Karate or _G.Teleport_to_Player or _G.Auto_Kill_Player_Melee or _G.Auto_Kill_Player_Gun or _G.Start_Tween_Island or _G.Auto_Next_Island or _G.Auto_Kill_Law then
                for _, v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
                    if v:IsA("BasePart") then
                        v.CanCollide = false    
                    end
                end
            end
        end)
    end)
end)
function CheckNearestTeleporter(aI)
    local MyLevel = game.Players.LocalPlayer.Data.Level.Value
    vcspos = aI.Position
    min = math.huge
    min2 = math.huge
    local y = game.PlaceId
    if y == 2753915549 then
        OldWorld = true
    elseif y == 4442272183 then
        NewWorld = true
    elseif y == 7449423635 then
        ThreeWorld = true
    end
    if ThreeWorld then
        TableLocations = {
            ["Caslte On The Sea"] = Vector3.new(-5058.77490234375, 314.5155029296875, -3155.88330078125),
            ["Hydra"] = Vector3.new(5756.83740234375, 610.4240112304688, -253.9253692626953),
            ["Mansion"] = Vector3.new(-12463.8740234375, 374.9144592285156, -7523.77392578125),
            ["Great Tree"] = Vector3.new(28282.5703125, 14896.8505859375, 105.1042709350586),
            ["Ngu1"] = Vector3.new(-11993.580078125, 334.7812805175781, -8844.1826171875),
            ["ngu2"] = Vector3.new(5314.58203125, 25.419387817382812, -125.94227600097656)
        }
    elseif NewWorld then
        TableLocations = {
            ["Mansion"] = Vector3.new(-288.46246337890625, 306.130615234375, 597.9988403320312),
            ["Flamingo"] = Vector3.new(2284.912109375, 15.152046203613281, 905.48291015625),
            ["122"] = Vector3.new(923.21252441406, 126.9760055542, 32852.83203125),
            ["3032"] = Vector3.new(-6508.5581054688, 89.034996032715, -132.83953857422)
        }
    elseif OldWorld then
        TableLocations = {
            ["1"] = Vector3.new(-7894.6201171875, 5545.49169921875, -380.2467346191406),
            ["2"] = Vector3.new(-4607.82275390625, 872.5422973632812, -1667.556884765625),
            ["3"] = Vector3.new(61163.8515625, 11.759522438049316, 1819.7841796875),
            ["4"] = Vector3.new(3876.280517578125, 35.10614013671875, -1939.3201904296875)
        }
    end
    TableLocations2 = {}
    for r, v in pairs(TableLocations) do
        TableLocations2[r] = (v - vcspos).Magnitude
    end
    for r, v in pairs(TableLocations2) do
        if v < min then
            min = v
            min2 = v
        end
    end
    for r, v in pairs(TableLocations2) do
        if v < min then
            min = v
            min2 = v
        end
    end
    for r, v in pairs(TableLocations2) do
        if v <= min then
            choose = TableLocations[r]
        end
    end
    min3 = (vcspos - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
    if min2 <= min3 then
        return choose
    end
end

function requestEntrance(aJ)
    args = {"requestEntrance", aJ}
    game.ReplicatedStorage.Remotes.CommF_:InvokeServer(unpack(args))
    oldcframe = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
    char = game.Players.LocalPlayer.Character.HumanoidRootPart
    char.CFrame = CFrame.new(oldcframe.X, oldcframe.Y + 50, oldcframe.Z)
    task.wait(0.5)
end

function AntiLowHealth(aK)
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =
        CFrame.new(
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,
        aK,
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z
    )
    wait()
end
PanicMode = true
IngoreY = true
TweenSpeed = 325
function topos(aL)
    pcall(function()
    print("1")
            if game:GetService("Players").LocalPlayer and game:GetService("Players").LocalPlayer.Character and game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") and game:GetService("Players").LocalPlayer.Character:FindFirstChild("HumanoidRootPart") and  game:GetService("Players").LocalPlayer.Character.Humanoid.Health > 0 and game:GetService("Players").LocalPlayer.Character.HumanoidRootPart then
                if not TweenSpeed then
                    TweenSpeed = 325
                end
                DefualtY = aL.Y
                TargetY = aL.Y
                targetCFrameWithDefualtY = CFrame.new(aL.X, DefualtY, aL.Z)
                targetPos = aL.Position
                oldcframe = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
                Distance = (targetPos - game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).Magnitude
                if Distance <= 300 then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = aL
                end
                local aM = CheckNearestTeleporter(aL)
                if aM then
                    pcall(function()
                            tween:Cancel()
                        end)
                    requestEntrance(aM)
                end
                b1 = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,DefualtY,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
                if IngoreY and (b1.Position - targetCFrameWithDefualtY.Position).Magnitude > 5 then
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,DefualtY,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
                    local tweenfunc = {}
                    local aN = game:service "TweenService"
                    local aO =
                        TweenInfo.new((targetPos -game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).Magnitude /TweenSpeed,Enum.EasingStyle.Linear)
                    tween = aN:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"],aO,{CFrame = targetCFrameWithDefualtY})
                    tween:Play()
                    function tweenfunc:Stop()
                        tween:Cancel()
                    end
                    tween.Completed:Wait()
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,TargetY,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
                else
                    local tweenfunc = {}
                    local aN = game:service "TweenService"
                    local aO =
                        TweenInfo.new((targetPos -game:GetService("Players").LocalPlayer.Character:WaitForChild("HumanoidRootPart").Position).Magnitude /TweenSpeed,Enum.EasingStyle.Linear)
                    tween = aN:Create(game:GetService("Players").LocalPlayer.Character["HumanoidRootPart"],aO,{CFrame = aL})
                    tween:Play()
                    function tweenfunc:Stop()
                        tween:Cancel()
                    end
                    tween.Completed:Wait()
                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.X,TargetY,game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame.Z)
                end
                if not tween then
                    return tween
                end
                return tweenfunc
            end
        end)
end
function CancelTween(tween)
		if not tween then
			tween:Cancel()
			_G.StopTween = true
			_G.UseSkill = false
			wait(0.2)
			_G.StopTween = false
			_G.Clip = false
		end
	end
local Library = loadstring(game:HttpGet("https://pastebin.com/raw/frKsq2Nu"))()
local ThemeManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/GhostDuckyy/UI-Libraries/refs/heads/main/LinoriaLib/addons/ThemeManager.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/GhostDuckyy/UI-Libraries/refs/heads/main/LinoriaLib/addons/SaveManager.lua"))()
local Window = Library:CreateWindow({
    Title = 'Attack Hub V1.0.2 [Beta]',
    Center = true,
    AutoShow = true,
    TabPadding = 8
})

local Tabs = {
    Main = Window:AddTab('General'),
    Players = Window:AddTab('Combat'),
    Shop = Window:AddTab('Shop'),
    Raid = Window:AddTab('Raid'),
    Misc = Window:AddTab('Misc'),
    ['Configurations'] = Window:AddTab('Configurations'),
}

local TabBox1 = Tabs.Main:AddLeftTabbox()
local TabBox2 = Tabs.Main:AddRightTabbox()
local Tab3 = Tabs.Main:AddRightGroupbox('   // Automatic \\\\')
local FightingStyle = Tabs.Main:AddRightGroupbox('   // Fighting Style \\\\')

local Teleport = Tabs.Players:AddRightGroupbox('  // Teleport \\\\')
local ESP = Tabs.Players:AddLeftGroupbox('  // ESP \\\\')
local DevilFruit = Tabs.Players:AddLeftGroupbox('  // DevilFruit \\\\')
local RaceV4 = Tabs.Players:AddRightGroupbox('         // Race V4 \\\\')

local Fragment = Tabs.Shop:AddLeftGroupbox('          // Fragment \\\\')
local Abilities = Tabs.Shop:AddLeftGroupbox('         // Abilities \\\\')
local FightingStyleShop = Tabs.Shop:AddLeftGroupbox('        // Fighting Style \\\\')
local Sword = Tabs.Shop:AddRightGroupbox('           // Sword \\\\')
local Gun = Tabs.Shop:AddRightGroupbox('            // Gun \\\\')
local Accessory = Tabs.Shop:AddRightGroupbox('         // Accessory \\\\')

local Raid1 = Tabs.Raid:AddLeftGroupbox('            // Raid \\\\')

local Misc1 = Tabs.Misc:AddLeftGroupbox('            // Misc \\\\')
local Misc2 = Tabs.Misc:AddLeftGroupbox('         // FrameRate \\\\')
local Misc3 = Tabs.Misc:AddLeftGroupbox('         // Players \\\\')
local Misc4 = Tabs.Misc:AddRightGroupbox('         // Server Job \\\\')
local Misc5 = Tabs.Misc:AddRightGroupbox('          // Settings \\\\')
local Misc6 = Tabs.Misc:AddRightGroupbox('           // Limit \\\\')

local Tab1 = TabBox1:AddTab('Main')
local Tab2 = TabBox1:AddTab('Mastery')

local Setting = TabBox2:AddTab('Settings')
local Stats = TabBox2:AddTab('Stats')

Setting:AddLabel(' // Settings \\\\')
Stats:AddLabel(' // Stats \\\\')


Tab1:AddLabel(' // Main \\\\')
Tab2:AddLabel(' // Mastery \\\\')


Tab1:AddToggle('MyToggle', {
    Text = 'Auto Farm Level',
    Default = false,
    Tooltip = 'ฟาร์ม เวล',

    Callback = function(v)
        _G.Auto_Farm_Level = v
        StopTween(_G.Auto_Farm_Level)
    end
})

spawn(function()
	while task.wait() do
		if _G.Auto_Farm_Level then
			pcall(function()
				CheckQuest()
				if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
					if _G.Insant_TP then
						if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude > 2500 then
							BTP(CFrameQ)
						elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude < 2500 then
							Tween(CFrameQ)
						end
					else
						Tween(CFrameQ)
					end
					if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
					end
				elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
							if v.Name == Ms then
								repeat wait()
									BringMob = true
									AutoHaki()
									EquipTool(_G.SelectWeapon)
yakmefan()
									Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
									v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
									v.HumanoidRootPart.Transparency = 1
									v.Humanoid.JumpPower = 0
									v.Humanoid.WalkSpeed = 0
									v.HumanoidRootPart.CanCollide = false
									FarmPos = v.HumanoidRootPart.CFrame
									MonFarm = v.Name
								until not _G.Auto_Farm_Level or not v.Parent or v.Humanoid.Health <= 0 or not game:GetService("Workspace").Enemies:FindFirstChild(v.Name) or game.Players.LocalPlayer.PlayerGui.Main.Quest.Visible == false
								BringMob = false
							end   
						end
					end
					for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].EnemySpawns:GetChildren()) do
						if string.find(v.Name,NameMon) then
							if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v.Position).Magnitude >= 10 then
								Tween(v.CFrame * CFrame.new(0,30,0))
							end
						end
					end
				end
			end)
		end
	end
end)

Tab1:AddToggle('MyToggle', {
    Text = 'Auto Farm Enemy',
    Default = false,
    Tooltip = 'ฟาร์ม มอน รอบ',

    Callback = function(v)
        _G.NeareastFarm = v
        StopTween(_G.NeareastFarm)
    end
})


spawn(function()
	while wait(.1) do
		if _G.NeareastFarm then
			pcall(function()
				for i,v in pairs (game.Workspace.Enemies:GetChildren()) do
					if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
						if v.Name then
							if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - v:FindFirstChild("HumanoidRootPart").Position).Magnitude <= 5000 then
								repeat wait()
									
									BringMob = true
									AutoHaki()
									EquipTool(_G.SelectWeapon)
yakmefan()
									Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,30,0))
									v.HumanoidRootPart.Size = Vector3.new(1, 1, 1)
									v.HumanoidRootPart.Transparency = 1
									v.Humanoid.JumpPower = 0
									v.Humanoid.WalkSpeed = 0
									v.HumanoidRootPart.CanCollide = false
									FarmPos = v.HumanoidRootPart.CFrame
									MonFarm = v.Name
								until not _G.NeareastFarm or not v.Parent or v.Humanoid.Health <= 0 or not game.Workspace.Enemies:FindFirstChild(v.Name)
								BringMob = false
							end
						end
					end
				end
			end)
		end
	end
end)
if World1 then 
Tab1:AddToggle('MyToggle', {
        Text = 'Auto Next Sea',
        Default = false,
        Tooltip = 'Auto New World',
        Callback = function(v)
            _G.AutoSecondSea = v
            StopTween(_G.AutoSecondSea)
        end
    })

    spawn(function()
        while wait() do 
            if _G.AutoSecondSea then
                pcall(function()
                    local MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
                        if MyLevel >= 700 and World1 then
                            if game:GetService("Workspace").Map.Ice.Door.CanCollide == false and game:GetService("Workspace").Map.Ice.Door.Transparency == 1 then
                                local CFrame1 = CFrame.new(4849.29883, 5.65138149, 719.611877)
                                repeat Tween(CFrame1) wait() until (CFrame1.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or _G.AutoSecondSea == false
                                wait(1.1)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress","Detective")
                                wait(0.5)
                                EquipTool("Key")
                                repeat Tween(CFrame.new(1347.7124, 37.3751602, -1325.6488)) wait() until (Vector3.new(1347.7124, 37.3751602, -1325.6488)-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or _G.AutoSecondSea == false
                                wait(0.5)
                            else
                                if game:GetService("Workspace").Map.Ice.Door.CanCollide == false and game:GetService("Workspace").Map.Ice.Door.Transparency == 1 then
                                    if game:GetService("Workspace").Enemies:FindFirstChild("Ice Admiral") then
                                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                            if v.Name == "Ice Admiral" then
                                                if not v.Humanoid.Health <= 0 then
                                                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                                        repeat task.wait()
                                                            AutoHaki()
                                                            EquipTool(_G.SelectWeapon)
yakmefan()
                                                            v.HumanoidRootPart.CanCollide = false
                                                            v.Humanoid.WalkSpeed = 0
                                                            v.Head.CanCollide = false
                                                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                            
                                                            FarmPos = v.HumanoidRootPart.CFrame
									                        MonFarm = v.Name
                                                            Tween(v.HumanoidRootPart.CFrame * CFrame.new(5,10,7))
                                                            sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                                        until not _G.AutoSecondSea or not v.Parent or v.Humanoid.Health <= 0
                                                    end
                                                else 
                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
                                                end
                                            end
                                        end
                                    else
                                        if game:GetService("ReplicatedStorage"):FindFirstChild("Ice Admiral") then
                                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Ice Admiral").HumanoidRootPart.CFrame * CFrame.new(5,10,7))
                                        end
                                    end
                                end
                            end
                        end
                    end)
                end
            end
        end)
elseif World1 then
        Tab1:AddToggle('MyToggle', {
            Text = 'Auto Next Sea',
            Default = false,
            Tooltip = 'Auto Third Sea',
        
            Callback = function(v)
                _G.AutoThirdSea = v
                StopTween(_G.AutoThirdSea)
            end
        })

    spawn(function()
        while wait() do
            if _G.AutoThirdSea then
                pcall(function()
                    if game:GetService("Players").LocalPlayer.Data.Level.Value >= 1500 and World2 then
                        _G.AutoFarm = false
                        if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ZQuestProgress","Check") == 0 then
                            Tween(CFrame.new(-1926.3221435547, 12.819851875305, 1738.3092041016))
                                if (CFrame.new(-1926.3221435547, 12.819851875305, 1738.3092041016).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 10 then
                                    wait(1.5)
                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ZQuestProgress","Begin")
                                end
                                wait(1.8)
                                if game:GetService("Workspace").Enemies:FindFirstChild("rip_indra") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "rip_indra" then
                                            repeat task.wait()
                                                AutoHaki()
                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                                
                                                PosMon = v.HumanoidRootPart.CFrame
                                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                v.HumanoidRootPart.CanCollide = false
                                                v.Humanoid.WalkSpeed = 0
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
                                                sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                            until _G.AutoThirdSea == false or v.Humanoid.Health <= 0 or not v.Parent
                                        end
                                    end
                                elseif not game:GetService("Workspace").Enemies:FindFirstChild("rip_indra") and (CFrame.new(-26880.93359375, 22.848554611206, 473.18951416016).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1000 then
                                    Tween(CFrame.new(-26880.93359375, 22.848554611206, 473.18951416016))
                            end
                        end
                    end
                end)
            end
        end
    end)
end
Tab1:AddDivider()

Tab1:AddLabel('  // Elite Hunter \\\\')

Tab1:AddToggle('MyToggle', {
    Text = 'Auto Farm Elite Hunter',
    Default = false,
    Tooltip = 'Auto Farm Elite Hunter',

    Callback = function(v)
        _G.AutoElitehunter = v
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
        StopTween(_G.AutoElitehunter)
    end
})

Tab1:AddToggle('MyToggle', {
    Text = 'Auto Farm Elite Hunter Hop',
    Default = false,
    Tooltip = 'Auto Farm Elite Hunter Hop',

    Callback = function(v)
        _G.AutoEliteHunterHop = v
    end
})

spawn(function()
    while wait() do
        if _G.AutoElitehunter and World3 then
            pcall(function()
                local QuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                    repeat  wait()
                        Tween(CFrame.new(-5418.892578125, 313.74130249023, -2826.2260742188)) 
                    until not _G.AutoElitehunter or (Vector3.new(-5418.892578125, 313.74130249023, -2826.2260742188)-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3
                    if (Vector3.new(-5418.892578125, 313.74130249023, -2826.2260742188)-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                        wait(1.1)
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter")
                        wait(0.5)
                    end
                elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                    if string.find(QuestTitle,"Diablo") or string.find(QuestTitle,"Deandre") or string.find(QuestTitle,"Urban") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Diablo") or game:GetService("Workspace").Enemies:FindFirstChild("Deandre") or game:GetService("Workspace").Enemies:FindFirstChild("Urban") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Diablo" or v.Name == "Deandre" or v.Name == "Urban" then
                                    if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                        repeat task.wait()
                                            AutoHaki()
                                            
                                            EquipTool(_G.SelectWeapon)
yakmefan()
                                            v.HumanoidRootPart.CanCollide = false
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                            Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                            sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                        until _G.AutoElitehunter == false or v.Humanoid.Health <= 0 or not v.Parent
                                    end
                                end
                            end
                        else
                            if game:GetService("ReplicatedStorage"):FindFirstChild("Diablo") then
                                Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Diablo").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            elseif game:GetService("ReplicatedStorage"):FindFirstChild("Deandre") then
                                Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Deandre").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            elseif game:GetService("ReplicatedStorage"):FindFirstChild("Urban") then
                                Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Urban").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            else
                                if _G.AutoEliteHunterHop and not game:GetService("ReplicatedStorage"):FindFirstChild("Urban") and not game:GetService("ReplicatedStorage"):FindFirstChild("Deandre") and not game:GetService("ReplicatedStorage"):FindFirstChild("Diablo") then
                                    Hop()
                                else
                                    Tween(CFrame.new(-5418.892578125, 313.74130249023, -2826.2260742188))
                                end
                            end
                        end                    
                    end
                end
            end)
        end
    end
end)




Tab1:AddDivider()

    Tab1:AddLabel('  // Bone \\\\')

    Tab1:AddToggle('MyToggle', {
        Text = 'Auto Farm [Bones]',
        Default = false,
        Tooltip = 'Auto Farm Bone',
    
        Callback = function(v)
            _G.Auto_Bone = v
            StopTween(_G.Auto_Bone)
        end
    })


    spawn(function()
        while wait() do 
            if _G.Auto_Bone and World3 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Reborn Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Living Zombie") or game:GetService("Workspace").Enemies:FindFirstChild("Demonic Soul") or game:GetService("Workspace").Enemies:FindFirstChild("Posessed Mummy") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Reborn Skeleton" or v.Name == "Living Zombie" or v.Name == "Demonic Soul" or v.Name == "Posessed Mummy" then
                               if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                   repeat task.wait()
                                        AutoHaki()
                                        
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.Head.CanCollide = false 
                                        BringMob = true
                                        FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                    until not _G.Auto_Bone or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                        Tween(CFrame.new(-9466.72949, 171.162918, 6132.01514))
                        BringMob = false
                        for i,v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do 
                            if v.Name == "Reborn Skeleton" then
                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            elseif v.Name == "Living Zombie" then
                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            elseif v.Name == "Demonic Soul" then
                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            elseif v.Name == "Posessed Mummy" then
                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                            end
                        end
                    end
                end)
            end
        end
    end)    


    Tab1:AddToggle('MyToggle', {
        Text = 'Auto Random Bones',
        Default = false,
        Tooltip = 'Auto Random Bone',
    
        Callback = function(v)
            _G.Auto_Random_Bone = v
        end
    })

    
spawn(function()
	pcall(function()
		while wait(.1) do
			if _G.Auto_Random_Bone then    
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones","Buy",1,1)
			end
		end
	end)
end)
    






    Tab1:AddToggle('MyToggle', {
        Text = 'Auto Cake Prince',
        Default = false,
        Tooltip = 'Auto Cake Prince',
    
        Callback = function(v)
            _G.AutoDoughtBoss = v
	        StopTween(_G.AutoDoughtBoss)
        end
    })


    spawn(function()
        while wait() do
            if _G.AutoDoughtBoss then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Cake Prince" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not _G.AutoDoughtBoss or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Cake Prince") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Cake Prince").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if KillMob == 0 then
                            end                    
                            if game:GetService("Workspace").Map.CakeLoaf.BigMirror.Other.Transparency == 1 then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Cookie Crafter") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Guard") or game:GetService("Workspace").Enemies:FindFirstChild("Baking Staff") or game:GetService("Workspace").Enemies:FindFirstChild("Head Baker") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Cookie Crafter" or v.Name == "Cake Guard" or v.Name == "Baking Staff" or v.Name == "Head Baker" then
                                            if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                                repeat task.wait()
                                                    AutoHaki()
                                                    EquipTool(_G.SelectWeapon)
yakmefan()
                                                    v.HumanoidRootPart.CanCollide = false
                                                    v.Humanoid.WalkSpeed = 0
                                                    v.Head.CanCollide = false 
                                                    v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                    BringMob = true
                                                    FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                                    game:GetService("VirtualUser"):CaptureController()
                                                    game:GetService("VirtualUser"):Button1Down(Vector2.new(1280,672))
                                                until not _G.AutoDoughtBoss or not v.Parent or v.Humanoid.Health <= 0 or game:GetService("Workspace").Map.CakeLoaf.BigMirror.Other.Transparency == 0 or game:GetService("ReplicatedStorage"):FindFirstChild("Cake Prince") or game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince") or KillMob == 0
                                            end
                                        end
                                    end
                                else
                                    Tween(CFrame.new(-2091.911865234375, 70.00884246826172, -12142.8359375))
                                    BringMob = false
                                    if game:GetService("ReplicatedStorage"):FindFirstChild("Cookie Crafter") then
                                        Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Cookie Crafter").HumanoidRootPart.CFrame * CFrame.new(2,20,2)) 
                                    else
                                        if game:GetService("ReplicatedStorage"):FindFirstChild("Cake Guard") then
                                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Cake Guard").HumanoidRootPart.CFrame * CFrame.new(2,20,2)) 
                                        else
                                            if game:GetService("ReplicatedStorage"):FindFirstChild("Baking Staff") then
                                                Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Baking Staff").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                            else
                                                if game:GetService("ReplicatedStorage"):FindFirstChild("Head Baker") then
                                                    Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Head Baker").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                                end
                                            end
                                        end
                                    end                       
                                end
                            else
                                if game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince") then
                                    Tween(game:GetService("Workspace").Enemies:FindFirstChild("Cake Prince").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                else
                                    if game:GetService("ReplicatedStorage"):FindFirstChild("Cake Prince") then
                                        Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Cake Prince").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                    end
                                end
                            end
                        end
                    end
                end)
            end
        end
    end)



    Tab1:AddDivider()
    Tab1:AddLabel('           // Event \\\\')

    Tab1:AddToggle('MyToggle', {
        Text = 'Auto Ectoplasm',
        Default = false,
        Tooltip = 'Auto Ectoplasm',
    
        Callback = function(v)
            _G.Auto_Ectoplasm = v
        end
    })




Tab2:AddToggle('MyToggle', {
    Text = 'Auto Farm Observation',
    Default = false,
    Tooltip = 'Auto Farm Observation',

    Callback = function(v)
        _G.AutoObservation  = v
        StopTween(_G.AutoObservation)
    end
})

spawn(function()
    while wait() do
        pcall(function()
            if _G.AutoObservation then
                repeat task.wait()
                    if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                        game:GetService('VirtualUser'):CaptureController()
                        game:GetService('VirtualUser'):SetKeyDown('0x65')
                        wait(2)
                        game:GetService('VirtualUser'):SetKeyUp('0x65')
                    end
                until game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") or not _G.AutoObservation
            end
        end)
    end
end)


spawn(function()
    pcall(function()
        while wait() do
            if _G.AutoObservation then
                if game:GetService("Players").LocalPlayer.VisionRadius.Value >= 3000 then
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://0";
                        Title = "Observation", 
                        Text = "You Have Max Points"
                    })
                    wait(2)
                else
                    if World2 then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Lava Pirate") then
                            if game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                                repeat task.wait()
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Enemies:FindFirstChild("Lava Pirate").HumanoidRootPart.CFrame * CFrame.new(3,0,0)
                                until _G.AutoObservation == false or not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                            else
                                repeat task.wait()
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Enemies:FindFirstChild("Lava Pirate").HumanoidRootPart.CFrame * CFrame.new(0,50,0)+
                                        wait(1)
                                    if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") and _G.AutoObservation_Hop == true then
                                        game:GetService("TeleportService"):Teleport(game.PlaceId,game:GetService("Players").LocalPlayer)
                                    end
                                until _G.AutoObservation == false or game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                            end
                        else
                            Tween(CFrame.new(-5478.39209, 15.9775667, -5246.9126))
                        end
                    elseif World1 then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Galley Captain") then
                            if game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                                repeat task.wait()
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Enemies:FindFirstChild("Galley Captain").HumanoidRootPart.CFrame * CFrame.new(3,0,0)
                                until _G.AutoObservation == false or not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                            else
                                repeat task.wait()
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Enemies:FindFirstChild("Galley Captain").HumanoidRootPart.CFrame * CFrame.new(0,50,0)
                                    wait(1)
                                    if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") and _G.AutoObservation_Hop == true then
                                        game:GetService("TeleportService"):Teleport(game.PlaceId,game:GetService("Players").LocalPlayer)
                                    end
                                until _G.AutoObservation == false or game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                            end
                        else
                            Tween(CFrame.new(5533.29785, 88.1079102, 4852.3916))
                        end
                    elseif World3 then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Giant Islander") then
                            if game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") then
                                repeat task.wait()
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Enemies:FindFirstChild("Giant Islander").HumanoidRootPart.CFrame * CFrame.new(3,0,0)
                                until _G.AutoObservation == false or not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                            else
                                repeat task.wait()
                                    game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Enemies:FindFirstChild("Giant Islander").HumanoidRootPart.CFrame * CFrame.new(0,50,0)
                                    wait(1)
                                    if not game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel") and _G.AutoObservation_Hop == true then
                                        game:GetService("TeleportService"):Teleport(game.PlaceId,game:GetService("Players").LocalPlayer)
                                    end
                                until _G.AutoObservation == false or game:GetService("Players").LocalPlayer.PlayerGui.ScreenGui:FindFirstChild("ImageLabel")
                            end
                        else
                            Tween(CFrame.new(4530.3540039063, 656.75695800781, -131.60952758789))
                        end
                    end
                end
            end
        end
    end)
end)

function EquipToolSword()
	pcall(function()
		for i,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
			if v.ToolTip == "Sword" and v:IsA('Tool') then
				local ToolHumanoid = game.Players.LocalPlayer.Backpack:FindFirstChild(v.Name) 
				game.Players.LocalPlayer.Character.Humanoid:EquipTool(ToolHumanoid) 
			end
		end
	end)
end

spawn(function()
	local gg = getrawmetatable(game)
	local old = gg.__namecall
	setreadonly(gg,false)
	gg.__namecall = newcclosure(function(...)
		local method = getnamecallmethod()
		local args = {
			...
		}
		if tostring(method) == "FireServer" then
			if tostring(args[1]) == "RemoteEvent" then
				if tostring(args[2]) ~= "true" and tostring(args[2]) ~= "false" then
					if _G.UseSkill then
						if type(args[2]) == "vector" then
							args[2] = PositionSkillMasteryDevilFruit
						else
							args[2] = CFrame.new(PositionSkillMasteryDevilFruit)
						end
						return old(unpack(args))
					end
				end
			end
		end
		return old(...)
	end)
end)

spawn(function()
	pcall(function()
		while task.wait() do
			for i,v in pairs(game:GetService("Players").LocalPlayer.Backpack:GetChildren()) do
				if v:IsA("Tool") then
					if v:FindFirstChild("RemoteFunctionShoot") then
						CurrentEquipGun = v.Name
					end
				end
			end
		end
	end)
end)

Tab2:AddToggle('MyToggle', {
    Text = 'Auto Farm Fruit Mastery',
    Default = false,
    Tooltip = 'Auto Farm Fruit Mastery',

    Callback = function(v)
        _G.AutoFarmMasDevilFruit = v
    end
})


spawn(function()
	while task.wait(.1) do
		if _G.AutoFarmMasDevilFruit then
			pcall(function()
				CheckQuest()
				if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
					if _G.Insant_TP then
						if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude > 2500 then
							BTP(CFrameQ)
							wait(0.2)
						elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude < 2500 then
							Tween(CFrameQ)
						end
					else
						Tween(CFrameQ)
					end
					if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
					end
				elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
							if v.Name == Ms then
								repeat game:GetService("RunService").Heartbeat:wait()
									if v.Humanoid.Health <= v.Humanoid.MaxHealth * _G.KillPercent / 100 then
										_G.UseSkill = true
										_G.Fast_Delay = 0.195
										EquipTool(game:GetService("Players").LocalPlayer.Data.DevilFruit.Value)
									else
										_G.UseSkill = false
										AutoHaki()
										BringMob = true
										_G.Fast_Delay = 0.195
										EquipTool(_G.SelectWeapon)
yakmefan()
										Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
										v.HumanoidRootPart.Size = Vector3.new(1, 1, 1)
										v.HumanoidRootPart.Transparency = 1
										v.Humanoid.JumpPower = 0
										v.Humanoid.WalkSpeed = 0
										v.HumanoidRootPart.CanCollide = false
										FarmPos = v.HumanoidRootPart.CFrame
										MonFarm = v.Name
									end
								until not _G.AutoFarmMasDevilFruit or not v.Parent or v.Humanoid.Health == 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false or not game:GetService("Workspace").Enemies:FindFirstChild(v.Name) or not TypeMastery == 'Level'
								BringMob = false
								_G.UseSkill = false

							end
						end
					end
				end
			end)
        end
    end
end)
Tab2:AddToggle('MyToggle', {
    Text = 'Auto Farm Gun Mastery',
    Default = false,
    Tooltip = 'Auto Farm Gun Mastery ',

    Callback = function(v)
        _G.AutoFarmMasGun = v
    end
})
spawn(function()
	while task.wait(.1) do
		if _G.AutoFarmMasGun then
			pcall(function()
				CheckQuest()
				if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
					if _G.Insant_TP then
						if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude > 2500 then
							BTP(CFrameQ)
							wait(0.2)
						elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude < 2500 then
							Tween(CFrameQ)
						end
					else
						Tween(CFrameQ)
					end
					if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
					end
				elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
							if v.Name == Ms then
								repeat game:GetService("RunService").Heartbeat:wait()
									if v.Humanoid.Health <= v.Humanoid.MaxHealth * _G.KillPercent / 100 then
										_G.UseSkill = true
										_G.Fast_Delay = 0.175
										EquipTool(CurrentEquipGun)
									else
										_G.UseSkill = false
										AutoHaki()
										BringMob = true
										_G.Fast_Delay = 0.175
										EquipTool(_G.SelectWeapon)
yakmefan()
										Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
										v.HumanoidRootPart.Size = Vector3.new(1, 1, 1)
										v.HumanoidRootPart.Transparency = 1
										v.Humanoid.JumpPower = 0
										v.Humanoid.WalkSpeed = 0
										v.HumanoidRootPart.CanCollide = false
										FarmPos = v.HumanoidRootPart.CFrame
										MonFarm = v.Name
									end
								until not _G.AutoFarmMasGun or not v.Parent or v.Humanoid.Health == 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false or not game:GetService("Workspace").Enemies:FindFirstChild(v.Name) or not TypeMastery == 'Level'
								BringMob = false
								_G.UseSkill = false

							end
						end
					end
				end
			end)
        end
    end
end)
Tab2:AddToggle('MyToggle', {
    Text = 'Auto Farm Sword Mastery',
    Default = false,
    Tooltip = 'Auto Farm Sword Mastery',

    Callback = function(v)
        _G.AutoFarmMasSword = v
    end
})
spawn(function()
	while task.wait(.1) do
		if _G.AutoFarmMasSword then
			pcall(function()
				CheckQuest()
				if not string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
					game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
					if _G.Insant_TP then
						if (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude > 2500 then
							BTP(CFrameQ)
							wait(0.2)
						elseif (game.Players.LocalPlayer.Character.HumanoidRootPart.Position - CFrameQ.Position).Magnitude < 2500 then
							Tween(CFrameQ)
						end
					else
						Tween(CFrameQ)
					end
					if (CFrameQ.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5 then
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,QuestLv)
					end
				elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
							if v.Name == Ms then
								repeat game:GetService("RunService").Heartbeat:wait()
									if v.Humanoid.Health <= v.Humanoid.MaxHealth * _G.KillPercent / 100 then
										_G.UseSkill = true
										_G.Fast_Delay = 0.175
										EquipTool(EquipToolSword)
									else
										_G.UseSkill = false
										_G.Fast_Delay = 0.175
										AutoHaki()
										BringMob = true
										EquipTool(_G.SelectWeapon)
yakmefan()
										Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
										v.HumanoidRootPart.Size = Vector3.new(1, 1, 1)
										v.HumanoidRootPart.Transparency = 1
										v.Humanoid.JumpPower = 0
										v.Humanoid.WalkSpeed = 0
										v.HumanoidRootPart.CanCollide = false
										FarmPos = v.HumanoidRootPart.CFrame
										MonFarm = v.Name
									end
								until not _G.AutoFarmMasSword or not v.Parent or v.Humanoid.Health == 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false or not game:GetService("Workspace").Enemies:FindFirstChild(v.Name) or not TypeMastery == 'Level'
								BringMob = false
								_G.UseSkill = false
							end
						end
					end
				end
			end)
        end 
    end
end)

Tab2:AddDivider()

Tab2:AddLabel('    // Setting Mastery \\\\')

Tab2:AddSlider('MySlider', {
    Text = 'Kill At (%)',
    Default = 25,
    Min = 0,
    Max = 100,
    Rounding = 0,
    Compact = false,

    Callback = function(v)
        _G.KillPercent = v
    end
})

Tab2:AddToggle('MyToggle', {
    Text = 'Skill Z',
    Default = true,
    Tooltip = 'Skill Z',

    Callback = function(v)
        _G.SkillZ = v
    end
})
Tab2:AddToggle('MyToggle', {
    Text = 'Skill X',
    Default = true,
    Tooltip = 'Skill X',

    Callback = function(v)
        _G.SkillX = v
    end
})
Tab2:AddToggle('MyToggle', {
    Text = 'Skill C',
    Default = true,
    Tooltip = 'Skill C',

    Callback = function(v)
        _G.SkillC = v
    end
})
Tab2:AddToggle('MyToggle', {
    Text = 'Skill V',
    Default = true,
    Tooltip = 'Skill V',

    Callback = function(v)
        _G.SkillV = v
    end
})
Tab2:AddToggle('MyToggle', {
    Text = 'Skill F',
    Default = true,
    Tooltip = 'Skill F',

    Callback = function(v)
        _G.SkillF = v
    end
})
spawn(function()
	while task.wait(1) do
		if _G.UseSkill then
			pcall(function()
				if _G.UseSkill then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v.Name == MonFarm and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health <= v.Humanoid.MaxHealth * _G.KillPercent / 100 then
							repeat game:GetService("RunService").Heartbeat:wait()
								EquipTool(game.Players.LocalPlayer.Data.DevilFruit.Value)
								Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,10,0))
								PositionSkillMasteryDevilFruit = v.HumanoidRootPart.Position
								if game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value) then
									game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value).MousePos.Value = PositionSkillMasteryDevilFruit
									local DevilFruitMastery = game:GetService("Players").LocalPlayer.Character:FindFirstChild(game.Players.LocalPlayer.Data.DevilFruit.Value).Level.Value
									if _G.SkillZ and DevilFruitMastery >= 1 then
										game:service('VirtualInputManager'):SendKeyEvent(true, "Z", false, game)
										wait(0.1)
										game:service('VirtualInputManager'):SendKeyEvent(false, "Z", false, game)
									end
									if _G.SkillX and DevilFruitMastery >= 2 then
										game:service('VirtualInputManager'):SendKeyEvent(true, "X", false, game)
										wait(0.2)
										game:service('VirtualInputManager'):SendKeyEvent(false, "X", false, game)
									end
									if _G.SkillC and DevilFruitMastery >= 3 then
										game:service('VirtualInputManager'):SendKeyEvent(true, "C", false, game)
										wait(0.3)
										game:service('VirtualInputManager'):SendKeyEvent(false, "C", false, game)
									end
									if _G.SkillV and DevilFruitMastery >= 4 then
										game:service('VirtualInputManager'):SendKeyEvent(true, "V", false, game)
										wait(0.4)
										game:service('VirtualInputManager'):SendKeyEvent(false, "V", false, game)
									end
									if _G.SkillF and DevilFruitMastery >= 5 then
										game:GetService("VirtualInputManager"):SendKeyEvent(true, "F", false, game)
										wait(0.5)
										game:GetService("VirtualInputManager"):SendKeyEvent(false, "F", false, game)
									end
								end
							until not AutoFarmMasDevilFruit or not _G.UseSkill or v.Humanoid.Health == 0
						end
					end
				end
			end)
		end
	end
end)
if World1 then 
    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Saber',
        Default = false,
        Tooltip = 'Auto Saber',
    
        Callback = function(v)
            _G.Auto_Saber = v
        end
    })


    spawn(function()
        while wait() do
            if _G.AutoSaber then
                if game.Players.localPlayer.Data.Level.Value < 200 then
                else
                    if game.Workspace.Map.Jungle.Final.Part.CanCollide == false then
                        if _G.AutoSaber and game.ReplicatedStorage:FindFirstChild("Saber Expert") or game.Workspace.Enemies:FindFirstChild("Saber Expert") then
                            if game.Workspace.Enemies:FindFirstChild("Saber Expert") then
                                for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                                    if v.Name == "Saber Expert" and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                                        repeat wait()
                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                Farmtween = Tween(v.HumanoidRootPart.Position,v.HumanoidRootPart.CFrame)
                                            elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Farmtween then
                                                    Farmtween:Stop()
                                                end
                                                AutoHaki()
                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)
                                                
                                            end
                                        until not _G.Auto_Saber or not v.Parent or v.Humanoid.Health <= 0
                                    end
                                end
                            else
                                Questtween = Tween(CFrame.new(-1405.41956, 29.8519993, 5.62435055).Position,CFrame.new(-1405.41956, 29.8519993, 5.62435055))
                                if (CFrame.new(-1405.41956, 29.8519993, 5.62435055).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                    if Questtween then
                                        Questtween:Stop()
                                    end
                                    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1405.41956, 29.8519993, 5.62435055, 0.885240912, 3.52892613e-08, 0.465132833, -6.60881128e-09, 1, -6.32913171e-08, -0.465132833, 5.29540891e-08, 0.885240912)
                                end
                            end
                        else
                            if _G.AutoSaberHop then
                                Hop()
                            end
                        end
                    elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Relic") or game.Players.LocalPlayer.Character:FindFirstChild("Relic") and game.Players.localPlayer.Data.Level.Value >= 200 then
                        EquipTool("Relic")
                        wait(0.5)
                        Questtween = Tween(CFrame.new(-1405.41956, 29.8519993, 5.62435055).Position,CFrame.new(-1405.41956, 29.8519993, 5.62435055))
                        if (CFrame.new(-1405.41956, 29.8519993, 5.62435055).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                            if Questtween then
                                Questtween:Stop()
                            end
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1405.41956, 29.8519993, 5.62435055, 0.885240912, 3.52892613e-08, 0.465132833, -6.60881128e-09, 1, -6.32913171e-08, -0.465132833, 5.29540891e-08, 0.885240912)
                        end
                    else
                        if Workspace.Map.Jungle.QuestPlates.Door.CanCollide == false then
                            if game.Workspace.Map.Desert.Burn.Part.CanCollide == false then
                                if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress","SickMan") == 0 then
                                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress","RichSon") == 0 then
                                        if game.Workspace.Enemies:FindFirstChild("Mob Leader [Lv. 120] [Boss]") then
                                            for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                                                if _G.AutoSaber and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and v.Name == "Mob Leader [Lv. 120] [Boss]" then
                                                    repeat
                                                        pcall(function() wait() 
                                                            if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude > 300 then
                                                                Farmtween = Tween(v.HumanoidRootPart.Position,v.HumanoidRootPart.CFrame)
                                                            elseif (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                                if Farmtween then
                                                                    Farmtween:Stop()
                                                                end
                                                                AutoHaki()
                                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                                if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                                                    local args = {
                                                                        [1] = "Buso"
                                                                    }
                                                                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                                                end
                                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame * CFrame.new(0, 30, 0)
                                                               
                                                            end
                                                        end)
                                                    until not _G.AutoSaber or not v.Parent or v.Humanoid.Health <= 0
                                                end
                                            end
                                        else
                                            Questtween = Tween(CFrame.new(-2848.59399, 7.4272871, 5342.44043).Position,CFrame.new(-2848.59399, 7.4272871, 5342.44043))
                                            if (CFrame.new(-2848.59399, 7.4272871, 5342.44043).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Questtween then
                                                    Questtween:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-2848.59399, 7.4272871, 5342.44043, -0.928248107, -8.7248246e-08, 0.371961564, -7.61816636e-08, 1, 4.44474857e-08, -0.371961564, 1.29216433e-08, -0.928248107)
                                            end
                                        end
                                    elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress","RichSon") == 1 then
                                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Relic") or game.Players.LocalPlayer.Character:FindFirstChild("Relic") then
                                            EquipTool("Relic")
                                            wait(0.5)
                                            Questtween = Tween(CFrame.new(-1405.41956, 29.8519993, 5.62435055).Position,CFrame.new(-1405.41956, 29.8519993, 5.62435055))
                                            if (CFrame.new(-1405.41956, 29.8519993, 5.62435055).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Questtween then
                                                    Questtween:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1405.41956, 29.8519993, 5.62435055)
                                            end
                                        else
                                            Questtween = Tween(CFrame.new(-910.979736, 13.7520342, 4078.14624).Position,CFrame.new(-910.979736, 13.7520342, 4078.14624))
                                            if (CFrame.new(-910.979736, 13.7520342, 4078.14624).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Questtween then
                                                    Questtween:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-910.979736, 13.7520342, 4078.14624, 0.00685182028, -1.53155766e-09, -0.999976516, 9.15205245e-09, 1, -1.46888401e-09, 0.999976516, -9.14177267e-09, 0.00685182028)
                                                wait(.5)
                                                local args = {
                                                    [1] = "ProQuestProgress",
                                                    [2] = "RichSon"
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end
                                        end
                                    else
                                        Questtween = Tween(CFrame.new(-910.979736, 13.7520342, 4078.14624).Position,CFrame.new(-910.979736, 13.7520342, 4078.14624))
                                        if (CFrame.new(-910.979736, 13.7520342, 4078.14624).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                            if Questtween then
                                                Questtween:Stop()
                                            end
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-910.979736, 13.7520342, 4078.14624)
                                            local args = {
                                                [1] = "ProQuestProgress",
                                                [2] = "RichSon"
                                            }
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                        end
                                    end
                                else
                                    if game.Players.LocalPlayer.Backpack:FindFirstChild("Cup") or game.Players.LocalPlayer.Character:FindFirstChild("Cup") then
                                        EquipTool("Cup")
                                        if game.Players.LocalPlayer.Character.Cup.Handle:FindFirstChild("TouchInterest") then
                                            Questtween = Tween(CFrame.new(1397.229, 37.3480148, -1320.85217).Position,CFrame.new(1397.229, 37.3480148, -1320.85217))
                                            if (CFrame.new(1397.229, 37.3480148, -1320.85217).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                                if Questtween then
                                                    Questtween:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1397.229, 37.3480148, -1320.85217, -0.11285457, 2.01368788e-08, 0.993611455, 1.91641178e-07, 1, 1.50028845e-09, -0.993611455, 1.90586206e-07, -0.11285457)
                                            end
                                        else
                                            wait(0.5)
                                            if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ProQuestProgress","SickMan") ~= 0 then
                                                local args = {
                                                    [1] = "ProQuestProgress",
                                                    [2] = "SickMan"
                                                }
                                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                                            end
                                        end
                                    else
                                        Questtween = Tween(game.Workspace.Map.Desert.Cup.Position,game.Workspace.Map.Desert.Cup.CFrame)
                                        if (game.Workspace.Map.Desert.Cup.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                            if Questtween then
                                                Questtween:Stop()
                                            end
                                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Map.Desert.Cup.CFrame
                                        end
                                        firetouchinterest(game.Workspace.Map.Desert.Cup.TouchInterest,game.Players.LocalPlayer.Character.Head, 1)
                                    end
                                end
                            else
                                if game.Players.LocalPlayer.Backpack:FindFirstChild("Torch") or game.Players.LocalPlayer.Character:FindFirstChild("Torch") then
                                    EquipTool("Torch")
                                    Questtween = Tween(CFrame.new(1114.87708, 4.9214654, 4349.8501).Position,CFrame.new(1114.87708, 4.9214654, 4349.8501))
                                    if (CFrame.new(1114.87708, 4.9214654, 4349.8501).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                        if Questtween then
                                            Questtween:Stop()
                                        end
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(1114.87708, 4.9214654, 4349.8501, -0.612586915, -9.68697833e-08, 0.790403247, -1.2634203e-07, 1, 2.4638446e-08, -0.790403247, -8.47679615e-08, -0.612586915)
                                    end
                                else
                                    Questtween = Tween(CFrame.new(-1610.00757, 11.5049858, 164.001587).Position,CFrame.new(-1610.00757, 11.5049858, 164.001587))
                                    if (CFrame.new(-1610.00757, 11.5049858, 164.001587).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 300 then
                                        if Questtween then
                                            Questtween:Stop()
                                        end
                                        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-1610.00757, 11.5049858, 164.001587, 0.984807551, -0.167722285, -0.0449818149, 0.17364943, 0.951244235, 0.254912198, 3.42372805e-05, -0.258850515, 0.965917408)
                                    end
                                end
                            end
                        else
                            for i,v in pairs(Workspace.Map.Jungle.QuestPlates:GetChildren()) do
                                if v:IsA("Model") then wait()
                                    if v.Button.BrickColor ~= BrickColor.new("Camo") then
                                        repeat wait()
                                            Questtween = Tween(v.Button.Position,v.Button.CFrame)
                                            if (v.Button.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 150 then
                                                if Questtween then
                                                    Questtween:Stop()
                                                end
                                                game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Button.CFrame
                                            end
                                        until not _G.AutoSaber or v.Button.BrickColor == BrickColor.new("Camo")
                                    end
                                end
                            end    
                        end
                    end
                end 
            end
        end
    end)
    
    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Pole',
        Default = false,
        Tooltip = 'Auto Pole',
    
        Callback = function(v)
            _G.Auto_Pole = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Pole Hop',
        Default = false,
        Tooltip = 'Auto Pole Hop',
    
        Callback = function(v)
            _G.Autopolehop = v
        end
    })

    spawn(function()
        while wait() do
            if  _G.Autopole and World1 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Thunder God") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Thunder God" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.Autopole or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-7748.0185546875, 5606.80615234375, -2305.898681640625))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Thunder God") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Thunder God").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.Autopolehop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Franky',
        Default = false,
        Tooltip = 'Auto Franky',
    
        Callback = function(v)
            _G.Auto_Franky = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Franky Hop',
        Default = false,
        Tooltip = 'Auto_Franky Hop',
    
        Callback = function(v)
            _G.Auto_FrankyHop = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Waden',
        Default = false,
        Tooltip = 'Auto Waden',
    
        Callback = function(v)
            _G.Autowaden = v
            StopTween( _G.Autowaden)
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Waden Hop',
        Default = false,
        Tooltip = 'Auto Waden Hop',
    
        Callback = function(v)
            _G.Autowaden = v
            StopTween( _G.Autowaden)
        end
    })


    spawn(function()
        while wait() do
            if  _G.Autowaden and World1 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Chief Warden") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Chief Warden" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.Autowaden or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(5186.14697265625, 24.86684226989746, 832.1885375976562))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Chief Warden") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Chief Warden").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.Autowadenhop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Greybeard',
        Default = false,
        Tooltip = 'Auto Greybeard',
    
        Callback = function(v)
            _G.Autogay = v
            StopTween( _G.Autogay)
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Greybeard Hop',
        Default = false,
        Tooltip = 'Auto Greybeard Hop',
    
        Callback = function(v)
            _G.Autogayhop = v
        end
    })
    
    spawn(function()
        while wait() do
            if  _G.Autogay and World1 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Greybeard") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Greybeard" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.Autogay or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-5023.38330078125, 28.65203285217285, 4332.3818359375))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Greybeard") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Greybeard").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.Autogayhop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Sharks saw',
        Default = false,
        Tooltip = 'Auto Sharks saw',
    
        Callback = function(v)
            _G.Autosaw = v
            StopTween( _G.Autosaw)
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Sharks saw Hop',
        Default = false,
        Tooltip = 'Auto Sharks saw Hop',
    
        Callback = function(v)
            _G.Autosawhop = v
        end
    })

    
    spawn(function()
        while wait() do
            if  _G.Autosaw and World1 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("The Saw") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "The Saw" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.Autosaw or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-690.33081054688, 15.09425163269, 1582.2380371094))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("The Saw") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("The Saw").HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                        else
                            if  _G.Autosawhop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)
    

elseif World2 then


    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Factory Farm',
        Default = false,
        Tooltip = 'Auto Factory Farm',
    
        Callback = function(v)
            _G.Auto_Factory_Farm = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Factory Farm Hop',
        Default = false,
        Tooltip = 'Auto Factory Farm',
    
        Callback = function(v)
            _G.Auto_Factory_Farm_Hop = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Bartilo Quest',
        Default = false,
        Tooltip = 'Auto Bartilo Quest',
    
        Callback = function(v)
            _G.AutoBartilo = v
            StopTween(_G.AutoBartilo)
        end
    })

    spawn(function()
        pcall(function()
            while wait(.1) do
                if _G.AutoBartilo then
                    if game:GetService("Players").LocalPlayer.Data.Level.Value >= 800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 0 then
                        if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Swan Pirates") and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "50") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then 
                            if game:GetService("Workspace").Enemies:FindFirstChild("Swan Pirate") then
                                Ms = "Swan Pirate"
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == Ms then
                                        pcall(function()
                                            repeat task.wait()
                                                sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRadius", math.huge)
                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                AutoHaki()
                                                v.HumanoidRootPart.Transparency = 1
                                                v.HumanoidRootPart.CanCollide = false
                                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))													
                                                FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                                
                                                BringMob = true
                                            until not v.Parent or v.Humanoid.Health <= 0 or _G.AutoBartilo == false or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                            BringMob = false
                                        end)
                                    end
                                end
                            else
                                repeat Tween(CFrame.new(932.624451, 156.106079, 1180.27466, -0.973085582, 4.55137119e-08, -0.230443969, 2.67024713e-08, 1, 8.47491108e-08, 0.230443969, 7.63147128e-08, -0.973085582)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(932.624451, 156.106079, 1180.27466, -0.973085582, 4.55137119e-08, -0.230443969, 2.67024713e-08, 1, 8.47491108e-08, 0.230443969, 7.63147128e-08, -0.973085582)).Magnitude <= 10
                            end
                        else
                            repeat Tween(CFrame.new(-456.28952, 73.0200958, 299.895966)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-456.28952, 73.0200958, 299.895966)).Magnitude <= 10
                            wait(1.1)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BartiloQuest",1)
                        end 
                    elseif game:GetService("Players").LocalPlayer.Data.Level.Value >= 800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 1 then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Jeremy") then
                            Ms = "Jeremy"
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == Ms then
                                    OldCFrameBartlio = v.HumanoidRootPart.CFrame
                                    repeat task.wait()
                                        sethiddenproperty(game:GetService("Players").LocalPlayer, "SimulationRadius", math.huge)
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        AutoHaki()
                                        v.HumanoidRootPart.Transparency = 1
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        v.HumanoidRootPart.CFrame = OldCFrameBartlio
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        game:GetService'VirtualUser':CaptureController()
                                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    until not v.Parent or v.Humanoid.Health <= 0 or _G.AutoBartilo == false
                                end
                            end
                        elseif game:GetService("ReplicatedStorage"):FindFirstChild("Jeremy") then
                            repeat Tween(CFrame.new(-456.28952, 73.0200958, 299.895966)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-456.28952, 73.0200958, 299.895966)).Magnitude <= 10
                            wait(1.1)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo")
                            wait(1)
                            repeat Tween(CFrame.new(2099.88159, 448.931, 648.997375)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(2099.88159, 448.931, 648.997375)).Magnitude <= 10
                            wait(2)
                        else
                            repeat Tween(CFrame.new(2099.88159, 448.931, 648.997375)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(2099.88159, 448.931, 648.997375)).Magnitude <= 10
                        end
                    elseif game:GetService("Players").LocalPlayer.Data.Level.Value >= 800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BartiloQuestProgress","Bartilo") == 2 then
                        repeat Tween(CFrame.new(-1850.49329, 13.1789551, 1750.89685)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1850.49329, 13.1789551, 1750.89685)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1858.87305, 19.3777466, 1712.01807)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1858.87305, 19.3777466, 1712.01807)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1803.94324, 16.5789185, 1750.89685)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1803.94324, 16.5789185, 1750.89685)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1858.55835, 16.8604317, 1724.79541)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1858.55835, 16.8604317, 1724.79541)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1869.54224, 15.987854, 1681.00659)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1869.54224, 15.987854, 1681.00659)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1800.0979, 16.4978027, 1684.52368)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1800.0979, 16.4978027, 1684.52368)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1819.26343, 14.795166, 1717.90625)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1819.26343, 14.795166, 1717.90625)).Magnitude <= 10
                        wait(1)
                        repeat Tween(CFrame.new(-1813.51843, 14.8604736, 1724.79541)) wait() until not _G.AutoBartilo or (game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-1813.51843, 14.8604736, 1724.79541)).Magnitude <= 10
                    end
                end 
            end
        end)
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Rengoku',
        Default = false,
        Tooltip = 'Auto Rengoku',
    
        Callback = function(v)
            _G.AutoRengoku = v
			StopTween(_G.AutoRengoku)
        end
    })


    spawn(function()
        pcall(function()
            while wait() do
                if _G.AutoRengoku then
                    if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Hidden Key") or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Hidden Key") then
                        EquipTool("Hidden Key")
                        Tween(CFrame.new(6571.1201171875, 299.23028564453, -6967.841796875))
                    elseif game:GetService("Workspace").Enemies:FindFirstChild("Snow Lurker") or game:GetService("Workspace").Enemies:FindFirstChild("Arctic Warrior") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if (v.Name == "Snow Lurker" or v.Name == "Arctic Warrior") and v.Humanoid.Health > 0 then
                                repeat task.wait()
                                    EquipTool(_G.SelectWeapon)
yakmefan()
                                    AutoHaki()
                                    v.HumanoidRootPart.CanCollide = false
                                    v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                    FarmPos = v.HumanoidRootPart.CFrame
									MonFarm = v.Name
                                    Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                    
                                    BringMob = true
                                until game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Hidden Key") or _G.AutoRengoku == false or not v.Parent or v.Humanoid.Health <= 0
                                BringMob = false
                            end
                        end
                    else
                        BringMob = false
                        Tween(CFrame.new(5439.716796875, 84.420944213867, -6715.1635742188))
                    end
                end
            end
        end)
    end)



    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Swan Glasses',
        Default = false,
        Tooltip = 'Auto Swan Glasses',
    
        Callback = function(v)
            _G.Auto_Swan_Glasses = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Swan Glasses Hop',
        Default = false,
        Tooltip = 'Auto Swan Glasses Hop',
    
        Callback = function(v)
            _G.Auto_Swan_Glasses_Hop = v
        end
    })

    spawn(function()
        pcall(function()
            while wait() do
                if _G.AutoFarmSwanGlasses then
                    if game:GetService("Workspace").Enemies:FindFirstChild("Don Swan") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Don Swan" and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                repeat task.wait()
                                    pcall(function()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    end)
                                until _G.AutoFarmSwanGlasses == false or v.Humanoid.Health <= 0
                            end
                        end
                    else 
                        repeat task.wait()
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(2284.912109375, 15.537666320801, 905.48291015625)) 
                        until (CFrame.new(2284.912109375, 15.537666320801, 905.48291015625).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 4 or _G.AutoFarmSwanGlasses == false
                    end
                elseif _G.AutoFarmSwanGlasses then
                    Hop()
                end
            end
        end)
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Law Sword',
        Default = false,
        Tooltip = 'Auto Law Sword',
    
        Callback = function(v)
            _G.AutoOderSword = v
        end
    })



    spawn(function()
        while wait() do
            if  _G.AutoOderSword then
                pcall(function()
                    if not game:GetService("Workspace").Enemies:FindFirstChild("Order") then
                        local args = {
                            [1] = "BlackbeardReward",
                            [2] = "Microchip",
                            [3] = "2"
                         }
                         game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                         wait(.1)
                         fireclickdetector(game:GetService("Workspace").Map.CircleIsland.RaidSummon.Button.Main.ClickDetector)
                    elseif game:GetService("Workspace").Enemies:FindFirstChild("Order") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Order" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.AutoOderSword or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Order") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Order").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.AutoOderSwordHop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)
    

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dragon Trident',
        Default = false,
        Tooltip = 'Auto Dragon Trident',
    
        Callback = function(v)
            _G.Auto_Dragon_Trident = v
            StopTween(_G.Auto_Dragon_Trident)
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dragon Trident Hop',
        Default = false,
        Tooltip = 'Auto Dragon Trident Hop',
    
        Callback = function(v)
            _G.Auto_Dragon_Trident_Hop = v
            StopTween(_G.Auto_Dragon_Trident_Hop)
        end
    })

    spawn(function()
        while wait() do
            if  _G.Auto_Dragon_Trident and World2 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Tide Keeper") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Tide Keeper" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.Auto_Dragon_Trident or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-3914.830322265625, 123.29389190673828, -11516.8642578125))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Tide Keeper").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.Auto_Dragon_Trident_Hop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)


    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dark Coat',
        Default = false,
        Tooltip = 'Auto Dark Coat',
    
        Callback = function(v)
            _G.Auto_Dark_Coat = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dark Coat Hop',
        Default = false,
        Tooltip = 'Auto Dark Coat Hop',
    
        Callback = function(v)
            _G.Auto_Dark_Coat_Hop = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Buy Legendary Sword',
        Default = false,
        Tooltip = 'Auto Buy Legendary Sword',
    
        Callback = function(v)
            _G.Auto_Buy_Legendary_Sword = v
        end
    })

    spawn(function()
        while wait() do
            if _G.AutoBuyLegendarySword then
                pcall(function()
                    local args = {
                        [1] = "LegendarySwordDealer",
                        [2] = "1"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    local args = {
                        [1] = "LegendarySwordDealer",
                        [2] = "2"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    local args = {
                        [1] = "LegendarySwordDealer",
                        [2] = "3"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                    if _G.AutoBuyLegendarySword_Hop and _G.AutoBuyLegendarySword and World2 then
                        wait(10)
                        Hop()
                    end
                end)
            end 
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Buy Enchanment Haki',
        Default = false,
        Tooltip = 'Auto Buy Enchanment Haki',
    
        Callback = function(v)
            _G.Auto_Buy_Enchanment_Haki = v
        end
    })

    spawn(function()
        while wait() do
            if _G.AutoBuyEnchancementColour then
                local args = {
                    [1] = "ColorsDealer",
                    [2] = "2"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                if _G.AutoBuyEnchancementColour_Hop and _G.AutoBuyEnchancementColour and not World1 then
                    wait(10)
                    Hop()
                end
            end 
        end
    end)

elseif World3 then

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Holy Torch',
        Default = false,
        Tooltip = 'Auto Holy Torch',
    
        Callback = function(v)
            _G.AutoHolyTorch = v
		    StopTween(_G.AutoHolyTorch)
        end
    })

    spawn(function()
        while wait() do
            if _G.AutoHolyTorch then
                pcall(function()
                    wait(1)
                    Tween(CFrame.new(-10752, 417, -9366))
                    wait(1)
                    Tween(CFrame.new(-11672, 334, -9474))
                    wait(1)
                    Tween(CFrame.new(-12132, 521, -10655))
                    wait(1)
                    Tween(CFrame.new(-13336, 486, -6985))
                    wait(1)
                    Tween(CFrame.new(-13489, 332, -7925))
                end)
            end
        end
    end)
    
    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Rainbow Haki',
        Default = false,
        Tooltip = 'Auto Rainbow Haki',
    
        Callback = function(v)
            _G.Auto_Rainbow_Haki = v
            StopTween(_G.Auto_Rainbow_Haki)
        end
    })

    spawn(function()
        pcall(function()
            while wait(.1) do
                if _G.Auto_Rainbow_Haki then
                    if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                        Tween(CFrame.new(-11892.0703125, 930.57672119141, -8760.1591796875))
                        if (Vector3.new(-11892.0703125, 930.57672119141, -8760.1591796875) - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30 then
                            wait(1.5)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("HornedMan","Bet")
                        end
                    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Stone") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Stone") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Stone" then
                                    
                                    repeat task.wait()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        v.HumanoidRootPart.CanCollide = false
                                        FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    until _G.Auto_Rainbow_Haki == false or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                end
                            end
                        else
                            Tween(CFrame.new(-1086.11621, 38.8425903, 6768.71436, 0.0231462717, -0.592676699, 0.805107772, 2.03251839e-05, 0.805323839, 0.592835128, -0.999732077, -0.0137055516, 0.0186523199))
                        end
                    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Island Empress") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Island Empress") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Island Empress" then
                                    
                                    repeat task.wait()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        v.HumanoidRootPart.CanCollide = false
                                        FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    until _G.Auto_Rainbow_Haki == false or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                end
                            end
                        else
                            Tween(CFrame.new(5713.98877, 601.922974, 202.751251, -0.101080291, -0, -0.994878292, -0, 1, -0, 0.994878292, 0, -0.101080291))
                        end
                    elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Kilo Admiral") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Kilo Admiral") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Kilo Admiral" then
                                    
                                    repeat task.wait()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    until _G.Auto_Rainbow_Haki == false or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                end
                            end
                        else
                            Tween(CFrame.new(2877.61743, 423.558685, -7207.31006, -0.989591599, -0, -0.143904909, -0, 1.00000012, -0, 0.143904924, 0, -0.989591479))
                        end
                    elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Captain Elephant") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Captain Elephant" then
                                    
                                    repeat task.wait()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    until _G.Auto_Rainbow_Haki == false or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                end
                            end
                        else
                            Tween(CFrame.new(-13485.0283, 331.709259, -8012.4873, 0.714521289, 7.98849911e-08, 0.69961375, -1.02065748e-07, 1, -9.94383065e-09, -0.69961375, -6.43015241e-08, 0.714521289))
                        end
                    elseif string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Beautiful Pirate") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Beautiful Pirate" then
                                    
                                    repeat task.wait()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        FarmPos = v.HumanoidRootPart.CFrame
									    MonFarm = v.Name
                                        
                                        sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                    until _G.Auto_Rainbow_Haki == false or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                end
                            end
                        else
                            Tween(CFrame.new(5312.3598632813, 20.141201019287, -10.158538818359))
                        end
                    else
                        Tween(CFrame.new(-11892.0703125, 930.57672119141, -8760.1591796875))
                        if (Vector3.new(-11892.0703125, 930.57672119141, -8760.1591796875) - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30 then
                            wait(1.5)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("HornedMan","Bet")
                        end
                    end
                end
            end
        end)
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Farm Elite Hunter',
        Default = false,
        Tooltip = 'Auto Farm Elite Hunter',
    
        Callback = function(v)
            _G.Auto_Farm_Elite_Hunter = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Farm Elite Hunter Hop',
        Default = false,
        Tooltip = 'Auto Farm Elite Hunter Hop',
    
        Callback = function(v)
            _G.Auto_Farm_Elite_Hunter_Hop = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Musketeer Hat',
        Default = false,
        Tooltip = 'Auto Musketeer Hat',
    
        Callback = function(v)
            _G.AutoMusketeerHat = v
            StopTween(_G.AutoMusketeerHat)
        end
    })

    spawn(function()
        pcall(function()
            while wait(.1) do
                if _G.AutoMusketeerHat then
                    if game:GetService("Players").LocalPlayer.Data.Level.Value >= 1800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress").KilledBandits == false then
                        if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Forest Pirate") and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "50") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Forest Pirate") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Forest Pirate" then
                                        repeat task.wait()
                                            pcall(function()
                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                AutoHaki()
                                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                                v.HumanoidRootPart.CanCollide = false
                                                
                                                FarmPos = v.HumanoidRootPart.CFrame
									            MonFarm = v.Name
                                                BringMob = true
                                            end)
                                        until _G.AutoMusketeerHat == false or not v.Parent or v.Humanoid.Health <= 0 or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                        BringMob = false
                                    end
                                end
                            else
                                BringMob = false
                                Tween(CFrame.new(-13206.452148438, 425.89199829102, -7964.5537109375))
                            end
                        else
                            Tween(CFrame.new(-12443.8671875, 332.40396118164, -7675.4892578125))
                            if (Vector3.new(-12443.8671875, 332.40396118164, -7675.4892578125) - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 30 then
                                wait(1.5)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","CitizenQuest",1)
                            end
                        end
                    elseif game:GetService("Players").LocalPlayer.Data.Level.Value >= 1800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress").KilledBoss == false then
                        if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible and string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, "Captain Elephant") and game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant") then
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Captain Elephant" then
                                        OldCFrameElephant = v.HumanoidRootPart.CFrame
                                        repeat task.wait()
                                            pcall(function()
                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                AutoHaki()
                                                v.HumanoidRootPart.CanCollide = false
                                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                                v.HumanoidRootPart.CanCollide = false
                                                v.HumanoidRootPart.CFrame = OldCFrameElephant
                                                
                                                sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                            end)
                                        until _G.AutoMusketeerHat == false or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
                                    end
                                end
                            else
                                Tween(CFrame.new(-13374.889648438, 421.27752685547, -8225.208984375))
                            end
                        else
                            Tween(CFrame.new(-12443.8671875, 332.40396118164, -7675.4892578125))
                            if (CFrame.new(-12443.8671875, 332.40396118164, -7675.4892578125).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 4 then
                                wait(1.5)
                                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress","Citizen")
                            end
                        end
                    elseif game:GetService("Players").LocalPlayer.Data.Level.Value >= 1800 and game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress","Citizen") == 2 then
                        Tween(CFrame.new(-12512.138671875, 340.39279174805, -9872.8203125))
                    end
                end
            end
        end)
    end)











    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Buddy Sword',
        Default = false,
        Tooltip = 'Auto Buddy Sword',
    
        Callback = function(v)
            _G.Auto_Buddy_Sword = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Buddy Sword Hop',
        Default = false,
        Tooltip = 'Auto Buddy Sword Hop',
    
        Callback = function(v)
            _G.Auto_Buddy_Sword_Hop = v
        end
    })

    spawn(function()
        while wait() do
            if _G.AutoBudySword and World3 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Cake Queen" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not _G.AutoBudySword or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-731.2034301757812, 381.5658874511719, -11198.4951171875))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Cake Queen") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Cake Queen").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if _G.AutoBudySwordHop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Observation V2',
        Default = false,
        Tooltip = 'Auto Observation V2',
    
        Callback = function(v)
            _G.AutoObservationHakiV2 = v
        end
    })

    spawn(function()
        while wait() do
            if _G.AutoObservationHakiV2 then
                if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
                    repeat 
                        Tween(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625)) 
                        wait() 
                    until _G.StopTween == true or not _G.AutoObservationHakiV2 or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-12444.78515625, 332.40396118164, -7673.1806640625)).Magnitude <= 10
                    wait(.5)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress","Citizen")
                    wait(1)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","CitizenQuest",1)
                else
                    if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text,"Defeat 50 Forest Pirates") then
                        if game:GetService("Workspace").Enemies:FindFirstChild("Forest Pirate") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Forest Pirate" then
                                    repeat wait()
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(1,20,1))
                                        PosHee =  v.HumanoidRootPart.CFrame
                                        if sethiddenproperty then
                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                        end
                                        v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        game:GetService'VirtualUser':CaptureController()
                                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                        Mangnetcitzenmon = true
                                    until _G.AutoObservationHakiV2 == false or v.Humanoid.Health <= 0
                                    Mangnetcitzenmon = false
                                end
                            end
                        else
                            repeat 
                                Tween(CFrame.new(-13277.568359375, 370.34185791016, -7821.1572265625)) 
                                wait() 
                            until _G.StopTween == true or not _G.AutoObservationHakiV2 or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-13277.568359375, 370.34185791016, -7821.1572265625)).Magnitude <= 10
                        end
                    elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text ==  "Defeat  Captain Elephant (0/1)" then 
                        if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant") then
                            for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                if v.Name == "Captain Elephant" then
                                    repeat wait()
                                        if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
                                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
                                        end
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(1,20,1))										
                                        if sethiddenproperty then
                                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                                        end
                                        v.HumanoidRootPart.CFrame = v.HumanoidRootPart.CFrame
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        game:GetService'VirtualUser':CaptureController()
                                        game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
                                    until _G.AutoObservationHakiV2 == false or v.Humanoid.Health <= 0
                                end
                            end
                        else
                            repeat 
                                Tween(CFrame.new(-13493.12890625, 318.89553833008, -8373.7919921875)) 
                                wait() 
                            until _G.StopTween == true or not _G.AutoObservationHakiV2 or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-13493.12890625, 318.89553833008, -8373.7919921875)).Magnitude <= 10
                        end        
                    end
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Banana") and  game.Players.LocalPlayer.Backpack:FindFirstChild("Apple") and game.Players.LocalPlayer.Backpack:FindFirstChild("Pineapple") then
                    repeat 
                        Tween(CFrame.new(-12444.78515625, 332.40396118164, -7673.1806640625)) 
                        wait() 
                    until _G.StopTween == true or not _G.AutoObservationHakiV2 or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-12444.78515625, 332.40396118164, -7673.1806640625)).Magnitude <= 10
                    wait(.5)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CitizenQuestProgress","Citizen")
                elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Fruit Bowl") or game.Players.LocalPlayer.Character:FindFirstChild("Fruit Bowl") then
                    repeat 
                        Tween(CFrame.new(-10920.125, 624.20275878906, -10266.995117188)) 
                        wait() 
                    until _G.StopTween == true or not _G.AutoObservationHakiV2 or (game.Players.LocalPlayer.Character.HumanoidRootPart.Position-Vector3.new(-10920.125, 624.20275878906, -10266.995117188)).Magnitude <= 10
                    wait(.5)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("KenTalk2","Start")
                    wait(1)
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("KenTalk2","Buy")
                else
                    for i,v in pairs(game.Workspace:GetDescendants()) do
                        if v.Name == "Apple" or v.Name == "Banana" or v.Name == "Pineapple" then
                            v.Handle.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,1,10)
                            wait()
                            firetouchinterest(game.Players.LocalPlayer.Character.HumanoidRootPart,v.Handle,0)    
                            wait()
                        end
                    end   
                end
            end
        end
    end)

    spawn(function()
        while wait() do
            pcall(function()
                if _G.AutoObservationHakiV2 then
                    if sethiddenproperty then
                        sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                    end
                end
            end)
            game:GetService("RunService").Heartbeat:Wait()
        end
    end)

    spawn(function()
        game:GetService("RunService").Heartbeat:connect(function()
            pcall(function()
                if _G.AutoObservationHakiV2 then
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Humanoid") then
                        game:GetService("Players").LocalPlayer.Character.Humanoid:ChangeState(11)
                    end
                end
            end)
        end)
    end)

    spawn(function()
        pcall(function()
            game:GetService("RunService").Heartbeat:Connect(function()
                game:GetService("RunService").Heartbeat:Wait()
                if _G.AutoObservationHakiV2 and StatrMagnet then
                    for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                        if v.Name == "Forest Pirate" and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
                            if v.Name == "Forest Pirate" then
                                v.HumanoidRootPart.CanCollide = false
                                v.HumanoidRootPart.Size = Vector3.new(50, 50, 50)
                                v.HumanoidRootPart.CFrame = PosHee
                            end
                        end
                    end
                end
            end)
        end)
    end)

    spawn(function()
        game:GetService("RunService").Heartbeat:connect(function()
            game:GetService("RunService").Heartbeat:Wait()
            pcall(function()
                if _G.AutoObservationHakiV2 and StatrMagnet then
                    CheckQuest()
                    for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
                        if v.Name == Ms then
                            v.Humanoid:ChangeState(11)
                        end
                    end
                end
            end)
            game:GetService("RunService").Heartbeat:Wait()
        end)
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Cavender',
        Default = false,
        Tooltip = 'Auto Cavender',
    
        Callback = function(v)
            _G.Auto_Cavender = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Cavender Hop',
        Default = false,
        Tooltip = 'Auto Cavender Hop',
    
        Callback = function(v)
            _G.Auto_Cavender_Hop = v
        end
    })

    spawn(function()
        while wait() do
            if  _G.AutoCarvender and World3 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Beautiful Pirate") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Beautiful Pirate" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.AutoCarvender or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(5311.07421875, 426.0243835449219, 165.12762451171875))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Beautiful Pirate") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Beautiful Pirate").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.AutoCavanderhop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Yama',
        Default = false,
        Tooltip = 'Auto Yama',
    
        Callback = function(v)
            _G.AutoYama = v
            StopTween(_G.AutoYama)
        end
    })

    spawn(function()
        while wait() do
            if _G.AutoYama then
                if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("EliteHunter","Progress") >= 30 then
                    repeat wait(.1)
                        fireclickdetector(game:GetService("Workspace").Map.Waterfall.SealedKatana.Handle.ClickDetector)
                    until game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Yama") or not _G.AutoYama
                end
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Tushita',
        Default = false,
        Tooltip = 'Auto Tushita',
    
        Callback = function(v)
            _G.Autotushita = v
            StopTween(_G.Autotushita)
        end
    })

    spawn(function()
        while wait() do
            if  _G.Autotushita and World3 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Longma") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Longma" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.Autotushita or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-10238.875976563, 389.7912902832, -9549.7939453125))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Longma") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Longma").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.Autotushitahop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Cursed Dual Katana',
        Default = false,
        Tooltip = 'Auto Cursed Dual Katana',
    
        Callback = function(v)
            _G.AutoCdk = v
            StopTween(_G.AutoCdk)
        end
    })


    spawn(function()
		while wait() do
			pcall(function()
				if _G.AutoCdk then
					if GetMaterial("Alucard Fragment") == 0 then
						Auto_Quest_Yama_1 = true
						Auto_Quest_Yama_2 = false
						Auto_Quest_Yama_3 = false
						Auto_Quest_Tushita_1 = false
						Auto_Quest_Tushita_2 = false
						Auto_Quest_Tushita_3 = false
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Evil")
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Evil")
					elseif GetMaterial("Alucard Fragment") == 1 then
						Auto_Quest_Yama_1 = false
						Auto_Quest_Yama_2 = true
						Auto_Quest_Yama_3 = false
						Auto_Quest_Tushita_1 = false
						Auto_Quest_Tushita_2 = false
						Auto_Quest_Tushita_3 = false
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Evil")
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Evil")
					elseif GetMaterial("Alucard Fragment") == 2 then
						Auto_Quest_Yama_1 = false
						Auto_Quest_Yama_2 = false
						Auto_Quest_Yama_3 = true
						Auto_Quest_Tushita_1 = false
						Auto_Quest_Tushita_2 = false
						Auto_Quest_Tushita_3 = false
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Evil")
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Evil")
					elseif GetMaterial("Alucard Fragment") == 3 then
						Auto_Quest_Yama_1 = false
						Auto_Quest_Yama_2 = false
						Auto_Quest_Yama_3 = false
						Auto_Quest_Tushita_1 = true
						Auto_Quest_Tushita_2 = false
						Auto_Quest_Tushita_3 = false
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Good")
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Good")
					elseif GetMaterial("Alucard Fragment") == 4 then
						Auto_Quest_Yama_1 = false
						Auto_Quest_Yama_2 = false
						Auto_Quest_Yama_3 = false
						Auto_Quest_Tushita_1 = false
						Auto_Quest_Tushita_2 = true
						Auto_Quest_Tushita_3 = false
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Good")
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Good")
					elseif GetMaterial("Alucard Fragment") == 5 then
						Auto_Quest_Yama_1 = false
						Auto_Quest_Yama_2 = false
						Auto_Quest_Yama_3 = false
						Auto_Quest_Tushita_1 = false
						Auto_Quest_Tushita_2 = false
						Auto_Quest_Tushita_3 = true
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Good")
						game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Good")
					elseif GetMaterial("Alucard Fragment") == 6 then
						if game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton Boss") or game:GetService("Workspace").ReplicatedStorage:FindFirstChild("Cursed Skeleton Boss") then
							Auto_Quest_Yama_1 = false
							Auto_Quest_Yama_2 = false
							Auto_Quest_Yama_3 = false
							Auto_Quest_Tushita_1 = false
							Auto_Quest_Tushita_2 = false
							Auto_Quest_Tushita_3 = false
							if game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton Boss") or game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton") then
								for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
									if v.Name == "Cursed Skeleton Boss" or v.Name == "Cursed Skeleton" then
										if v.Humanoid.Health > 0 then
											v.HumanoidRootPart.CanCollide = false
											v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
											Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,50,0))
											game:GetService'VirtualUser':CaptureController()
											game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
										end
									end
								end
							end
						else
							if (CFrame.new(-12361.7060546875, 603.3547973632812, -6550.5341796875).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 100 then
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Good")
								wait(1)
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","Progress","Evil")
								wait(1)
								Tween(CFrame.new(-12361.7060546875, 603.3547973632812, -6550.5341796875))
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)
								Tween(CFrame.new(-12253.5419921875, 598.8999633789062, -6546.8388671875))
							else
								Tween(CFrame.new(-12361.7060546875, 603.3547973632812, -6550.5341796875))
							end   
						end
					end
				end
			end)
		end
	end)

	spawn(function()
		while wait() do
			if Auto_Quest_Yama_1 then
				pcall(function()
					if game:GetService("Workspace").Enemies:FindFirstChild("Mythological Pirate") then
						for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
							if v.Name == "Mythological Pirate" then
								repeat wait()
									Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,0,-2))
								until _G.AutoCdk == false or Auto_Cursed_Dual_Katana == false or Auto_Quest_Yama_1 == false
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","StartTrial","Evil")
							end
						end
					else
						Tween(CFrame.new(-13451.46484375, 543.712890625, -6961.0029296875))
					end
				end)
			end
		end
	end)

	spawn(function()
		while wait() do
			pcall(function()
				if Auto_Quest_Yama_2 then
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v:FindFirstChild("HazeESP") then
							v.HazeESP.Size = UDim2.new(50,50,50,50)
							v.HazeESP.MaxDistance = "inf"
						end
					end
					for i,v in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
						if v:FindFirstChild("HazeESP") then
							v.HazeESP.Size = UDim2.new(50,50,50,50)
							v.HazeESP.MaxDistance = "inf"
						end
					end
				end
			end)
		end
	end)

	spawn(function()
		while wait() do
			pcall(function()
				for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
					if Auto_Quest_Yama_2 and v:FindFirstChild("HazeESP") and (v.HumanoidRootPart.Position - PosMonsEsp.Position).magnitude <= 300 then
						v.HumanoidRootPart.CFrame = PosMonsEsp
						v.HumanoidRootPart.CanCollide = false
						v.HumanoidRootPart.Size = Vector3.new(50,50,50)
						if not v.HumanoidRootPart:FindFirstChild("BodyVelocity") then
							local vc = Instance.new("BodyVelocity", v.HumanoidRootPart)
							vc.MaxForce = Vector3.new(1, 1, 1) * math.huge
							vc.Velocity = Vector3.new(0, 0, 0)
						end
					end
				end
			end)
		end
	end)

	spawn(function()
		while wait() do
			if Auto_Quest_Yama_2 then 
				pcall(function() 
					for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
						if v:FindFirstChild("HazeESP") then
							repeat wait()
								if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 2000 then
									Tween(y.HumanoidRootPart.CFrameMon * CFrame.new(0,20,0))
								else
									BringMob = true
									FastAttack = true
									if Auto_Buso then
										if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
										end
									end
									if not game.Players.LocalPlayer.Character:FindFirstChild(_G.SelectWeapon) then
										wait()
										EquipTool(_G.SelectWeapon)
yakmefan()
									end
									PosMonsEsp = v.HumanoidRootPart.CFrame
									if not FastAttack then
										game:GetService'VirtualUser':CaptureController()
										game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
									end
									v.HumanoidRootPart.Size = Vector3.new(60,60,60)
									if _G.Configs["Show Hitbox"] then
										v.HumanoidRootPart.Transparency = _G.Hitbox_LocalTransparency
									else
										v.HumanoidRootPart.Transparency = 1
									end
									v.Humanoid.JumpPower = 0
									v.Humanoid.WalkSpeed = 0
									v.HumanoidRootPart.CanCollide = false
									v.Humanoid:ChangeState(11)
									Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,20,0))								
								end      
							until Auto_Cursed_Dual_Katana == false or Auto_Quest_Yama_2 == false or not v.Parent or v.Humanoid.Health <= 0 or not v:FindFirstChild("HazeESP")
						else
							for x,y in pairs(game:GetService("ReplicatedStorage"):GetChildren()) do
								if y:FindFirstChild("HazeESP") then
									if (y.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 2000 then
										Tween(y.HumanoidRootPart.CFrameMon* CFrame.new(0,20,0))
									else
										Tween(y.HumanoidRootPart.CFrame * CFrame.new(0,20,0))
									end
								end
							end
						end
					end
				end)
			end
		end
	end)

	spawn(function()
		while wait() do
			if Auto_Quest_Yama_3 then
				pcall(function()
					if game.Players.LocalPlayer.Backpack:FindFirstChild("Hallow Essence") then         
						_G.Auto_Bone = false           
						Tween(game:GetService("Workspace").Map["Haunted Castle"].Summoner.Detection.CFrame)
					elseif game:GetService("Workspace").Map:FindFirstChild("HellDimension") then
						repeat wait()
							if game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Hell's Messenger [Boss]") then
								for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
									if v.Name == "Cursed Skeleton" or v.Name == "Cursed Skeleton" or v.Name == "Hell's Messenger" then
										if v.Humanoid.Health > 0 then
											repeat wait()
												BringMob = true
												FastAttack = true
												if Auto_Buso then
													if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
													end
												end
												if not game.Players.LocalPlayer.Character:FindFirstChild(_G.SelectWeapon) then
													wait()
													EquipTool(_G.SelectWeapon)
yakmefan()
												end
												PosMonsEsp = v.HumanoidRootPart.CFrame
												if not FastAttack then
													game:GetService'VirtualUser':CaptureController()
													game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
												end
												v.HumanoidRootPart.Size = Vector3.new(60,60,60)
												if _G.Configs["Show Hitbox"] then
													v.HumanoidRootPart.Transparency = _G.Hitbox_LocalTransparency
												else
													v.HumanoidRootPart.Transparency = 1
												end
												v.Humanoid.JumpPower = 0
												v.Humanoid.WalkSpeed = 0
												v.HumanoidRootPart.CanCollide = false
												v.Humanoid:ChangeState(11)
												Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,50,0))
											until v.Humanoid.Health <= 0 or not v.Parent or Auto_Quest_Yama_3 == false
										end
									end
								end
							else
								wait(5)
								Tween(game:GetService("Workspace").Map.HellDimension.Torch1.CFrame)
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)        
								Tween(game:GetService("Workspace").Map.HellDimension.Torch2.CFrame)
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)     
								Tween(game:GetService("Workspace").Map.HellDimension.Torch3.CFrame)
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)     
								Tween(game:GetService("Workspace").Map.HellDimension.Exit.CFrame)
							end
						until Auto_Cursed_Dual_Katana == false or Auto_Quest_Yama_3 == false or GetMaterial("Alucard Fragment") == 3
					else
						if game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper") or game.ReplicatedStorage:FindFirstChild("Soul Reaper") then
							if game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper") then
								for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
									if v.Name == "Soul Reaper" then
										if v.Humanoid.Health > 0 then
											repeat wait()
												Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,0,-2))
											until Auto_Cursed_Dual_Katana == false or Auto_Quest_Yama_3 == false or game:GetService("Workspace").Map:FindFirstChild("HellDimension")
										end
									end
								end
							else
								Tween(CFrame.new(-9570.033203125, 315.9346923828125, 6726.89306640625))
							end
						else
							_G.Auto_Bone = true
							game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones","Buy",1,1)
						end
					end
				end)
			end
		end
	end)

	spawn(function() 
		while wait() do
			if Auto_Quest_Tushita_1 then
				game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CDKQuest","BoatQuest",workspace.NPCs:FindFirstChild("Luxury Boat Dealer"))
			end
		end
	end)

	spawn(function()
		while wait() do
			if Auto_Quest_Tushita_1 then
				Tween(CFrame.new(-9546.990234375, 21.139892578125, 4686.1142578125))
				wait(5)
				Tween(CFrame.new(-6120.0576171875, 16.455780029296875, -2250.697265625))
				wait(5)
				Tween(CFrame.new(-9533.2392578125, 7.254445552825928, -8372.69921875))    
			end
		end
	end)

	spawn(function()
		while wait() do
			if Auto_Quest_Tushita_2 then
				pcall(function()
					if (CFrame.new(-5539.3115234375, 313.800537109375, -2972.372314453125).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 500 then
						for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
							if Auto_Quest_Tushita_2 and v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
								if (v.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude < 2000 then
									repeat wait()
										v.HumanoidRootPart.CanCollide = false
										v.HumanoidRootPart.Size = Vector3.new(60, 60, 60)
										Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,50,0))
										game:GetService'VirtualUser':CaptureController()
										game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
									until v.Humanoid.Health <= 0 or not v.Parent or Auto_Quest_Tushita_2 == false
								end
							end
						end
					else
						Tween(CFrame.new(-5545.1240234375, 313.800537109375, -2976.616455078125))
					end
				end)
			end
		end
	end)

	spawn(function()
		while wait() do
			if Auto_Quest_Tushita_3 then
				pcall(function()
					if game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen") or game.ReplicatedStorage:FindFirstChild("Cake Queen") then
						if game:GetService("Workspace").Enemies:FindFirstChild("Cake Queen") then
							for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
								if v.Name == "Cake Queen" then
									if v.Humanoid.Health > 0 then
										repeat wait()
											if Auto_Buso then
												if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
													game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
												end
											end
											if not game.Players.LocalPlayer.Character:FindFirstChild(_G.SelectWeapon) then
												wait()
												EquipTool(_G.SelectWeapon)
yakmefan()
											end
											if not FastAttack then
												game:GetService'VirtualUser':CaptureController()
												game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
											end
											v.HumanoidRootPart.Size = Vector3.new(60,60,60)
											if _G.Configs["Show Hitbox"] then
												v.HumanoidRootPart.Transparency = _G.Hitbox_LocalTransparency
											else
												v.HumanoidRootPart.Transparency = 1
											end
											v.Humanoid.JumpPower = 0
											v.Humanoid.WalkSpeed = 0
											v.HumanoidRootPart.CanCollide = false
											v.Humanoid:ChangeState(11)
                                            
											Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,50,0))
										until Auto_Cursed_Dual_Katana == false or Auto_Quest_Tushita_3 == false or game:GetService("Workspace").Map:FindFirstChild("HeavenlyDimension")
									end
								end
							end
						else
							Tween(CFrame.new(-709.3132934570312, 381.6005859375, -11011.396484375))
						end
					elseif game:GetService("Workspace").Map:FindFirstChild("HeavenlyDimension") then
						repeat wait()
							if game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Cursed Skeleton") or game:GetService("Workspace").Enemies:FindFirstChild("Heaven's Guardian") then
								for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
									if v.Name == "Cursed Skeleton" or v.Name == "Cursed Skeleton" or v.Name == "Heaven's Guardian" then
										if v.Humanoid.Health > 0 then
											repeat wait()
												if Auto_Buso then
													if not game.Players.LocalPlayer.Character:FindFirstChild("HasBuso") then
														game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
													end
												end
												if not game.Players.LocalPlayer.Character:FindFirstChild(_G.SelectWeapon) then
													wait()
													EquipTool(_G.SelectWeapon)
yakmefan()
												end
												if not FastAttack then
													game:GetService'VirtualUser':CaptureController()
													game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
												end
												v.HumanoidRootPart.Size = Vector3.new(60,60,60)
												if _G.Configs["Show Hitbox"] then
													v.HumanoidRootPart.Transparency = _G.Hitbox_LocalTransparency
												else
													v.HumanoidRootPart.Transparency = 1
												end
												v.Humanoid.JumpPower = 0
												v.Humanoid.WalkSpeed = 0
												v.HumanoidRootPart.CanCollide = false
												v.Humanoid:ChangeState(11)
											until v.Humanoid.Health <= 0 or not v.Parent or Auto_Quest_Tushita_3 == false
										end
									end
								end
							else
								wait(5)
								Tween(game:GetService("Workspace").Map.HeavenlyDimension.Torch1.CFrame)
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)        
								Tween(game:GetService("Workspace").Map.HeavenlyDimension.Torch2.CFrame)
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)     
								Tween(game:GetService("Workspace").Map.HeavenlyDimension.Torch3.CFrame)
								wait(1.5)
								game:GetService("VirtualInputManager"):SendKeyEvent(true, "E", false, game)
								wait(1.5)     
								Tween(game:GetService("Workspace").Map.HeavenlyDimension.Exit.CFrame)
							end
						until Auto_Cursed_Dual_Katana == false or Auto_Quest_Tushita_3 == false or GetMaterial("Alucard Fragment") == 6
					else
						hop()
                end
            end)
        end
    end
 end)

 Tab3:AddToggle('MyToggle', {
    Text = 'Auto Serpent Bow',
    Default = false,
    Tooltip = 'Auto Serpent Bow',

    Callback = function(v)
        _G.Auto_Serpent_Bow = v
    end
})

Tab3:AddToggle('MyToggle', {
    Text = 'Auto Hallow Scythe',
    Default = false,
    Tooltip = 'Auto Hallow Scythe',
    
    Callback = function(v)
        _G.AutoFarmBossHallow = v
        StopTween(_G.AutoFarmBossHallow)
    end
})

Tab3:AddToggle('MyToggle', {
    Text = 'Auto Hallow Scythe Hop',
    Default = false,
    Tooltip = 'Auto Hallow Scythe Hop',
    
    Callback = function(v)
        _G.AutoFarmBossHallowHop = v
        StopTween(_G.AutoFarmBossHallowHop)
    end
})

spawn(function()
    while wait() do
        if _G.AutoFarmBossHallow then
            pcall(function()
                if game:GetService("Workspace").Enemies:FindFirstChild("Soul Reaper") then
                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                        if string.find(v.Name , "Soul Reaper") then
                            repeat task.wait()
                                EquipTool(_G.SelectWeapon)
yakmefan()
                                AutoHaki()
                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                Tween(v.HumanoidRootPart.CFrame*CFrame.new(2,40,2))
                                v.HumanoidRootPart.Transparency = 1
                                sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                            until v.Humanoid.Health <= 0 or _G.AutoFarmBossHallow == false
                        end
                    end
                elseif game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Hallow Essence") or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Hallow Essence") then
                    repeat Tween(CFrame.new(-8932.322265625, 146.83154296875, 6062.55078125)) wait() until (CFrame.new(-8932.322265625, 146.83154296875, 6062.55078125).Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 8                        
                    EquipTool("Hallow Essence")
                else
                    if game:GetService("ReplicatedStorage"):FindFirstChild("Soul Reaper") then
                        Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Soul Reaper").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                    else
                        if _G.AutoFarmBossHallowHop then
                            Hop()
                        end
                    end
                end
            end)
        end
    end
end)


    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dark Dagger',
        Default = false,
        Tooltip = 'Auto Dark Dagger',
    
        Callback = function(v)
            _G.AutoDarkDagger = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dark Dagger Hop',
        Default = false,
        Tooltip = 'Auto Dark Dagger Hop',
    
        Callback = function(v)
            _G.AutoDarkDaggerHop = v
        end
    })


    spawn(function()
        pcall(function()
            while wait() do
                if _G.AutoDarkDagger then
                    if game:GetService("Workspace").Enemies:FindFirstChild("rip_indra True Form") or game:GetService("Workspace").Enemies:FindFirstChild("rip_indra") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == ("rip_indra True Form" or v.Name == "rip_indra") and v.Humanoid.Health > 0 and v:IsA("Model") and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") then
                                repeat task.wait()
                                    pcall(function()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        game:GetService("VirtualUser"):CaptureController()
                                        game:GetService("VirtualUser"):Button1Down(Vector2.new(1280, 670),workspace.CurrentCamera.CFrame)
                                    end)
                                until _G.AutoDarkDagger == false or v.Humanoid.Health <= 0
                            end
                        end
                    else
                        Tween(CFrame.new(-5344.822265625, 423.98541259766, -2725.0930175781))
                    end
                elseif _G.AutoDarkDaggerHop then
                    Hop()
                end
            end
        end)
    end)
    
    


    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Dough V2',
        Default = false,
        Tooltip = 'Auto Dough V2',
    
        Callback = function(v)
            _G.Auto_Dough_V2 = v
        end
    })

    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Quest Soul Guitar',
        Default = false,
        Tooltip = 'Auto Quest Soul Guitar',
    
        Callback = function(v)
            _G.AutoNevaSoulGuitar = v
            StopTween(_G.AutoNevaSoulGuitar)
        end
    })



    spawn(function()
        pcall(function()
            while wait(50) do
                if game:GetService("Lighting").Sky.MoonTextureId=="http://www.roblox.com/asset/?id=9709149431" then
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://9709149431",
                        Title = "",
                        Text = "🌕 : Full Moon 100%"
                    })
                elseif game:GetService("Lighting").Sky.MoonTextureId=="http://www.roblox.com/asset/?id=9709149052" then
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://9709149052",
                        Title = "", 
                        Text = "🌖 : Full Moon 75%"
                    })
                elseif game:GetService("Lighting").Sky.MoonTextureId=="http://www.roblox.com/asset/?id=9709143733" then
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://9709143733",
                        Title = "", 
                        Text = "🌗 : Full Moon 50%"
                    })
                elseif game:GetService("Lighting").Sky.MoonTextureId=="http://www.roblox.com/asset/?id=9709150401" then
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://9709150401",
                        Title = "", 
                        Text = "🌘 : Full Moon 25%"
                    })
                elseif game:GetService("Lighting").Sky.MoonTextureId=="http://www.roblox.com/asset/?id=9709149680" then
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://9709149680",
                        Title = "", 
                        Text = "🌘: Full Moon 15%"
                    })
                else
                    game:GetService("StarterGui"):SetCore("SendNotification", {
                        Icon = "rbxassetid://0",
                        Title = "", 
                        Text = "🌑: Full Moon 0%"
                    })
                end
            end
        end)
    end)


    spawn(function()
		while wait() do
			pcall(function()
				if _G.AutoNevaSoulGuitar then
					if GetWeaponInventory("Soul Guitar") == false then
						if (CFrame.new(-9681.458984375, 6.139880657196045, 6341.3720703125).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 5000 then
							if game:GetService("Workspace").NPCs:FindFirstChild("Skeleton Machine") then
								game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("soulGuitarBuy",true)
							else
								if game:GetService("Workspace").Map["Haunted Castle"].Candle1.Transparency == 0 then
									if game:GetService("Workspace").Map["Haunted Castle"].Placard1.Left.Part.Transparency == 0 then
										Quest2 = true
										repeat wait() Tween(CFrame.new(-8762.69140625, 176.84783935546875, 6171.3076171875)) until (CFrame.new(-8762.69140625, 176.84783935546875, 6171.3076171875).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.AutoNevaSoulGuitar
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard7.Left.ClickDetector)
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard6.Left.ClickDetector)
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard5.Left.ClickDetector)
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard4.Right.ClickDetector)
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard3.Left.ClickDetector)
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard2.Right.ClickDetector)
										wait(1)
										fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"].Placard1.Right.ClickDetector)
										wait(1)
									elseif game:GetService("Workspace").Map["Haunted Castle"].Tablet.Segment1:FindFirstChild("ClickDetector") then
										if game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part1:FindFirstChild("ClickDetector") then
											Quest4 = true
											repeat wait() Tween(CFrame.new(-9553.5986328125, 65.62338256835938, 6041.58837890625)) until (CFrame.new(-9553.5986328125, 65.62338256835938, 6041.58837890625).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.AutoNevaSoulGuitar
											wait(1)
											Tween(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part3.CFrame)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part3.ClickDetector)
											wait(1)
											Tween(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part4.CFrame)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part4.ClickDetector)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part4.ClickDetector)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part4.ClickDetector)
											wait(1)
											Tween(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part6.CFrame)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part6.ClickDetector)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part6.ClickDetector)
											wait(1)
											Tween(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part8.CFrame)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part8.ClickDetector)
											wait(1)
											Tween(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part10.CFrame)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part10.ClickDetector)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part10.ClickDetector)
											wait(1)
											fireclickdetector(game:GetService("Workspace").Map["Haunted Castle"]["Lab Puzzle"].ColorFloor.Model.Part10.ClickDetector)
										else
											Quest3 = true
											--Not Work Yet
										end
									else
										if game:GetService("Workspace").NPCs:FindFirstChild("Ghost") then
											local args = {
												[1] = "GuitarPuzzleProgress",
												[2] = "Ghost"
											}

											game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
										end
										if game.Workspace.Enemies:FindFirstChild("Living Zombie") then
											for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
												if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
													if v.Name == "Living Zombie" then
														EquipTool(_G.SelectWeapon)
yakmefan()
														v.HumanoidRootPart.Size = Vector3.new(60,60,60)
														v.HumanoidRootPart.Transparency = 1
														v.Humanoid.JumpPower = 0
														v.Humanoid.WalkSpeed = 0
														v.HumanoidRootPart.CanCollide = false
														v.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0,20,0)
														Tween(CFrame.new(-10160.787109375, 138.6616973876953, 5955.03076171875))
														game:GetService'VirtualUser':CaptureController()
														game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
													end
												end
											end
										else
											Tween(CFrame.new(-10160.787109375, 138.6616973876953, 5955.03076171875))
										end
									end
								else    
									if string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("gravestoneEvent",2), "Error") then
										print("Go to Grave")
										Tween(CFrame.new(-8653.2060546875, 140.98487854003906, 6160.033203125))
									elseif string.find(game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("gravestoneEvent",2), "Nothing") then
										print("Wait Next Night")
									else
										game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("gravestoneEvent",2,true)
									end
								end
							end
								else
									Tween(CFrame.new(-9681.458984375, 6.139880657196045, 6341.3720703125))
								end
							else
								if _G.soulGuitarhop then
							hop()
                        end
                    end
                end
            end)
        end
    end)


    Tab3:AddToggle('MyToggle', {
        Text = 'Auto Twin Hook',
        Default = false,
        Tooltip = 'Auto Twin Hook',
    
        Callback = function(v)
            _G.AutoTwinHook = v
            StopTween(_G.AutoTwinHook)
        end
    })


    spawn(function()
        while wait() do
            if  _G.AutoTwinHook and World3 then
                pcall(function()
                    if game:GetService("Workspace").Enemies:FindFirstChild("Captain Elephant") then
                        for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                            if v.Name == "Captain Elephant" then
                                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                                    repeat task.wait()
                                        AutoHaki()
                                        EquipTool(_G.SelectWeapon)
yakmefan()
                                        v.HumanoidRootPart.CanCollide = false
                                        v.Humanoid.WalkSpeed = 0
                                        v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                        Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,40,2))
                                        
                                        sethiddenproperty(game.Players.LocalPlayer,"SimulationRadius",math.huge)
                                    until not  _G.AutoTwinHook or not v.Parent or v.Humanoid.Health <= 0
                                end
                            end
                        end
                    else
                    Tween(CFrame.new(-13348.0654296875, 405.8904113769531, -8570.62890625))
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Captain Elephant") then
                            Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Captain Elephant").HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                        else
                            if  _G.AutoTwinHook_Hop then
                                Hop()
                            end
                        end
                    end
                end)
            end
        end
    end)
end

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto Superhuman',
    Default = false,
    Tooltip = 'Auto Superhuman',

    Callback = function(v)
        _G.Auto_Superhuman = v
    end
})

spawn(function()
    while wait() do
        if _G.Auto_Superhuman and game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then 
            pcall(function()
                if game:GetService("Players").LocalPlayer.Data.Beli.Value >= 500000 and (game.Players.LocalPlayer.Character:FindFirstChild("Combat") or game.Players.LocalPlayer.Backpack:FindFirstChild("Combat")) then
                    _G.SelectWeapon = "Combat"
                    local args = {
                        [1] = "BuyElectro"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end   
                if game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") or game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") then
                    _G.SelectWeapon = "Superhuman"
                end  
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 299  then
                    _G.SelectWeapon = "Black Leg"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 299  then
                    _G.SelectWeapon = "Electro"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 299  then
                    _G.SelectWeapon = "Fishman Karate"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 299  then
                    _G.SelectWeapon = "Dragon Claw"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300  then
                    local args = {
                        [1] = "BuyFishmanKarate"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300  then
                    local args = {
                        [1] = "BuyFishmanKarate"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300  then
                    local args = {
                        [1] = "BuyBlackLeg"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300  then
                    local args = {
                        [1] = "BuySuperhuman"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300  then
                    local args = {
                        [1] = "BuySuperhuman"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end 
            end)
        end
    end
end)

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto Fully Superhuman',
    Default = false,
    Tooltip = 'Auto Fully Superhuman',

    Callback = function(v)
        _G.Auto_Fully_Superhuman = v
    end
})

spawn(function()
    while wait() do
        if _G.Auto_Fully_Superhuman and game.Players.LocalPlayer:FindFirstChild("WeaponAssetCache") then 
            pcall(function()
                if game:GetService("Players").LocalPlayer.Data.Beli.Value >= 500000 and (game.Players.LocalPlayer.Character:FindFirstChild("Combat") or game.Players.LocalPlayer.Backpack:FindFirstChild("Combat")) then
                    _G.SelectWeapon = "Combat"
                    local args = {
                        [1] = "BuyElectro"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end   
                if game.Players.LocalPlayer.Character:FindFirstChild("Superhuman") or game.Players.LocalPlayer.Backpack:FindFirstChild("Superhuman") then
                    _G.SelectWeapon = "Superhuman"
                end  
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 299  then
                    _G.SelectWeapon = "Black Leg"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Electro") and game.Players.LocalPlayer.Backpack:FindFirstChild("Electro").Level.Value <= 299  then
                    _G.SelectWeapon = "Electro"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value <= 299  then
                    _G.SelectWeapon = "Fishman Karate"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value <= 299  then
                    _G.SelectWeapon = "Dragon Claw"
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 300  then
                    local args = {
                        [1] = "BuyFishmanKarate"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 300  then
                    local args = {
                        [1] = "BuyFishmanKarate"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Electro") and game.Players.LocalPlayer.Character:FindFirstChild("Electro").Level.Value >= 300  then
                    local args = {
                        [1] = "BuyBlackLeg"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Backpack:FindFirstChild("Fishman Karate").Level.Value >= 300  then
                    if game.Players.LocalPlayer.Data.Fragments.Value < 1500 then
                        if game.Players.LocalPlayer.Data.Level.Value > 1100 then
                            _G.Auto_Farm_Level = false
                            _G.JoinD = true
                            wait(1.5)
                            _G.Auto_Dungeon_Superhuman = true
                        end
                    else
                        _G.JoinD = false
                        _G.Auto_Farm_Level = true
                        _G.Auto_Dungeon_Superhuman = false
                        local args = {
                            [1] = "BlackbeardReward",
                            [2] = "DragonClaw",
                            [3] = "2"
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","1")
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
                    end
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate") and game.Players.LocalPlayer.Character:FindFirstChild("Fishman Karate").Level.Value >= 300  then
                    if game.Players.LocalPlayer.Data.Fragments.Value < 1500 then
                        if game.Players.LocalPlayer.Data.Level.Value > 1100 then
                            _G.Auto_Farm_Level = false
                            _G.JoinD = true
                            wait(1.5)
                            _G.Auto_Dungeon_Superhuman = true
                        end
                    else
                        _G.JoinD = false
                        _G.Auto_Farm_Level = true
                        _G.Auto_Dungeon_Superhuman = false
                        local args = {
                            [1] = "BlackbeardReward",
                            [2] = "DragonClaw",
                            [3] = "2"
                        }
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","1")
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
                    end
                end

                if game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Backpack:FindFirstChild("Dragon Claw").Level.Value >= 300  then
                    local args = {
                        [1] = "BuySuperhuman"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end
                if game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw") and game.Players.LocalPlayer.Character:FindFirstChild("Dragon Claw").Level.Value >= 300  then
                    local args = {
                        [1] = "BuySuperhuman"
                    }
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                end 
            end)
        end
    end
end)
spawn(function()
    while wait() do
        if _G.Auto_Fully_Superhuman and _G.Auto_Dungeon_Superhuman then
            for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                    pcall(function()
                        repeat wait()
                            v.Humanoid.Health = 0
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                            v.HumanoidRootPart.Transparency = 1
                        until not _G.Auto_Dungeon_Superhuman or not v.Parent or v.Humanoid.Health <= 0
                    end)
                end
            end
        else
        -- _G.Auto_Farm_Level = false
        end
    end
end)
spawn(function()
    while wait() do
        if _G.Auto_Fully_Superhuman and _G.Auto_Dungeon_Superhuman then
            for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                    pcall(function()
                        repeat wait(.1)
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            v.Humanoid.Health = 0
                            v.HumanoidRootPart.CanCollide = false
                            v.HumanoidRootPart.Size = Vector3.new(500,500,500)
                            v.HumanoidRootPart.Transparency = 1
                        until not _G.Auto_Dungeon_Superhuman or not v.Parent or v.Humanoid.Health <= 0
                    end)
                end
            end
        else
        -- _G.Auto_Farm_Level = false
        end
    end
end)
spawn(function()
    while wait() do
        if _G.Auto_Dungeon_Superhuman then
            if not game.Players.LocalPlayer.PlayerGui.Main.Timer.Visible == false then
                if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5").CFrame * CFrame.new(0,70,100))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4").CFrame * CFrame.new(0,70,100))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3").CFrame * CFrame.new(0,70,100))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2").CFrame * CFrame.new(0,70,100))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1").CFrame * CFrame.new(0,70,100))
                end
            end
        else
        -- _G.Auto_Farm_Level = false
        end
    end
end)
spawn(function()
    while wait(2) do
        if _G.Auto_Fully_Superhuman and _G.Auto_Dungeon_Superhuman and _G.JoinD then
            if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == false then
                if Second_Sea then
                    fireclickdetector(game:GetService("Workspace").Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                elseif Third_Sea then
                    fireclickdetector(game:GetService("Workspace").Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                end
            end
        end
    end
end)
spawn(function()
    while wait() do
        pcall(function()
            if _G.Auto_Fully_Superhuman and _G.Auto_Dungeon_Superhuman then
                if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == false then
                    local Fragment = game:GetService("Players")["Localplayer"].Data.Fragments.Value
                    if Fragment >= 1499 then
                        _G.Auto_Dungeon_Superhuman = false
                        _G.Auto_Farm_Level = true
                    else
                        --_G.Auto_Farm_Level = false
                    end
                end
            end
        end)
    end
end)

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto Death Step',
    Default = false,
    Tooltip = 'Auto Death Step',

    Callback = function(v)
        _G.Auto_Death_Step = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Death_Step then
            if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Black Leg") or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Black Leg") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Death Step") or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Death Step") then
                if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Black Leg") and game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 450 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
                    _G.SelectWeapon = "Death Step"
                end  
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Black Leg") and game:GetService("Players").LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 450 then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
                    _G.SelectWeapon = "Death Step"
                end  
                if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Black Leg") and game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value <= 449 then
                    _G.SelectWeapon = "Black Leg"
                end 
            else 
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
            end
        end
    end
end)

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto Fully Death Step',
    Default = false,
    Tooltip = 'Auto Fully Death Step',

    Callback = function(v)
        _G.Auto_Fully_Death_Step = v
    end
})

spawn(function()
    while wait() do
        if _G.Auto_Fully_Death_Step then
            pcall(function()
                if not game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") or not game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") or not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Death Step") or not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Death Step") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
                end				
                if game:GetService("Workspace").Map.IceCastle.Hall.LibraryDoor.PhoeyuDoor.Transparency == 0 then  
                    if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Library Key") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Library Key") then
                        EquipTool("Library Key")
                        repeat wait() Tween(CFrame.new(6371.2001953125, 296.63433837890625, -6841.18115234375)) until (CFrame.new(6371.2001953125, 296.63433837890625, -6841.18115234375).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.Auto_Fully_Death_Step
                        if (CFrame.new(6371.2001953125, 296.63433837890625, -6841.18115234375).Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
                            wait(1.2)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep",true)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
                            wait(0.5)
                        end
                    elseif game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Backpack:FindFirstChild("Black Leg").Level.Value >= 450 or game.Players.LocalPlayer.Character:FindFirstChild("Black Leg") and game.Players.LocalPlayer.Character:FindFirstChild("Black Leg").Level.Value >= 450 then   
                        if game:GetService("ReplicatedStorage"):FindFirstChild("Awakened Ice Admiral") or game:GetService("Workspace").Enemies:FindFirstChild("Awakened Ice Admiral") then
                            if game:GetService("Workspace").Enemies:FindFirstChild("Awakened Ice Admiral") then 	
                                for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                    if v.Name == "Awakened Ice Admiral" then    
                                        repeat wait()
                                            AutoHaki()
                                            
                                            EquipTool(_G.SelectWeapon)
yakmefan()
                                            v.Head.CanCollide = false
                                            v.Humanoid.WalkSpeed = 0
                                            v.HumanoidRootPart.CanCollide = false
                                            v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                            Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,40,0))
                                            sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
                                        until not v.Parent or v.Humanoid.Health <= 0 or _G.Auto_Fully_Death_Step == false or game:GetService("Players").LocalPlayer.Character:FindFirstChild("Library Key") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Library Key")
                                    end
                                end
                            else
                                repeat wait() Tween(game:GetService("ReplicatedStorage"):FindFirstChild("Awakened Ice Admiral").HumanoidRootPart.CFrame) until game:GetService("Workspace").Enemies:FindFirstChild("Awakened Ice Admiral")
                            end
                        else 
                            Hop()
                        end
                    end
                else 
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
                end
            end)
        end
    end
end)

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto Electric Claw',
    Default = false,
    Tooltip = 'Auto Electric Claw',

    Callback = function(v)
        _G.Auto_ElectricClaw = v
    end
})

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto SharkMan Karate',
    Default = false,
    Tooltip = 'Auto SharkMan Karate',

    Callback = function(v)
        _G.Auto_Sharkman_Karate = v
    end
})

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto Dragon Talon',
    Default = false,
    Tooltip = 'Auto SharkMan Karate',

    Callback = function(v)
        _G.Auto_Sharkman_Karate = v
    end
})

FightingStyle:AddToggle('MyToggle', {
    Text = 'Auto God Human',
    Default = false,
    Tooltip = 'Auto God Human',

    Callback = function(v)
        _G.Auto_Godhuman = v
    end
})

Tab1:AddLabel(' // Main \\\\')

Setting:AddDropdown('MyDropdown', {
    Values = {"Melee","Sword","Fruit"},
    Default = 0,
    Multi = false,

    Text = 'Select Weapon',
    Tooltip = 'Select Weapon',

    Callback = function(v)
        _G.ChooseWeapon = v
    end
})


task.spawn(function()
	while wait() do
		pcall(function()
			if _G.ChooseWeapon == "Melee" then
				for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
					if v.ToolTip == "Melee" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							_G.SelectWeapon = v.Name
						end
					end
				end
			elseif _G.ChooseWeapon == "Sword" then
				for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
					if v.ToolTip == "Sword" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							_G.SelectWeapon = v.Name
						end
					end
				end
			elseif _G.ChooseWeapon == "Fruit" then
				for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
					if v.ToolTip == "Blox Fruit" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							_G.SelectWeapon = v.Name
						end
					end
				end
			else
				for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
					if v.ToolTip == "Melee" then
						if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
							_G.SelectWeapon = v.Name
						end
					end
				end
			end
		end)
	end
end)

-- [require module]
local CombatFramework = require(game:GetService("Players").LocalPlayer.PlayerScripts:WaitForChild("CombatFramework"))
local CombatFrameworkR = getupvalues(CombatFramework)[2]
local RigController = require(game:GetService("Players")["LocalPlayer"].PlayerScripts.CombatFramework.RigController)
local RigControllerR = getupvalues(RigController)[2]
local realbhit = require(game.ReplicatedStorage.CombatFramework.RigLib)
local cooldownfastattack = tick()

function CameraShaker() 
local Camera = require(game.ReplicatedStorage.Util.CameraShaker)
Camera:Stop()
end
-- [FastAttack]
function CurrentWeapon()
local ac = CombatFrameworkR.activeController
local ret = ac.blades[1]
if not ret then return game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name end
pcall(function()
while ret.Parent ~= game.Players.LocalPlayer.Character do ret = ret.Parent end
end)
if not ret then return game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool").Name end
return ret
end

function getAllBladeHits(Sizes)
    local Hits = {}
    local Client = game.Players.LocalPlayer
    local Characters = workspace.Characters:GetChildren()
    local Enemies = game:GetService("Workspace").Enemies:GetChildren()
    for i = 1, #Enemies do
    local v = Enemies[i]
    local Human = v:FindFirstChildOfClass("Humanoid")
    if Human and Human.RootPart and Human.Health > 0 and Client:DistanceFromCharacter(Human.RootPart.Position) <= Sizes + 5 then
        table.insert(Hits, Human.RootPart)
    end
    end
    for i=1,#Characters do local v = Characters[i]
        if v ~= game.Players.LocalPlayer.Character then
            local Human = v:FindFirstChildOfClass("Humanoid")
            if Human and Human.RootPart and Human.Health > 0 and Client:DistanceFromCharacter(Human.RootPart.Position) <= Sizes + 5 then
                table.insert(Hits,Human.RootPart)
            end
        end
    end
    return Hits
    end

    function yakmefan()
        local ac = CombatFrameworkR.activeController
        if ac and ac.equipped then
         for Ryuen = 1, 1 do
            local bladehit = getAllBladeHits(100)
            if #bladehit > 0 then
                local AcAttack8 = debug.getupvalue(ac.attack, 5)
                local AcAttack9 = debug.getupvalue(ac.attack, 6)
                local AcAttack7 = debug.getupvalue(ac.attack, 4)
                local AcAttack10 = debug.getupvalue(ac.attack, 7)
                local NumberAc12 = (AcAttack8 * 798405 + AcAttack7 * 727595) % AcAttack9
                local NumberAc13 = AcAttack7 * 798405
                (function() 
                    NumberAc12 = (NumberAc12 * AcAttack9 + NumberAc13) % 1099511627776
                    AcAttack8 = math.floor(NumberAc12 / AcAttack9)
                    AcAttack7 = NumberAc12 - AcAttack8 * AcAttack9
                end)()
                AcAttack10 = AcAttack10 + 1
                debug.setupvalue(ac.attack, 5, AcAttack8)
                debug.setupvalue(ac.attack, 6, AcAttack9)
                debug.setupvalue(ac.attack, 4, AcAttack7)
                debug.setupvalue(ac.attack, 7, AcAttack10)
                for k, v in pairs(ac.animator.anims.basic) do
                    v:Play(0.01, 0.01, 0.01)
                end
                if game.Players.LocalPlayer.Character:FindFirstChildOfClass("Tool") and ac.blades and ac.blades[1] then
                    game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("weaponChange",tostring(CurrentWeapon()))
                    game.ReplicatedStorage.Remotes.Validator:FireServer(math.floor(NumberAc12 / 1099511627776 * 16777215), AcAttack10)
                    game:GetService("ReplicatedStorage").RigControllerEvent:FireServer("hit", bladehit, 1, "")
                end
            end
        end
        end
        end
 
                coroutine.wrap(function()
                    while task.wait(0) do
                        local ac = CombatFrameworkR.activeController
                        if ac and ac.equipped then
                            task.wait(0.05)
                            if FastAttack or _G.FastAttack then
                                yakmefan()
                                if _G.FastType == "Normal" then
                                    if tick() - cooldownfastattack > .9 then wait(.1) cooldownfastattack = tick() end
                                elseif _G.FastType == "Fast" then
                                    if tick() - cooldownfastattack > 1.5 then wait(.01) cooldownfastattack = tick() end
                                elseif _G.FastType == "Slow" then
                                    if tick() - cooldownfastattack > .3 then wait(.7) cooldownfastattack = tick() end
                                end
                                setscriptable(game.Players.LocalPlayer, "SimulationRadius", true)
                                sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                            end
                        end
                    end
                end)()
                _G.FastType = "Fast" 
Setting:AddToggle('MyToggle', {
    Text = 'Fast Attack',
    Default = true,
    Tooltip = 'ระวังเด้ง เพราะ มันเป็นตัวเบต้า',
    Callback = function(v)
        _G.FastAttack = v
    end
})

Setting:AddToggle('MyToggle', {
    Text = 'Disabled Damage',
    Default = false,
   -- Tooltip = 'Insant Teleport',
    Callback = function(v)
        _G.MassDaHeegeen = v
spawn(function()
	while wait() do
		if _G.MassDaHeegeen then
			game:GetService("ReplicatedStorage").Assets.GUI.DamageCounter.Enabled = false
		else
			game:GetService("ReplicatedStorage").Assets.GUI.DamageCounter.Enabled = true
		end
	end
end)
    end
})
Setting:AddToggle('MyToggle', {
    Text = 'Insant Teleport',
    Default = true,
    Tooltip = 'Insant Teleport',
    Callback = function(v)
        _G.Insant_TP = v
        BypassTP = v 
    end
})

_G.Set = true
spawn(function()
    while wait() do
        if _G.Set then
            pcall(function()
                local args = {
                [1] = "SetSpawnPoint"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end)
        end
    end
end)
_G.BringMonster = true

spawn(function()
	while task.wait() do
		pcall(function()
			if _G.BringMonster and BringMob then
				CheckQuest()
				for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
					if _G.Auto_Farm_Level and BringMob and v.Name == MonFarm and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 220 then
						v.HumanoidRootPart.Size = Vector3.new(50,50,50)
						v.HumanoidRootPart.CFrame = FarmPos
						v.Humanoid:ChangeState(14)
						v.HumanoidRootPart.CanCollide = false
						v.Head.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
					elseif _G.Auto_Farm_Level and BringMob and v.Name == MonFarm and v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 300 then
						v.HumanoidRootPart.Size = Vector3.new(50,50,50)
						v.HumanoidRootPart.CFrame = FarmPos
						v.Humanoid:ChangeState(14)
						v.HumanoidRootPart.CanCollide = false
						v.Head.CanCollide = false
						if v.Humanoid:FindFirstChild("Animator") then
							v.Humanoid.Animator:Destroy()
						end
						sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
					elseif v.Name == MonFarm then 
						if (v.HumanoidRootPart.Position - FarmPos.Position).Magnitude <= 300 then
							v.HumanoidRootPart.Size = Vector3.new(50,50,50)
							v.HumanoidRootPart.CFrame = FarmPos
							v.Humanoid:ChangeState(14)
							v.HumanoidRootPart.CanCollide = false
							v.Head.CanCollide = false
							if v.Humanoid:FindFirstChild("Animator") then
								v.Humanoid.Animator:Destroy()
							end
							sethiddenproperty(game:GetService("Players").LocalPlayer,"SimulationRadius",math.huge)
						end
					end
				end
			end
		end)
	end
end)


Misc5:AddToggle('MyToggle', {
    Text = 'Auto Haki',
    Default = true,
    Tooltip = 'Auto Haki',

    Callback = function(v)
        _G.AutoHaki = v
    end
})
spawn(function()
    while wait() do
        if _G.AutoHaki then
            AutoHaki()
        end
    end
end)
Misc5:AddToggle('MyToggle', {
    Text = 'Auto Ken',
    Default = false,
    Tooltip = 'Auto Ken',

    Callback = function(v)
        _G.Auto_Haki_Ken = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Haki_Ken then
            local args = {
                [1] = "Ken",
                [2] = true
            }
        
            game:GetService("ReplicatedStorage").Remotes.CommE:FireServer(unpack(args))
        end
    end
end)

Setting:AddButton({
    Text = 'Redeem All Code',
    Func = function()
        function UseCode(Text)
            game:GetService("ReplicatedStorage").Remotes.Redeem:InvokeServer(Text)
        end
        UseCode("Sub2UncleKizaru")
        UseCode("SUB2NOOBMASTER123")
        UseCode("StrawHatMaine")
        UseCode("Sub2OfficialNoobie")
        UseCode("SUB2GAMERROBOT_EXP1")
        UseCode("SUB2GAMERROBOT_RESET1")
        UseCode("THEGREATACE")
        UseCode("BIGNEWS")
        UseCode("FUDD10")
        UseCode("fudd10_v2")
        UseCode("Bluxxy")
        UseCode("Starcodeheo")
        UseCode("JCWK")
        UseCode("Magicbus")
        UseCode("Sub2Fer999")
        UseCode("kittgaming")
        UseCode("GAMERROBOT")
        UseCode("SUBGAMERROBOT")
        UseCode("ADMINGIVEAWAY")
        UseCode("KITT_RESET")
        UseCode("SECRET_ADMIN")
        UseCode("Sub2Daigrock")
        UseCode("Axiore")
        UseCode("TantaiGaming")
        UseCode("DEVSCOOKING")
        UseCode("Sub2CaptainMaui")
        UseCode("KITT_RESET")
        UseCode("NEWTROLL")
    end,
    DoubleClick = false,
    Tooltip = 'Redeem All Code'
})




Stats:AddToggle('MyToggle', {
    Text = 'Up Stats Melee',
    Default = false,
    Tooltip = 'Up Stats Melee',

    Callback = function(v)
        _G.Auto_Stats_Melee = v
    end
})

Stats:AddToggle('MyToggle', {
    Text = 'Up Stats Defense',
    Default = false,
    Tooltip = 'Up Stats Defense',

    Callback = function(v)
        _G.Auto_Stats_Defense = v
    end
})
Stats:AddToggle('MyToggle', {
    Text = 'Up Stats Sword',
    Default = false,
    Tooltip = 'Up Stats Sword',

    Callback = function(v)
        _G.Auto_Stats_Sword = v
    end
})
Stats:AddToggle('MyToggle', {
    Text = 'Up Stats Gun',
    Default = false,
    Tooltip = 'Up Stats Gun',

    Callback = function(v)
        _G.Auto_Stats_Gun = v
    end
})
Stats:AddToggle('MyToggle', {
    Text = 'Auto Up Fruit',
    Default = false,
    Tooltip = 'Auto Up Fruit',

    Callback = function(v)
        _G.Auto_Stats_Devil_Fruit = v
    end
})
Stats:AddSlider('MySlider', {
    Text = 'Point',
    Default = 3,
    Min = 0,
    Max = 10,
    Rounding = 0,
    Compact = false,

    Callback = function(v)
        _G.P = v
    end
})

spawn(function()
	while wait() do
		if _G.Auto_Stats_Devil_Fruit then
			local args = {
				[1] = "AddPoint",
				[2] = "Demon Fruit",
				[3] = _G.P
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end
	end
end)

spawn(function()
	while wait() do
		if _G.Auto_Stats_Gun then
			local args = {
				[1] = "AddPoint",
				[2] = "Gun",
				[3] = _G.P
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end
	end
end)


spawn(function()
	while wait() do
		if _G.Auto_Stats_Sword then
			local args = {
				[1] = "AddPoint",
				[2] = "Sword",
				[3] = _G.P
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end
	end
end)

spawn(function()
	while wait() do
		if _G.Auto_Stats_Defense then
			local args = {
				[1] = "AddPoint",
				[2] = "Defense",
				[3] = _G.P
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end
	end
end)


spawn(function()
	while wait() do
		if _G.Auto_Stats_Melee then
			local args = {
				[1] = "AddPoint",
				[2] = "Melee",
				[3] = _G.P
			}

			game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
		end
	end
end)


if World1 then
    Island = {
        "WindMill",
        "Marine",
        "Middle Town",
        "Jungle",
        "Pirate Village",
        "Desert",
        "Snow Island",
        "MarineFord",
        "Colosseum",
        "Sky Island 1",
        "Sky Island 2",
        "Sky Island 3",
        "Prison",
        "Magma Village",
        "Under Water Island",
        "Fountain City",
        "Shank Room",
        "Mob Island"
    }
elseif World2 then
    Island = {
        "The Cafe",
        "Frist Spot",
        "Dark Area",
        "Flamingo Mansion",
        "Flamingo Room",
        "Green Zone",
        "Factory",
        "Colossuim",
        "Zombie Island",
        "Two Snow Mountain",
        "Punk Hazard",
        "Cursed Ship",
        "Ice Castle",
        "Forgotten Island",
        "Ussop Island",
        "Mini Sky Island"
    }
elseif World3 then
    Island = {
        "Mansion",
        "Port Town",
        "Great Tree",
        "Castle On The Sea",
        "MiniSky", 
        "Hydra Island",
        "Floating Turtle",
        "Haunted Castle",
        "Ice Cream Island",
        "Peanut Island",
        "Cake Island",
        "Tiki Outpost"
    }	
end



Teleport:AddDropdown('MyDropdown', {
    Values = Island,
    Default = 1,
    Multi = false,

    Text = 'Select Island',
    Tooltip = 'Select Island',

    Callback = function(Value)
        _G.Select_Island = Value
    end
})

Teleport:AddToggle('MyToggle', {
    Text = 'Teleport To Island',
    Default = false,
    Tooltip = '',

    Callback = function(v)
        _G.Start_Tween_Island = v
        if _G.Start_Tween_Island == true  then
            repeat wait()
                if _G.Select_Island == "WindMill" then
                   Tween(CFrame.new(979.79895019531, 16.516613006592, 1429.0466308594))
                elseif _G.Select_Island == "Marine" then
                   Tween(CFrame.new(-2566.4296875, 6.8556680679321, 2045.2561035156))
                elseif _G.Select_Island == "Middle Town" then
                   Tween(CFrame.new(-690.33081054688, 15.09425163269, 1582.2380371094))
                elseif _G.Select_Island == "Jungle" then
                   Tween(CFrame.new(-1612.7957763672, 36.852081298828, 149.12843322754))
                elseif _G.Select_Island == "Pirate Village" then
                   Tween(CFrame.new(-1181.3093261719, 4.7514905929565, 3803.5456542969))
                elseif _G.Select_Island == "Desert" then
                   Tween(CFrame.new(944.15789794922, 20.919729232788, 4373.3002929688))
                elseif _G.Select_Island == "Snow Island" then
                   Tween(CFrame.new(1347.8067626953, 104.66806030273, -1319.7370605469))
                elseif _G.Select_Island == "MarineFord" then
                   Tween(CFrame.new(-4914.8212890625, 50.963626861572, 4281.0278320313))
                elseif _G.Select_Island == "Colosseum" then
                   Tween( CFrame.new(-1427.6203613281, 7.2881078720093, -2792.7722167969))
                elseif _G.Select_Island == "Sky Island 1" then
                   Tween(CFrame.new(-4869.1025390625, 733.46051025391, -2667.0180664063))
                elseif _G.Select_Island == "Sky Island 2" then  
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
                elseif _G.Select_Island == "Sky Island 3" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
                elseif _G.Select_Island == "Prison" then
                   Tween( CFrame.new(4875.330078125, 5.6519818305969, 734.85021972656))
                elseif _G.Select_Island == "Magma Village" then
                   Tween(CFrame.new(-5247.7163085938, 12.883934020996, 8504.96875))
                elseif _G.Select_Island == "Under Water Island" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
                elseif _G.Select_Island == "Fountain City" then
                   Tween(CFrame.new(5127.1284179688, 59.501365661621, 4105.4458007813))
                elseif _G.Select_Island == "Shank Room" then
                   Tween(CFrame.new(-1442.16553, 29.8788261, -28.3547478))
                elseif _G.Select_Island == "Mob Island" then
                   Tween(CFrame.new(-2850.20068, 7.39224768, 5354.99268))
                elseif _G.Select_Island == "The Cafe" then
                   Tween(CFrame.new(-380.47927856445, 77.220390319824, 255.82550048828))
                elseif _G.Select_Island == "Frist Spot" then
                   Tween(CFrame.new(-11.311455726624, 29.276733398438, 2771.5224609375))
                elseif _G.Select_Island == "Dark Area" then
                   Tween(CFrame.new(3780.0302734375, 22.652164459229, -3498.5859375))
                elseif _G.Select_Island == "Flamingo Mansion" then
                   Tween(CFrame.new(-483.73370361328, 332.0383605957, 595.32708740234))
                elseif _G.Select_Island == "Flamingo Room" then
                   Tween(CFrame.new(2284.4140625, 15.152037620544, 875.72534179688))
                elseif _G.Select_Island == "Green Zone" then
                   Tween( CFrame.new(-2448.5300292969, 73.016105651855, -3210.6306152344))
                elseif _G.Select_Island == "Factory" then
                   Tween(CFrame.new(424.12698364258, 211.16171264648, -427.54049682617))
                elseif _G.Select_Island == "Colossuim" then
                   Tween( CFrame.new(-1503.6224365234, 219.7956237793, 1369.3101806641))
                elseif _G.Select_Island == "Zombie Island" then
                   Tween(CFrame.new(-5622.033203125, 492.19604492188, -781.78552246094))
                elseif _G.Select_Island == "Two Snow Mountain" then
                   Tween(CFrame.new(753.14288330078, 408.23559570313, -5274.6147460938))
                elseif _G.Select_Island == "Punk Hazard" then
                   Tween(CFrame.new(-6127.654296875, 15.951762199402, -5040.2861328125))
                elseif _G.Select_Island == "Cursed Ship" then
                   Tween(CFrame.new(923.40197753906, 125.05712890625, 32885.875))
                elseif _G.Select_Island == "Ice Castle" then
                   Tween(CFrame.new(6148.4116210938, 294.38687133789, -6741.1166992188))
                elseif _G.Select_Island == "Forgotten Island" then
                   Tween(CFrame.new(-3032.7641601563, 317.89672851563, -10075.373046875))
                elseif _G.Select_Island == "Ussop Island" then
                   Tween(CFrame.new(4816.8618164063, 8.4599885940552, 2863.8195800781))
                elseif _G.Select_Island == "Mini Sky Island" then
                   Tween(CFrame.new(-288.74060058594, 49326.31640625, -35248.59375))
                elseif _G.Select_Island == "Great Tree" then
                   Tween(CFrame.new(2681.2736816406, 1682.8092041016, -7190.9853515625))
                elseif _G.Select_Island == "Castle On The Sea" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-5076.60107, 314.54129, -3152.13086, 0.351963997, -4.56893581e-08, -0.93601352, 6.84364423e-08, 1, -2.30789325e-08, 0.93601352, -5.59344855e-08, 0.351963997))
                elseif _G.Select_Island == "MiniSky" then
                   Tween(CFrame.new(-260.65557861328, 49325.8046875, -35253.5703125))
                elseif _G.Select_Island == "Port Town" then
                   Tween(CFrame.new(-290.7376708984375, 6.729952812194824, 5343.5537109375))
                elseif _G.Select_Island == "Hydra Island" then
                   Tween(CFrame.new(5228.8842773438, 604.23400878906, 345.0400390625))
                elseif _G.Select_Island == "Floating Turtle" then
                   Tween(CFrame.new(-13274.528320313, 531.82073974609, -7579.22265625))
                elseif _G.Select_Island == "Mansion" then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-12471.169921875, 374.94024658203, -7551.677734375))
                elseif _G.Select_Island == "Haunted Castle" then
                   Tween(CFrame.new(-9515.3720703125, 164.00624084473, 5786.0610351562))
                elseif _G.Select_Island == "Ice Cream Island" then
                   Tween(CFrame.new(-902.56817626953, 79.93204498291, -10988.84765625))
                elseif _G.Select_Island == "Peanut Island" then
                   Tween(CFrame.new(-2062.7475585938, 50.473892211914, -10232.568359375))
                elseif _G.Select_Island == "Cake Island" then
                   Tween(CFrame.new(-1884.7747802734375, 19.327526092529297, -11666.8974609375))
                elseif _G.Select_Island == "Tiki Outpost" then
                   Tween(CFrame.new(-16753.5977, 189.528107, 451.797333, -0.777145505, 0, -0.629321039, 0, 1, 0, 0.629321039, 0, -0.777145505))
                end
            until not _G.Start_Tween_Island
        end
    end
})



DevilFruit:AddToggle('MyToggle', {
    Text = 'Auto Buy Random Fruit',
    Default = false,
    Tooltip = 'Auto Buy Random Fruit',

    Callback = function(v)
        _G.Auto_Random_Fruit = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Random_Fruit then	
            local args = {
                [1] = "Cousin",
                [2] = "Buy"
            }
            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        end
    end
end)
DevilFruit:AddButton({
    Text = 'Buy Random Fruit',
    Func = function()
        local args = {
            [1] = "Cousin",
            [2] = "Buy"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end,
    DoubleClick = false,
    Tooltip = 'Buy Random Fruit'
})

local Remote_GetFruits = game.ReplicatedStorage:FindFirstChild("Remotes").CommF_:InvokeServer("GetFruits");
	
	Table_DevilFruitSniper = {}
	ShopDevilSell = {}
	
	for i,v in next,Remote_GetFruits do
		table.insert(Table_DevilFruitSniper,v.Name)
		if v.OnSale then 
			table.insert(ShopDevilSell,v.Name)
		end
	end

DevilFruit:AddDropdown('MyMultiDropdown', {

    Values = Table_DevilFruitSniper,
    Default = 0,
    Multi = true,

    Text = 'Select Devil Fruit',
    Tooltip = 'Select Devil Fruit',

    Callback = function(v)
        _G.Select_Devil_Fruit = v
    end
})

DevilFruit:AddToggle('MyToggle', {
    Text = 'Auto Bring Fruit',
    Default = false,
    Tooltip = 'Auto Buy Random Fruit',

    Callback = function(v)
        _G.Auto_Bring_Fruit = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Bring_Fruit then
            pcall(function()
                for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
                    if v:IsA("Tool") and string.find(v.Name,"Fruit") then 
                        if (v.Handle.CFrame.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 1500 then
                            game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame * CFrame.new(0,50,0)
                            repeat wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame * CFrame.new(0,50,0) until (v.Handle.CFrame.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1 or not _G.Auto_Bring_Fruit
                            repeat wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame until (v.Handle.CFrame.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1 or not _G.Auto_Bring_Fruit
                        else
                            repeat wait() game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame until (v.Handle.CFrame.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 1 or not _G.Auto_Bring_Fruit
                        end
                    end
                end
            end)
        end
    end
end)

DevilFruit:AddToggle('MyToggle', {
    Text = 'Auto Store Fruit',
    Default = false,
    Tooltip = 'Auto Store Fruit',

    Callback = function(v)
        _G.Auto_Store_Fruit = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Store_Fruit then
            pcall(function()
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bomb Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bomb Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Bomb-Bomb",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bomb Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bomb Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spike Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spike Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Spike-Spike",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spike Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spike Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Chop Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Chop Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Chop-Chop",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Chop Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Chop Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spring Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spring Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Spring-Spring",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spring Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spring Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Kilo Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Kilo Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Kilo-Kilo",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Kilo Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Kilo Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Smoke Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Smoke Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Smoke-Smoke",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Smoke Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Smoke Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spin Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spin Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Spin-Spin",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Spin Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Spin Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flame Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flame Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Flame-Flame",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flame Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flame Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Falcon Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Falcon Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Bird-Bird: Falcon",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Falcon Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Falcon Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Ice Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Ice Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Ice-Ice",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Ice Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Ice Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Sand Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Sand Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Sand-Sand",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Sand Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Sand Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dark Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dark Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Dark-Dark",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dark Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dark Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Revive Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Revive Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Revive-Revive",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Revive Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Revive Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Diamond Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Diamond Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Diamond-Diamond",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Diamond Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Diamond Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Light Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Light Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Light-Light",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Light Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Light Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Love Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Love Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Love-Love",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Love Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Love Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rubber Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rubber Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Rubber-Rubber",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rubber Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rubber Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Barrier Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Barrier Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Barrier-Barrier",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Barrier Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Barrier Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Magma Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Magma Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Magma-Magma",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Magma Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Magma Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Door Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Door Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Door-Door",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Door Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Door Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Quake Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Quake Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Quake-Quake",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Quake Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Quake Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Human-Human: Buddha Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Human-Human: Buddha Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Human-Human: Buddha",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Human-Human: Buddha Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Human-Human: Buddha Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("String Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("String Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","String-String",game:GetService("Players").LocalPlayer.Character:FindFirstChild("String Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("String Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Phoenix Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Phoenix Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Bird-Bird: Phoenix",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Bird: Phoenix Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Bird: Phoenix Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rumble Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rumble Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Rumble-Rumble",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Rumble Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Rumble Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Paw Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Paw Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Paw-Paw",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Paw Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Paw Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Gravity Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Gravity Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Gravity-Gravity",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Gravity Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Gravity Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dough Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dough Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Dough-Dough",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dough Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dough Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Shadow Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Shadow Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Shadow-Shadow",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Shadow Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Shadow Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Venom Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Venom Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Venom-Venom",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Venom Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Venom Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Control Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Control Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Control-Control",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Control Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Control Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dragon Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Dragon-Dragon",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Dragon Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Dragon Fruit"))
                end
                if game:GetService("Players").LocalPlayer.Character:FindFirstChild("Leopard Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Leopard Fruit") then
                    game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StoreFruit","Leopard-Leopard",game:GetService("Players").LocalPlayer.Character:FindFirstChild("Leopard Fruit") or game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Leopard Fruit"))
                end
            end)
        end
    end
end)


RaceV4:AddToggle('MyToggle', {
    Text = 'Auto Evo Race V2',
    Default = false,
    Tooltip = 'Auto Evo Race V2',

    Callback = function(v)
        _G.Auto_EvoRace = v
		StopTween(_G.Auto_EvoRace)
    end
})

spawn(function()
    pcall(function()
        while wait(.1) do
            if _G.Auto_EvoRace then
                if not game:GetService("Players").LocalPlayer.Data.Race:FindFirstChild("Evolved") then
                    if game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Alchemist","1") == 0 then
                        Tween(CFrame.new(-2779.83521, 72.9661407, -3574.02002, -0.730484903, 6.39014104e-08, -0.68292886, 3.59963224e-08, 1, 5.50667032e-08, 0.68292886, 1.56424669e-08, -0.730484903))
                        if (Vector3.new(-2779.83521, 72.9661407, -3574.02002) - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 4 then
                            wait(1.3)
                            game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Alchemist","2")
                        end
                    elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Alchemist","1") == 1 then
                        pcall(function()
                            if not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flower 1") and not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flower 1") then
                                Tween(game:GetService("Workspace").Flower1.CFrame)
                            elseif not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flower 2") and not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flower 2") then
                                Tween(game:GetService("Workspace").Flower2.CFrame)
                            elseif not game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flower 3") and not game:GetService("Players").LocalPlayer.Character:FindFirstChild("Flower 3") then
                                if game:GetService("Workspace").Enemies:FindFirstChild("Zombie") then
                                    for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
                                        if v.Name == "Zombie" then
                                            repeat task.wait()
                                                AutoHaki()
                                                EquipTool(_G.SelectWeapon)
yakmefan()
                                                Tween(v.HumanoidRootPart.CFrame * CFrame.new(2,20,2))
                                                v.HumanoidRootPart.CanCollide = false
                                                v.HumanoidRootPart.Size = Vector3.new(50,50,50)
                                                
                                                FarmPos = v.HumanoidRootPart.CFrame
                                                MonFarm = v.Name
                                                BringMob = true
                                            until game:GetService("Players").LocalPlayer.Backpack:FindFirstChild("Flower 3") or not v.Parent or v.Humanoid.Health <= 0 or _G.Auto_EvoRace == false
                                            BringMob = false
                                        end
                                    end
                                else
                                    BringMob = false
                                    Tween(CFrame.new(-5685.9233398438, 48.480125427246, -853.23724365234))
                                end
                            end
                        end)
                    elseif game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Alchemist","1") == 2 then
                        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Alchemist","3")
                    end
                end
            end
        end
    end)
end)




RaceV4:AddButton({
    Text = 'Teleport To Lever',
    Func = function()
        Tween(CFrame.new(28577.1641, 14907.3477, -87.3899612, 0, 0, -1, 0, 1, 0, 1, 0, 0))
    end,
    DoubleClick = false,
    Tooltip = 'Teleport To Lever'
})

RaceV4:AddButton({
    Text = 'Teleport To Trail Door',
    Func = function()
        if game:GetService("Players").LocalPlayer.Data.Race.Value == "Skypiea" then
            Tween(CFrame.new(28967.408203125, 14918.0751953125, 234.31198120117188))
        elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Mink" then
            Tween(CFrame.new(29020.66015625, 14889.4267578125, -379.2682800292969))
        elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Cyborg" then
            Tween(CFrame.new(28492.4140625, 14894.4267578125, -422.1100158691406))
        elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Human" then
            Tween(CFrame.new(29237.294921875, 14889.4267578125, -206.94955444335938))
        elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Fishman" then
            Tween(CFrame.new(28224.056640625, 14889.4267578125, -210.5872039794922))
        end 
    end,
    DoubleClick = false,
    Tooltip = 'Teleport To Trail Door'
})


RaceV4:AddToggle('MyToggle', {
    Text = 'Auto Complete Trial',
    Default = false,
    Tooltip = 'Auto Complete Trial',

    Callback = function(v)
        _G.Auto_Complete_Trial = v
    end
})
spawn(function()
	while wait() do
		if _G.Auto_Complete_Trial then
			pcall(function()
				if (game:GetService("Workspace").Map["Temple of Time"].DoNotEnter.CFrame.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude >= 2000 then
					game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map["Temple of Time"].DoNotEnter.CFrame
				else
					if game:GetService("Players").LocalPlayer.Data.Race.Value == "Skypiea" then
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Map.SkyTrial.Model.FinishPart.CFrame
					elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Mink" then
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game:GetService("Workspace").Map.MinkTrial.Ceiling.CFrame * CFrame.new(0, -5, 0)
					elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Cyborg" then
						game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame * CFrame.new(0, 300, 0)
					elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Human" then
							for i,v in pairs(game.Workspace.Enemies:GetChildren()) do
								if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 1000 then
									repeat wait()
										v.HumanoidRootPart.Size = Vector3.new(60,60,60)
										v.HumanoidRootPart.CanCollide = false
										v.Humanoid.WalkSpeed = 0
										v.Head.CanCollide = false
										BringMob = true
										EquipTool(_G.SelectWeapon)
yakmefan()
										FarmPos = v.HumanoidRootPart.CFrame
                                        MonFarm = v.Name
										v.HumanoidRootPart.Transparency = 1
										Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,40,0))
									until not _G.Auto_Complete_Trial or not v.Parent or v.Humanoid.Health <= 0
									BringMob = false
								end
							end
					elseif game:GetService("Players").LocalPlayer.Data.Race.Value == "Fishman" then
							for i,v in pairs(game:GetService("Workspace").SeaBeasts:GetChildren()) do
								if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 and (v.HumanoidRootPart.Position-game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).magnitude <= 1000 then
									repeat wait()
										v.HumanoidRootPart.Size = Vector3.new(150,150,150)
										v.HumanoidRootPart.CanCollide = false
										v.Humanoid.WalkSpeed = 0
										v.Head.CanCollide = false
										v.HumanoidRootPart.Transparency = 1
										Tween(v.HumanoidRootPart.CFrame * CFrame.new(0,40,0))
										for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
											if v.ToolTip == "Sword" then
												if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
													EquipTool(v.Name)
												end
											end
										end
										game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
										game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
										wait(0.2)
										game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
										game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
										for i ,v in pairs(game.Players.LocalPlayer.Backpack:GetChildren()) do
											if v.ToolTip == "Blox Fruit" then
												if game.Players.LocalPlayer.Backpack:FindFirstChild(tostring(v.Name)) then
													EquipTool(v.Name)
												end
											end
										end
										game:GetService("VirtualInputManager"):SendKeyEvent(true,"Z",false,game)
										game:GetService("VirtualInputManager"):SendKeyEvent(false,"Z",false,game)
										wait(0.2)
										game:GetService("VirtualInputManager"):SendKeyEvent(true,"X",false,game)
										game:GetService("VirtualInputManager"):SendKeyEvent(false,"X",false,game)
										wait(0.2)
										game:GetService("VirtualInputManager"):SendKeyEvent(true,"C",false,game)
										game:GetService("VirtualInputManager"):SendKeyEvent(false,"C",false,game)
										wait(0.2)
										game:GetService("VirtualInputManager"):SendKeyEvent(true,"V",false,game)
										game:GetService("VirtualInputManager"):SendKeyEvent(false,"V",false,game)
										wait(0.2)
										game:GetService'VirtualUser':CaptureController()
										game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
									until not _G.Auto_Complete_Trial or not v.Parent or v.Humanoid.Health <= 0
									BringMob = false
								end
							end
					end
				end
			end)
		end
	end
end)
local MyButton = Fragment:AddButton({
    Text = 'Reset Stuts Point',
    Func = function()
        local args = {
            [1] = "BlackbeardReward",
            [2] = "Refund",
            [3] = "2"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end,
    DoubleClick = false,
    Tooltip = 'Reset Stuts Point'
})

local MyButton = Fragment:AddButton({
    Text = 'Reroll Race',
    Func = function()
        local args = {
            [1] = "BlackbeardReward",
            [2] = "Reroll",
            [3] = "2"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end,
    DoubleClick = false,
    Tooltip = 'Reroll Race'
})

local MyButton = Abilities:AddButton({
    Text = 'Buso Haki',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki","Buso")
    end,
    DoubleClick = false,
    Tooltip = 'Buso Haki'
})

local MyButton = Abilities:AddButton({
    Text = 'Geppo',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki","Geppo")
    end,
    DoubleClick = false,
    Tooltip = 'Geppo'
})

local MyButton = Abilities:AddButton({
    Text = 'Soru',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki","Soru")
    end,
    DoubleClick = false,
    Tooltip = 'Soru'
})

local MyButton = Abilities:AddButton({
    Text = 'Ken Haki',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("KenTalk","Buy")
    end,
    DoubleClick = false,
    Tooltip = 'Ken Haki'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Black Leg',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg")
    end,
    DoubleClick = false,
    Tooltip = 'Black Leg'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Electro',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro")
    end,
    DoubleClick = false,
    Tooltip = 'Electro'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Fishman Karate',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate")
    end,
    DoubleClick = false,
    Tooltip = 'Fishman Karate'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Dragon Claw',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","1")
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
    end,
    DoubleClick = false,
    Tooltip = 'Dragon Claw'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Superhuman',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman")
    end,
    DoubleClick = false,
    Tooltip = 'Superhuman'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Death Step',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep")
    end,
    DoubleClick = false,
    Tooltip = 'Death Step'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Sharkman Karate',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate",true)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate")
    end,
    DoubleClick = false,
    Tooltip = 'Sharkman Karate'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Eletric Claw',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw")
    end,
    DoubleClick = false,
    Tooltip = 'Eletric Claw'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Dragon Talon',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon")
    end,
    DoubleClick = false,
    Tooltip = 'Dragon Talon'
})

local MyButton = FightingStyleShop:AddButton({
    Text = 'Godhuman',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman")
    end,
    DoubleClick = false,
    Tooltip = 'Godhuman'
})

local MyButton = Sword:AddButton({
    Text = 'Katana',
    Func = function()
        
    end,
    DoubleClick = false,
    Tooltip = 'Katana'
})

local MyButton = Sword:AddButton({
    Text = 'Cutlass',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Cutlass")
    end,
    DoubleClick = false,
    Tooltip = 'Cutlass'
})

local MyButton = Sword:AddButton({
    Text = 'Duel Katana',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Duel Katana")
    end,
    DoubleClick = false,
    Tooltip = 'Duel Katana'
})

local MyButton = Sword:AddButton({
    Text = 'Iron Mace',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Iron Mace")
    end,
    DoubleClick = false,
    Tooltip = 'Iron Mace'
})

local MyButton = Sword:AddButton({
    Text = 'Pipe',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Pipe")
    end,
    DoubleClick = false,
    Tooltip = 'Pipe'
})

local MyButton = Sword:AddButton({
    Text = 'Triple Katana',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Triple Katana")
    end,
    DoubleClick = false,
    Tooltip = 'Triple Katana'
})

local MyButton = Sword:AddButton({
    Text = 'Dual Handed Blade',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Dual-Headed Blade")
    end,
    DoubleClick = false,
    Tooltip = 'Dual Handed Blade'
})

local MyButton = Sword:AddButton({
    Text = 'Bisento',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Bisento")
    end,
    DoubleClick = false,
    Tooltip = 'Bisento'
})

local MyButton = Sword:AddButton({
    Text = 'Soul Cane',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Soul Cane")
    end,
    DoubleClick = false,
    Tooltip = 'Soul Cane'
})

local MyButton = Gun:AddButton({
    Text = 'Slingshot',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Slingshot")
    end,
    DoubleClick = false,
    Tooltip = 'Slingshot'
})

local MyButton = Gun:AddButton({
    Text = 'Musket',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Musket")
    end,
    DoubleClick = false,
    Tooltip = 'Musket'
})

local MyButton = Gun:AddButton({
    Text = 'Flintlock',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Flintlock")
    end,
    DoubleClick = false,
    Tooltip = 'Flintlock'
})

local MyButton = Gun:AddButton({
    Text = 'Refind Flintlock',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Refined Flintlock")
    end,
    DoubleClick = false,
    Tooltip = 'Refind Flintlock'
})

local MyButton = Gun:AddButton({
    Text = 'Cannon',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Cannon")
    end,
    DoubleClick = false,
    Tooltip = 'Cannon'
})

local MyButton = Gun:AddButton({
    Text = 'Kabucha',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Slingshot","1")
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Slingshot","2")
    end,
    DoubleClick = false,
    Tooltip = 'Kabucha'
})

local MyButton = Accessory:AddButton({
    Text = 'Black Cape',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Black Cape")
    end,
    DoubleClick = false,
    Tooltip = 'Black Cape'
})

local MyButton = Accessory:AddButton({
    Text = 'Toemo Ring',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Tomoe Ring")
    end,
    DoubleClick = false,
    Tooltip = 'Toemo Ring'
})

local MyButton = Accessory:AddButton({
    Text = 'Swordsman Hat',
    Func = function()
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Swordsman Hat")
    end,
    DoubleClick = false,
    Tooltip = 'Swordsman Hat'
})

Dungeon = {
    "Flame", 
    "Ice", 
    "Quake", 
    "Light",
    "Dark",
    "String",
    "Rumble",
    "Magma",
    "Human: Buddha",
    "Sand",
    "Bird: Phoenix"
}

Raid1:AddDropdown('MyDropdown', {
    Values = Dungeon,
    Default = 0,
    Multi = false,

    Text = 'Select Raid',
    Tooltip = 'Select Raid',

    Callback = function(v)
        _G.Select_Dungeon = v
    end
})

Raid1:AddToggle('MyToggle', {
    Text = 'Auto Buy Chip Dungeon',
    Default = false,
    Tooltip = 'Auto Buy Chip Dungeon',

    Callback = function(v)
        _G.Auto_Buy_Chips_Dungeon = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Buy_Chips_Dungeon then
            pcall(function()
                local args = {
                    [1] = "RaidsNpc",
                    [2] = "Select",
                    [3] = _G.Select_Dungeon
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end)
        end
    end
end)
Raid1:AddToggle('MyToggle', {
    Text = 'Auto Start Dungeon',
    Default = false,
    Tooltip = 'Auto Start Dungeon',

    Callback = function(v)
        _G.Auto_Start_Dungeon = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Start_Dungeon then
            pcall(function()
                if World2 then
                    if not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") then 
                            fireclickdetector(game.Workspace.Map.CircleIsland.RaidSummon2.Button.Main.ClickDetector)
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                       -- XD
                    end
                elseif World3 then
                    if not game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        if game.Players.LocalPlayer.Backpack:FindFirstChild("Special Microchip") then
                            fireclickdetector(game.Workspace.Map["Boat Castle"].RaidSummon2.Button.Main.ClickDetector)
                        end
                    elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                        -- XD
                    end
                end
            end)
        end
    end
end)
Raid1:AddToggle('MyToggle', {
    Text = 'Kill Aura',
    Default = false,
    Tooltip = 'Kill Aura',

    Callback = function(v)
        _G.Kill_Aura = v
    end
})
spawn(function()
    while wait() do
        if _G.Kill_Aura then
            for i,v in pairs(game.Workspace.Enemies:GetDescendants()) do
                if v:FindFirstChild("Humanoid") and v:FindFirstChild("HumanoidRootPart") and v.Humanoid.Health > 0 then
                    pcall(function()
                        repeat wait(.1)
                            v.Humanoid.Health = 0
                            v.HumanoidRootPart.CanCollide = false
                            sethiddenproperty(game.Players.LocalPlayer, "SimulationRadius", math.huge)
                        until not _G.Kill_Aura  or not v.Parent or v.Humanoid.Health <= 0
                    end)
                end
            end
        end
    end
end)
Raid1:AddToggle('MyToggle', {
    Text = 'Auto Next Island',
    Default = false,
    Tooltip = 'Auto Next Island',

    Callback = function(v)
        _G.Auto_Next_Island = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Next_Island then
            if game:GetService("Players")["LocalPlayer"].PlayerGui.Main.Timer.Visible == true and game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") or game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                if game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 5") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 5"].CFrame * CFrame.new(4, 65, 10))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 4") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 4"].CFrame *  CFrame.new(4, 65, 10))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 3") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 3"].CFrame * CFrame.new(4, 65, 10))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 2") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 2"].CFrame * CFrame.new(4, 65, 10))
                elseif game:GetService("Workspace")["_WorldOrigin"].Locations:FindFirstChild("Island 1") then
                    Tween(game:GetService("Workspace")["_WorldOrigin"].Locations["Island 1"].CFrame * CFrame.new(4, 65, 10))
                end
            end
        end
    end
end)
Raid1:AddToggle('MyToggle', {
    Text = 'Auto Awakener',
    Default = false,
    Tooltip = 'Auto Awakener',

    Callback = function(v)
        _G.Auto_Awakener = v
    end
})
spawn(function()
    while wait(.1) do
        if _G.Auto_Awakener then
            pcall(function()
                local args = {
                    [1] = "Awakener",
                    [2] = "Check"
                }

                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
                local args = {
                    [1] = "Awakener",
                    [2] = "Awaken"
                }
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
            end)
        end
    end
end)


Misc1:AddLabel('         // Join Team \\\\')

local MyButton = Misc1:AddButton({
    Text = 'Join Pirates',
    Func = function()
        local args = {
            [1] = "SetTeam",
            [2] = "Pirates"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args)) 
        local args = {
            [1] = "BartiloQuestProgress"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end,
    DoubleClick = false,
    Tooltip = 'Join Pirates'
})

local MyButton = Misc1:AddButton({
    Text = 'Join Marines',
    Func = function()
        local args = {
            [1] = "SetTeam",
            [2] = "Marines"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
        local args = {
            [1] = "BartiloQuestProgress"
        }
        game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer(unpack(args))
    end,
    DoubleClick = false,
    Tooltip = 'Join Marines'
})
function Hop()
    local PlaceID = game.PlaceId
    local AllIDs = {}
    local foundAnything = ""
    local actualHour = os.date("!*t").hour
    local Deleted = false
    function TPReturner()
        local Site;
        if foundAnything == "" then
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100'))
        else
            Site = game.HttpService:JSONDecode(game:HttpGet('https://games.roblox.com/v1/games/' .. PlaceID .. '/servers/Public?sortOrder=Asc&limit=100&cursor=' .. foundAnything))
        end
        local ID = ""
        if Site.nextPageCursor and Site.nextPageCursor ~= "null" and Site.nextPageCursor ~= nil then
            foundAnything = Site.nextPageCursor
        end
        local num = 0;
        for i,v in pairs(Site.data) do
            local Possible = true
            ID = tostring(v.id)
            if tonumber(v.maxPlayers) > tonumber(v.playing) then
                for _,Existing in pairs(AllIDs) do
                    if num ~= 0 then
                        if ID == tostring(Existing) then
                            Possible = false
                        end
                    else
                        if tonumber(actualHour) ~= tonumber(Existing) then
                            local delFile = pcall(function()
                                AllIDs = {}
                                table.insert(AllIDs, actualHour)
                            end)
                        end
                    end
                    num = num + 1
                end
                if Possible == true then
                    table.insert(AllIDs, ID)
                    wait()
                    pcall(function()
                        wait()
                        game:GetService("TeleportService"):TeleportToPlaceInstance(PlaceID, ID, game.Players.LocalPlayer)
                    end)
                    wait(4)
                end
            end
        end
    end
    function Teleport() 
        while wait() do
            pcall(function()
                TPReturner()
                if foundAnything ~= "" then
                    TPReturner()
                end
            end)
        end
    end
    Teleport()
end

Misc1:AddLabel('           // Server \\\\')

local MyButton = Misc1:AddButton({
    Text = 'Server Hop',
    Func = function()
        Hop()
    end,
    DoubleClick = false,
    Tooltip = 'Server Hop'
})

local MyButton = Misc1:AddButton({
    Text = 'Rejoin Server',
    Func = function()
        local ts = game:GetService("TeleportService")
				local p = game:GetService("Players").LocalPlayer
				ts:Teleport(game.PlaceId, p)
    end,
    DoubleClick = false,
    Tooltip = 'Rejoin Server'
})

Misc1:AddToggle('MyToggle', {
    Text = 'Auto Rejoin',
    Default = true,
    Tooltip = 'Auto Rejoin When Kick',

    Callback = function(v)
        _G.Auto_Rejoin_When_Kick = v
    end
})
spawn(function()
    while wait() do
        if _G.Auto_Rejoin_When_Kick then
            getgenv().rejoin = game:GetService("CoreGui").RobloxPromptGui.promptOverlay.ChildAdded:Connect(function(child)
                if child.Name == 'ErrorPrompt' and child:FindFirstChild('MessageArea') and child.MessageArea:FindFirstChild("ErrorFrame") then
                    game:GetService("TeleportService"):Teleport(game.PlaceId) 
                end
            end)
        end
    end
end)


Misc2:AddToggle('MyToggle', {
    Text = 'WhiteScreen',
    Default = false,
    Tooltip = 'WhiteScreen',

    Callback = function(v)
        _G.WhiteScreen = v
    end
})

spawn(function()
    while wait() do
        if _G.WhiteScreen == true then
            game:GetService("RunService"):Set3dRenderingEnabled(false)
        elseif _G.WhiteScreen == false then
            game:GetService("RunService"):Set3dRenderingEnabled(true)
        end
    end
end)



Misc2:AddSlider('MySlider', {
    Text = 'Select FPS Lock',
    Default = 60,
    Min = 1,
    Max = 999,
    Rounding = 0,
    Compact = false,

    Callback = function(v)
        SelectFPSLock = v
    end
})

Misc2:AddToggle('MyToggle', {
    Text = 'Lock FPS',
    Default = false,
    Tooltip = 'Lock FPS',

    Callback = function(v)
        _G.Lock_FPS = v
        if _G.Lock_FPS == true then 
        setfpscap(SelectFPSLock)
        else 
            setfpscap(120)
        end 
    end
})

Misc3:AddToggle('MyToggle', {
    Text = 'Walk On Water',
    Default = true,
    Tooltip = 'Walk On Water',

    Callback = function(v)
        _G.WalkOnWater = v
    end
})
spawn(function()
    while task.wait() do
        pcall(function()
            if _G.WalkOnWater then
                game:GetService("Workspace").Map["WaterBase-Plane"].Size = Vector3.new(1000,112,1000)
            else
                game:GetService("Workspace").Map["WaterBase-Plane"].Size = Vector3.new(1000,80,1000)
            end
        end)
    end
end)

ThemeManager:SetLibrary(Library)
SaveManager:SetLibrary(Library)
SaveManager:IgnoreThemeSettings()
SaveManager:SetIgnoreIndexes({ 'MenuKeybind' })
SaveManager:BuildConfigSection(Tabs['Configurations'])
ThemeManager:ApplyToTab(Tabs['Configurations'])
SaveManager:LoadAutoloadConfig()

local function UpdateTime()
local GameTime = math.floor(workspace.DistributedGameTime+0.5)
local Hour = math.floor(GameTime/(60^2))%24
local Minute = math.floor(GameTime/(60^1))%60
local Second = math.floor(GameTime/(60^0))%60
Library:SetWatermark('Attack Hub |  Hr(s) : '..Hour..' Min(s) : '..Minute..' Sec(s) : '..Second)
end
spawn(function()
while true do
UpdateTime()	game:GetService("RunService").RenderStepped:Wait()
end
end)
local ScreenGui = Instance.new("ScreenGui")
local ImageButton = Instance.new("ImageButton")
local UICorner = Instance.new("UICorner")
ScreenGui.Parent = game.CoreGui
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
ImageButton.Parent = ScreenGui
ImageButton.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
ImageButton.BorderSizePixel = 0
ImageButton.Position = UDim2.new(0.120833337, 0, 0.0952890813, 0)
ImageButton.Size = UDim2.new(0, 50, 0, 50)
ImageButton.Draggable = true
ImageButton.Image = "http://www.roblox.com/asset/?id=7040391851"
ImageButton.MouseButton1Down:connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true,305,false,game)
	game:GetService("VirtualInputManager"):SendKeyEvent(false,305,false,game)
end)
