----------------------------------------------------------------------
--timeAUtofarm
if _G.KEY == "CHOPROX" then
local tf = 0
local timeZ = 0
local Farmv2 = false
--Chest
local CommonChest = false
local UncommonChest = false
local RareChest = false
local EpicChest = false
local LegendaryChest = false
--Teams
local BlackTeam = false
local BlueTeam  = false 
local GreenTeam = false   
local MagentaTeam = false 
local RedTeam = false    
local WhiteTeam = false
local YellowTeam = false
--Teleport
local Teleport = Game.Players.LocalPlayer.Character.HumanoidRootPart
function CommonChest()
local args = {
    [1] = "Common Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end

function UncommonChest()
local args = {
    [1] = "Uncommon Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end

function RareChest()
local args = {
    [1] = "Rare Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end

function EpicChest()
local args = {
    [1] = "Epic Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end

function LegendaryChest()
local args = {
    [1] = "Legendary Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end
function FarmV2()
while _G.AUTOFARM do
game.workspace.Gravity = 0
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-57.3277435, 54.11306, 723.097717, -0.999458313, -4.35474812e-09, -0.032909818, -2.43262122e-09, 1, -5.84459166e-08, 0.032909818, -5.83342015e-08, -0.999458313)
local TweenService = game:GetService("TweenService")
local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(20, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
{CFrame = CFrame.new(-52.8971481, 51.6515312, 8698.07812, -0.999616921, -0.00748590147, 0.0266463459, -7.22909554e-09, 0.962729931, 0.270464629, -0.0276779067, 0.270361006, -0.962361097)}):Play()
wait("20")
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-57.3277435, 54.11306, 723.097717, -0.999458313, -4.35474812e-09, -0.032909818, -2.43262122e-09, 1, -5.84459166e-08, 0.032909818, -5.83342015e-08, -0.999458313)
end
end

function GetGo()
while _G.AUTOFARM do
wait("1")
workspace.ClaimRiverResultsGold:FireServer()
end
end

   --
   local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/naypramx/Ui__Project/Script/XeNonUi", true))()
    library:CreateWatermark("ChoPro x Hub map Build A Boat For Treasure") -- Config แตกนะเดียวค่อยแก้รอเน็ตมาก่อน By MeowX#0001
    local CenterHubNo1 = library:CreateWindow("ChoPro x Hub",Enum.KeyCode.RightControl)
    local Tab = CenterHubNo1:CreateTab("script")
    local Sector1 = Tab:CreateSector("Farm","left")
	local Sector2 = Tab:CreateSector("Teleport","left") --right
	local Sector3 = Tab:CreateSector("Buy Chest","right")
    Sector1:AddLabel("Farm ")
    Sector1:AddToggle("Auto Farm gold⛵",false,function(t)
       _G.AUTOFARM = t
if tf ~= 0 and timeZ ~= 0 then	   
	   while _G.AUTOFARM do
		  game.workspace.Gravity = 0
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-57.3277435, 54.11306, 723.097717, -0.999458313, -4.35474812e-09, -0.032909818, -2.43262122e-09, 1, -5.84459166e-08, 0.032909818, -5.83342015e-08, -0.999458313)
local TweenService = game:GetService("TweenService")
local Tw = TweenService:Create(game.Players.LocalPlayer.Character.HumanoidRootPart, TweenInfo.new(tf, Enum.EasingStyle.Linear, Enum.EasingDirection.Out,0,false,0), 
{CFrame = CFrame.new(-52.8971481, 51.6515312, 8698.07812, -0.999616921, -0.00748590147, 0.0266463459, -7.22909554e-09, 0.962729931, 0.270464629, -0.0276779067, 0.270361006, -0.962361097)}):Play()
wait(timeZ)
game.workspace.Gravity = 192
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-56.2867813, -350.44455, 9496.73535, 0.182033226, -9.23010504e-08, -0.983292401, -1.59918905e-08, 1, -9.68299076e-08, 0.983292401, 3.33509647e-08, 0.182033226) * CFrame.new(0,-2,0)
wait("3")
game.Players.LocalPlayer.Character.Humanoid.Health = 0
wait("16.5")
end
elseif tf == 0 and timeZ == 0 then	
	 print()
	 end
if Farmv2 == true then
FarmV2()
Game.Players.LocalPlayer:Kick("รออัดเดต")
end
		if _G.AUTOFARM == false then
       print("stop")
		end	
end)
Sector1:AddToggle("Auto Get",false,function(t)
if t == true then
GetGo()
Game.Players.LocalPlayer:Kick("รออัพเดต")
end
if t == false then
 _G.AUTOFARM = false
print()
end
end)
Sector1:AddDropdown("auto farm mode",{
"mode fast",
"mode normat",
"mode slow",
"Auto farmV2"
},"",false,function(t)
if t == "mode fast" then
print(t)
tf = 10
timeZ = 11
end	
if t == "mode normat" then
print(t)
tf = 15
timeZ = 16
end	
 if t == "mode slow" then
print(t)
tf = 25
timeZ = 26
 end	
 if t == "Auto farmV2" then
Farmv2 = true
tf = 0
timeZ = 0
 end
end)
Sector2:AddDropdown("auto farm mode",{
"Black Team   ⬛",
"Blue Team    🟦",
"Green Team   🟩",
"Magenta Team 🟪",
"Red Team     🟥",
"White Team   ⬜",
"Yellow Team  🟨",
},"",false,function(t)
if t == "Black Team   ⬛" then
 BlackTeam = true
 BlueTeam  = false 
 GreenTeam = false   
 MagentaTeam = false 
 RedTeam = false    
 WhiteTeam = false
  YellowTeam = false
end
if t == "Blue Team    🟦" then
BlackTeam = false
 BlueTeam  = true 
 GreenTeam = false   
 MagentaTeam = false 
 RedTeam = false    
 WhiteTeam = false
  YellowTeam = false
end
if t == "Green Team   🟩" then
BlackTeam = false
 BlueTeam  = false 
 GreenTeam = true  
 MagentaTeam = false 
 RedTeam = false    
 WhiteTeam = false
  YellowTeam = false
end
if t == "Magenta Team 🟪" then
BlackTeam = false
 BlueTeam  = false 
 GreenTeam = false   
 MagentaTeam = true
 RedTeam = false    
 WhiteTeam = false
  YellowTeam = false
end	
if t == "Red Team     🟥" then
BlackTeam = false
 BlueTeam  = false 
 GreenTeam = false   
 MagentaTeam = false 
 RedTeam = true 
 WhiteTeam = false
  YellowTeam = false
end
if t == "White Team   ⬜" then
BlackTeam = false
 BlueTeam  = false 
 GreenTeam = false   
 MagentaTeam = false 
 RedTeam = false    
 WhiteTeam = true
  YellowTeam = false
end
if t == "Yellow Team  🟨" then
BlackTeam = false
 BlueTeam  = false 
 GreenTeam = false   
 MagentaTeam = false 
 RedTeam = false    
 WhiteTeam = false
  YellowTeam = true
end
end)
_G.TP = true
 Sector2:AddToggle("Teleport Teams",false,function(t)
 if t == true then
	 _G.TP = true
   while _G.TP do
	 wait("0.1")
	 print("do")
     if BlackTeam == true then
      Teleport.CFrame = CFrame.new(-479.183594, -9.35057735, -69.5191345, 0.0191004109, 0.0480180942, -0.998663843, 8.59629257e-09, 0.998846054, 0.048026856, 0.99981755, -0.000917341269, 0.0190783702)
      end
	  if BlueTeam == true then
      Teleport.CFrame = CFrame.new(371.556, -9.78000164, 299.929535, 0.0484575145, -4.20890123e-09, 0.998825252, -2.11321289e-08, 1, 5.23906651e-09, -0.998825252, -2.13611759e-08, 0.0484575145)
	   end 
	   if GreenTeam == true then
	   Teleport.CFrame = CFrame.new(-479.034119, -9.74000263, 294.020416, 0.016509505, 5.1710586e-08, -0.999863684, 1.7944769e-09, 1, 5.17472643e-08, 0.999863684, -2.64855404e-09, 0.016509505)  
	   end
	   if MagentaTeam == true then
       Teleport.CFrame = CFrame.new(370.649811, -9.89999676, 646.890808, -0.0276095718, -7.04997234e-08, 0.999618769, 9.30200805e-09, 1, 7.07835284e-08, -0.999618769, 1.12527649e-08, -0.0276095718)
	   end
	   if RedTeam == true then
	   Teleport.CFrame = CFrame.new(371.780914, -9.78000164, -64.3214493, 0.0582691319, -4.38945698e-08, 0.99830091, 8.79327056e-10, 1, 4.39179537e-08, -0.99830091, -1.68122805e-09, 0.0582691319)
	   end
	  if WhiteTeam == true then
	   Teleport.CFrame = CFrame.new(-49.1447296, -9.81999874, -494.950012, -0.999949396, 2.60278412e-08, 0.010057237, 2.68992757e-08, 1, 8.65122658e-08, -0.010057237, 8.6778428e-08, -0.999949396)
	  end
	   if YellowTeam == true then
	   Teleport.CFrame = CFrame.new(-478.062744, -9.85999584, 639.235229, -0.0173586681, -1.61047122e-08, -0.999849319, -1.2159628e-08, 1, -1.58960329e-08, 0.999849319, 1.18818617e-08, -0.0173586681)
	   end 	 	 	  	    	
   end
 end
if t == false then
_G.TP = false
wait("0.1")
end
end)
Sector3:AddButton("Buy Common Chest🟢",function()   
CommonChest()
end)	
Sector3:AddButton("Buy Uncommon Chest🟡",function()   
UncommonChest()
end)	
Sector3:AddButton("Buy Rare Chest🔴",function()   
RareChest()
end)	
Sector3:AddButton("Buy Epic Chest🔵",function()   
EpicChest()
end)
Sector3:AddButton("Buy Legendary Chest🟣",function()   
LegendaryChest()
end)
Sector3:AddDropdown("Auto buy chest",{
"Common Chest",
"Uncommon Chest",
"Rare Chest",
"Epic Chest",
"Legendary Chest",
},"",false,function(t)
if t == "Common Chest" then
CommonChest = true --true
UncommonChest = false
RareChest = false
EpicChest = false
LegendaryChest = false
end
if t == "Uncommon Chest" then
CommonChest = false
UncommonChest = true --true
RareChest = false
EpicChest = false
LegendaryChest = false
end
if t == "Rare Chest" then
CommonChest = false
UncommonChest = false
RareChest = true --true
EpicChest = false
LegendaryChest = false
end
if t == "Epic Chest" then
CommonChest = false
UncommonChest = false
RareChest = false
EpicChest = true --true
LegendaryChest = false
end
if t == "Legendary Chest" then
CommonChest = false
UncommonChest = false
RareChest = false
EpicChest = false
LegendaryChest = true --true
end
end)
_G.B = true
Sector3:AddToggle("Buy Chest",false,function(t)
_G.B = true
 if t == true then
 _G.B = true
 if CommonChest == true then
 while _G.B do
 local args = {
    [1] = "Common Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))

 wait("1")
end
 end
 if UncommonChest == true then
 while _G.B do
 wait("1")
 local args = {
    [1] = "Uncommon Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
 end
 end
 if RareChest == true then
while _G.B do
wait("1")
local args = {
    [1] = "Rare Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end
end
if EpicChest == true then
while _G.B do
wait("1")
local args = {
    [1] = "Epic Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end
end
 if LegendaryChest == true then
 while _G.B do
 wait("1")
 local args = {
    [1] = "Legendary Chest",
    [2] = 1
}
workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
 end
 end
 end
 if t == false then
 _G.B = false
 end
end)
--_G.B = false
print("hi")
-- TAD 2
function WoodBlock()
local args = {
    [1] = "WoodBlock",
    [2] = 1
}

workspace.ItemBoughtFromShop:InvokeServer(unpack(args))
end	
local Tab = CenterHubNo1:CreateTab("Buy")
local Sector1 = Tab:CreateSector("Buy Block","left")
Sector1:AddButton("Buy Common Chest🟢",function()   
WoodBlock()
end)	
end
