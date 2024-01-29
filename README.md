local Rayfield = loadstring(game:HttpGet('https://raw.githubusercontent.com/shlexware/Rayfield/main/source'))()

--Window
local Window = Rayfield:CreateWindow({
   Name = "Interminable Rooms | V1",
   LoadingTitle = "An Interminable Rooms Script",
   LoadingSubtitle = "by a60039",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },
   Discord = {
      Enabled = false,
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/vTEn3zeG8n would be vTEn3zeG8n.
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Pr!me Hub",
      Subtitle = "Key System",
      Note = "Join the discord (discord.gg/vTEn3zeG8n)",
      FileName = "Pr!me Hub",
      SaveKey = true,
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = "P2k6"
   }
})


--Welcome Notification
Rayfield:Notify({
   Title = "Interminable Rooms Script",
   Content = "Successfully loaded! This script is uncomplete, so expect bugs.",
   Duration = 8,
   Image = 4483362458,
   Actions = { -- Notification Buttons
      Ignore = {
         Name = "Okay!",
         Callback = function()
         print("The user tapped Okay!")
      end
   },
},
})


--Tabs 
local Tab = Window:CreateTab("Main", 4483362458)
local Tab2 = Window:CreateTab("Entity Tips", 4483362458)
local Tab3 = Window:CreateTab("Credits", 4483362458)



--Interminable Rooms Game Files
local EntitiesFolder = Workspace:WaitForChild("Entities")
local sd


local Section = Tab:CreateSection("Entity Notifiers")


--Toggles
local Toggle = Tab:CreateToggle({
    Name = "Notify Entities",
    CurrentValue = false,
    Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
    Callback = function(Value)
        EntitiesFolder.ChildAdded:Connect(function(entity)
            Rayfield:Notify({
               Title = entity.Name,
               Content = "Has spawned.",
               Duration = math.huge,
               Image = 4483362458,
               Actions = { -- Notification Buttons
                  Ignore = {
                     Name = "Okay!",
                     Callback = function()
                     print("The user tapped Okay!")
                  end
               },
            },
            })
            end)
    end,
 })


local Toggle = Tab:CreateToggle({
   Name = "Notify Entities Being Deleted",
   CurrentValue = false,
   Flag = "Toggle2", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value) 
    EntitiesFolder.ChildRemoved:Connect(function(entity)
        Rayfield:Notify({
           Title = entity.Name,
           Content = "Has deleted.",
           Duration = math.huge,
           Image = 4483362458,
           Actions = { -- Notification Buttons
              Ignore = {
                 Name = "Okay!",
                 Callback = function()
                 print("The user tapped Okay!")
              end
           },
        },
        })
        end)
   end,
})

local Section = Tab:CreateSection("ESP")


local Button = Tab:CreateButton({
   Name = "Entity ESP",
   Callback = function()
    EntitiesFolder.ChildAdded:Connect(function(entity) 
	pcall(function()
   -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = true
ESP.Names = true
ESP:Toggle(true)

-- object
for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-10" then
ESP:AddObjectListener(Workspace.Entities["A-10"], { 
    Name = "Torso", 
    CustomName = 'A-10', 
    Color = Color3.fromRGB(0, 21, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "X-10" then
ESP:AddObjectListener(Workspace.Entities["X-10"], { 
    Name = "Torso", 
    CustomName = 'X-10', 
    Color = Color3.fromRGB(19, 254, 254), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-35" then
ESP:AddObjectListener(Workspace.Entities["A-35"], { 
    Name = "Torso", 
    CustomName = 'A-35', 
    Color = Color3.fromRGB(0, 255, 89), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "X-35" then
ESP:AddObjectListener(Workspace.Entities["X-35"], { 
    Name = "Torso", 
    CustomName = 'X-35', 
    Color = Color3.fromRGB(255, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-60" then
ESP:AddObjectListener(Workspace.Entities["A-60"], { 
    Name = "Torso", 
    CustomName = 'A-60', 
    Color = Color3.fromRGB(255, 0, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "X-60" then
ESP:AddObjectListener(Workspace.Entities["X-60"], { 
    Name = "Torso", 
    CustomName = 'X-60', 
    Color = Color3.fromRGB(255, 255, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-80" then
ESP:AddObjectListener(Workspace.Entities["A-80"], { 
    Name = "Torso", 
    CustomName = 'A-80', 
    Color = Color3.fromRGB(0, 199, 27), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-100" then
ESP:AddObjectListener(Workspace.Entities["A-100"], { 
    Name = "Torso", 
    CustomName = 'A-100', 
    Color = Color3.fromRGB(243, 5, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-120" then
ESP:AddObjectListener(Workspace.Entities["A-120"], { 
    Name = "Torso", 
    CustomName = 'A-120', 
    Color = Color3.fromRGB(251, 255, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-120 Minion" then
ESP:AddObjectListener(Workspace.Entities["A-120 Minion"], { 
    Name = "Torso", 
    CustomName = 'TLUB-120', 
    Color = Color3.fromRGB(251, 255, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-150" then
ESP:AddObjectListener(Workspace.Entities["A-150"], { 
    Name = "Torso", 
    CustomName = 'A-150', 
    Color = Color3.fromRGB(0, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-183" then
ESP:AddObjectListener(Workspace.Entities["A-183"], { 
    Name = "Torso", 
    CustomName = 'A-183', 
    Color = Color3.fromRGB(247, 154, 5), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-200" then
ESP:AddObjectListener(Workspace.Entities["A-200"], { 
    Name = "Torso", 
    CustomName = 'A-200', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-245" then
ESP:AddObjectListener(Workspace.Entities["A-245"], { 
    Name = "Torso", 
    CustomName = 'A-245', 
    Color = Color3.fromRGB(79, 255, 155), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-258" then
ESP:AddObjectListener(Workspace.Entities["A-258"], { 
    Name = "Torso", 
    CustomName = 'A-258', 
    Color = Color3.fromRGB(255, 174, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-278" then
ESP:AddObjectListener(Workspace.Entities["A-278"], { 
    Name = "Torso", 
    CustomName = 'A-278', 
    Color = Color3.fromRGB(183, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "ULB-278" then
ESP:AddObjectListener(Workspace.Entities["ULB-278"], { 
    Name = "Torso", 
    CustomName = 'ULB-258', 
    Color = Color3.fromRGB(0, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "TLAB-278" then
ESP:AddObjectListener(Workspace.Entities["TLAB-278"], { 
    Name = "Torso", 
    CustomName = 'TLAB-278', 
    Color = Color3.fromRGB(212, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-300" then
ESP:AddObjectListener(Workspace.Entities["A-300"], { 
    Name = "Torso", 
    CustomName = 'A-300', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-332" then
ESP:AddObjectListener(Workspace.Entities["A-332"], { 
    Name = "Torso", 
    CustomName = 'A-332', 
    Color = Color3.fromRGB(5, 250, 197), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-350" then
ESP:AddObjectListener(Workspace.Entities["A-350"], { 
    Name = "Torso", 
    CustomName = 'A-350', 
    Color = Color3.fromRGB(100, 100, 100), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-1" then
ESP:AddObjectListener(Workspace.Entities["E-1"], { 
    Name = "Torso", 
    CustomName = 'E-1', 
    Color = Color3.fromRGB(250, 246, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "XE-1" then
ESP:AddObjectListener(Workspace.Entities["XE-1"], { 
    Name = "Torso", 
    CustomName = 'XE-1', 
    Color = Color3.fromRGB(104, 252, 206), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-22" then
ESP:AddObjectListener(Workspace.Entities["E-22"], { 
    Name = "Torso", 
    CustomName = 'E-22', 
    Color = Color3.fromRGB(252, 128, 57), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-42LEFT" then
ESP:AddObjectListener(Workspace.Entities["E-42LEFT"], { 
    Name = "Torso", 
    CustomName = 'E-42', 
    Color = Color3.fromRGB(255, 201, 219), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-42RIGHT" then
ESP:AddObjectListener(Workspace.Entities["E-42RIGHT"], { 
    Name = "Torso", 
    CustomName = 'E-42', 
    Color = Color3.fromRGB(255, 201, 219), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-60" then
ESP:AddObjectListener(Workspace.Entities["E-60"], { 
    Name = "Torso", 
    CustomName = 'E-60', 
    Color = Color3.fromRGB(255, 0, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-142" then
ESP:AddObjectListener(Workspace.Entities["E-142"], { 
    Name = "Torso", 
    CustomName = 'E-142', 
    Color = Color3.fromRGB(252, 0, 194), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-144" then
ESP:AddObjectListener(Workspace.Entities["E-144"], { 
    Name = "Torso", 
    CustomName = 'E-144', 
    Color = Color3.fromRGB(0, 255, 131), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-200" then
ESP:AddObjectListener(Workspace.Entities["E-200"], { 
    Name = "Torso", 
    CustomName = 'E-200', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-5" then
ESP:AddObjectListener(Workspace.Entities["V-5"], { 
    Name = "Torso", 
    CustomName = 'V-5', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-27" then
ESP:AddObjectListener(Workspace.Entities["V-27"], { 
    Name = "Torso", 
    CustomName = 'V-27', 
    Color = Color3.fromRGB(200, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-35" then
ESP:AddObjectListener(Workspace.Entities["V-35"], { 
    Name = "Torso", 
    CustomName = 'V-35', 
    Color = Color3.fromRGB(197, 2, 204), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-50" then
ESP:AddObjectListener(Workspace.Entities["V-50"], { 
    Name = "Torso", 
    CustomName = 'V-50', 
    Color = Color3.fromRGB(187, 84, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "Noah" then
ESP:AddObjectListener(Workspace.Entities.Noah, { 
    Name = "Torso", 
    CustomName = 'Noah', 
    Color = Color3.fromRGB(255, 0, 64), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "John" then
ESP:AddObjectListener(Workspace.Entities.John, { 
    Name = "Torso", 
    CustomName = 'John', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "JohnLocker" then
ESP:AddObjectListener(Workspace.Entities.JohnLocker, { 
    Name = "Torso", 
    CustomName = 'Locker John', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end
end)
end)
   end,
})


local Button = Tab:CreateButton({
   Name = "Entity ESP Fixer",
   Callback = function()
   -- loadstring
local ESP = loadstring(game:HttpGet("https://kiriot22.com/releases/ESP.lua"))()

-- config
ESP.Players = false
ESP.Boxes = true
ESP.Names = true
ESP:Toggle(true)

-- object
for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-10" then
ESP:AddObjectListener(Workspace.Entities["A-10"], { 
    Name = "Torso", 
    CustomName = 'A-10', 
    Color = Color3.fromRGB(0, 21, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "X-10" then
ESP:AddObjectListener(Workspace.Entities["X-10"], { 
    Name = "Torso", 
    CustomName = 'X-10', 
    Color = Color3.fromRGB(19, 254, 254), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-35" then
ESP:AddObjectListener(Workspace.Entities["A-35"], { 
    Name = "Torso", 
    CustomName = 'A-35', 
    Color = Color3.fromRGB(0, 255, 89), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "X-35" then
ESP:AddObjectListener(Workspace.Entities["X-35"], { 
    Name = "Torso", 
    CustomName = 'X-35', 
    Color = Color3.fromRGB(255, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-60" then
ESP:AddObjectListener(Workspace.Entities["A-60"], { 
    Name = "Torso", 
    CustomName = 'A-60', 
    Color = Color3.fromRGB(255, 0, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "X-60" then
ESP:AddObjectListener(Workspace.Entities["X-60"], { 
    Name = "Torso", 
    CustomName = 'X-60', 
    Color = Color3.fromRGB(255, 255, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-80" then
ESP:AddObjectListener(Workspace.Entities["A-80"], { 
    Name = "Torso", 
    CustomName = 'A-80', 
    Color = Color3.fromRGB(0, 199, 27), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-100" then
ESP:AddObjectListener(Workspace.Entities["A-100"], { 
    Name = "Torso", 
    CustomName = 'A-100', 
    Color = Color3.fromRGB(243, 5, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-120" then
ESP:AddObjectListener(Workspace.Entities["A-120"], { 
    Name = "Torso", 
    CustomName = 'A-120', 
    Color = Color3.fromRGB(251, 255, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-120 Minion" then
ESP:AddObjectListener(Workspace.Entities["A-120 Minion"], { 
    Name = "Torso", 
    CustomName = 'TLUB-120', 
    Color = Color3.fromRGB(251, 255, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-150" then
ESP:AddObjectListener(Workspace.Entities["A-150"], { 
    Name = "Torso", 
    CustomName = 'A-150', 
    Color = Color3.fromRGB(0, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-183" then
ESP:AddObjectListener(Workspace.Entities["A-183"], { 
    Name = "Torso", 
    CustomName = 'A-183', 
    Color = Color3.fromRGB(247, 154, 5), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-200" then
ESP:AddObjectListener(Workspace.Entities["A-200"], { 
    Name = "Torso", 
    CustomName = 'A-200', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-245" then
ESP:AddObjectListener(Workspace.Entities["A-245"], { 
    Name = "Torso", 
    CustomName = 'A-245', 
    Color = Color3.fromRGB(79, 255, 155), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-258" then
ESP:AddObjectListener(Workspace.Entities["A-258"], { 
    Name = "Torso", 
    CustomName = 'A-258', 
    Color = Color3.fromRGB(255, 174, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-278" then
ESP:AddObjectListener(Workspace.Entities["A-278"], { 
    Name = "Torso", 
    CustomName = 'A-278', 
    Color = Color3.fromRGB(183, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "ULB-278" then
ESP:AddObjectListener(Workspace.Entities["ULB-278"], { 
    Name = "Torso", 
    CustomName = 'ULB-258', 
    Color = Color3.fromRGB(0, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "TLAB-278" then
ESP:AddObjectListener(Workspace.Entities["TLAB-278"], { 
    Name = "Torso", 
    CustomName = 'TLAB-278', 
    Color = Color3.fromRGB(212, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-300" then
ESP:AddObjectListener(Workspace.Entities["A-300"], { 
    Name = "Torso", 
    CustomName = 'A-300', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-332" then
ESP:AddObjectListener(Workspace.Entities["A-332"], { 
    Name = "Torso", 
    CustomName = 'A-332', 
    Color = Color3.fromRGB(5, 250, 197), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "A-350" then
ESP:AddObjectListener(Workspace.Entities["A-350"], { 
    Name = "Torso", 
    CustomName = 'A-350', 
    Color = Color3.fromRGB(100, 100, 100), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-1" then
ESP:AddObjectListener(Workspace.Entities["E-1"], { 
    Name = "Torso", 
    CustomName = 'E-1', 
    Color = Color3.fromRGB(250, 246, 0), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "XE-1" then
ESP:AddObjectListener(Workspace.Entities["XE-1"], { 
    Name = "Torso", 
    CustomName = 'XE-1', 
    Color = Color3.fromRGB(104, 252, 206), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-22" then
ESP:AddObjectListener(Workspace.Entities["E-22"], { 
    Name = "Torso", 
    CustomName = 'E-22', 
    Color = Color3.fromRGB(252, 128, 57), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-42LEFT" then
ESP:AddObjectListener(Workspace.Entities["E-42LEFT"], { 
    Name = "Torso", 
    CustomName = 'E-42', 
    Color = Color3.fromRGB(255, 201, 219), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-42RIGHT" then
ESP:AddObjectListener(Workspace.Entities["E-42RIGHT"], { 
    Name = "Torso", 
    CustomName = 'E-42', 
    Color = Color3.fromRGB(255, 201, 219), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-60" then
ESP:AddObjectListener(Workspace.Entities["E-60"], { 
    Name = "Torso", 
    CustomName = 'E-60', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-142" then
ESP:AddObjectListener(Workspace.Entities["E-142"], { 
    Name = "Torso", 
    CustomName = 'E-142', 
    Color = Color3.fromRGB(252, 0, 194), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-144" then
ESP:AddObjectListener(Workspace.Entities["E-144"], { 
    Name = "Torso", 
    CustomName = 'E-144', 
    Color = Color3.fromRGB(0, 255, 131), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "E-200" then
ESP:AddObjectListener(Workspace.Entities["E-200"], { 
    Name = "Torso", 
    CustomName = 'E-200', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-5" then
ESP:AddObjectListener(Workspace.Entities["V-5"], { 
    Name = "Torso", 
    CustomName = 'V-5', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-27" then
ESP:AddObjectListener(Workspace.Entities["V-27"], { 
    Name = "Torso", 
    CustomName = 'V-27', 
    Color = Color3.fromRGB(200, 0, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-35" then
ESP:AddObjectListener(Workspace.Entities["V-35"], { 
    Name = "Torso", 
    CustomName = 'V-35', 
    Color = Color3.fromRGB(197, 2, 204), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "V-50" then
ESP:AddObjectListener(Workspace.Entities["V-50"], { 
    Name = "Torso", 
    CustomName = 'V-50', 
    Color = Color3.fromRGB(187, 84, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "Noah" then
ESP:AddObjectListener(Workspace.Entities.Noah, { 
    Name = "Torso", 
    CustomName = 'Noah', 
    Color = Color3.fromRGB(255, 0, 64), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "John" then
ESP:AddObjectListener(Workspace.Entities.John, { 
    Name = "Torso", 
    CustomName = 'John', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end

for i, v in pairs(game:GetService("Workspace").Entities:GetChildren()) do
 if v.Name == "JohnLocker" then
ESP:AddObjectListener(Workspace.Entities.JohnLocker, { 
    Name = "Torso", 
    CustomName = 'Locker John', 
    Color = Color3.fromRGB(255, 255, 255), -- Color
    IsEnabled = "whatever" 
})
ESP.whatever = true
end
end
   end,
})


local Section = Tab:CreateSection("No-Drain Flashlights")


 local Button = Tab:CreateButton({
    Name = "Infinite Flashlight",
    Callback = function()
        game.Players.LocalPlayer.Character.FlashlightValues:Destroy()
        game.Players.LocalPlayer.Character.Battery.Value = math.huge
    end,
 })


 local Button = Tab:CreateButton({
    Name = "Infinite Gummy Flashlight (Requires Gamepass)",
    Callback = function()
        game.Players.LocalPlayer.Character.GummyFlashlightValue:Destroy()
        game.Players.LocalPlayer.Character.GummyBattery.Value = math.huge
    end,
 })
 
 
 local Section = Tab:CreateSection("Speed")
 
 
 local Keybind = Tab:CreateKeybind({
   Name = "Sprint",
   CurrentKeybind = "Q",
   HoldToInteract = false,
   Flag = "Keybind1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Keybind)
   game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 24
   end,
})


local Slider = Tab:CreateSlider({
   Name = "Walkspeed",
   Range = {1, 100},
   Increment = 1,
   Suffix = "WalkSpeed",
   CurrentValue = 10,
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
   game.Players.LocalPlayer.character.Humanoid.WalkSpeed = Value
   end,
})


local Section = Tab:CreateSection("Miscellaneous")


 local Button = Tab:CreateButton({
    Name = "Silence Footsteps",
    Callback = function()
        game.Players.LocalPlayer.Character.Footsteps:Destroy()
    end,
 })
 
 
local Section = Tab2:CreateSection("A-Section")
local Section = Tab3:CreateSection("Credits")


--Paragraphs
local Paragraph = Tab2:CreateParagraph({Title = "A-10", Content = "Hãy trốn đi."})
local Paragraph = Tab2:CreateParagraph({Title = "X-10", Content = "Nó giống như A-10 nhưng nhanh hơnr."})
local Paragraph = Tab2:CreateParagraph({Title = "A-35", Content = "Nó bật lại 1,5 lần. Khi bạn nghe thấy nó, hãy trốn vào bất cứ điều gì."})
local Paragraph = Tab2:CreateParagraph({Title = "X-35", Content = "Nó bật lại 2 lần. Mặc dù nó nhanh hơn A-35 nhưng hãy trốn trong bất cứ thứ gì."})
local Paragraph = Tab2:CreateParagraph({Title = "A-60", Content = "Khi nó đi vào phòng bạn, nó ở lại một lúc rồi biến mất."})
local Paragraph = Tab2:CreateParagraph({Title = "X-60", Content = "A-60 nhưng nhanh hơn, cùng chiến lược."})
local Paragraph = Tab2:CreateParagraph({Title = "A-80", Content = "Đừng đến gần nó nếu không bạn sẽ bị thương."})
local Paragraph = Tab2:CreateParagraph({Title = "A-100", Content = "Nó đi đến phòng mới nhất và kiểm tra TỦ KHÓA MÀU XÁM rồi quay lại."})
local Paragraph = Tab2:CreateParagraph({Title = "A-120", Content = "Đơn giản chỉ cần trốn đi. Nó bật lại một vài lần và sinh ra tay sai."})
local Paragraph = Tab2:CreateParagraph({Title = "A-150", Content = "Nó xuất hiện từ một tờ giấy. Nó kiểm tra tất cả tủ khóa màu xám trong phòng mới nhất."})
local Paragraph = Tab2:CreateParagraph({Title = "A-183", Content = "Đơn giản chỉ cần ẩn đi. Nó bật lại nhiều lần và rất nhanh."})
local Paragraph = Tab2:CreateParagraph({Title = "A-200", Content = "Nó đến trước mặt bạn. Đơn giản chỉ cần trốn khi bạn nghe thấy một tiếng hét lớn."})
local Paragraph = Tab2:CreateParagraph({Title = "A-245", Content = "Nó phá vỡ tất cả tủ khóa trong phòng hiện tại."})
local Paragraph = Tab2:CreateParagraph({Title = "A-258", Content = "Nó xuất hiện trong phòng hiện tại và phát ra âm thanh chói tai."})
local Paragraph = Tab2:CreateParagraph({Title = "A-278", Content = "Nó đến từ một cổng thông tin. Chỉ trốn trong tủ đựng đồ hoặc tủ lạnh màu xám."})
local Paragraph = Tab2:CreateParagraph({Title = "A-300", Content = "Nó sinh ra một thực thể. Màu sắc của nó thay đổi theo thực thể mà nó sinh ra."})
local Paragraph = Tab2:CreateParagraph({Title = "A-332", Content = "Khi bạn nghe hoặc nhìn thấy văn bản ẩn, hãy trốn vào bất cứ thứ gì cho đến khi nó biến mất."})
local Paragraph = Tab2:CreateParagraph({Title = "A-350", Content = "Hide. It throws orbs at you."})
local Paragraph = Tab2:CreateParagraph({Title = "Noah", Content = "Do not hide when it appears."})
local Paragraph = Tab2:CreateParagraph({Title = "John", Content = "It is just a jumpscare."})
local Paragraph = Tab2:CreateParagraph({Title = "Mario", Content = "It is just John but rarer."})


local Section = Tab2:CreateSection("E-Section")


local Paragraph = Tab2:CreateParagraph({Title = "E-1", Content = "Đừng mở đèn pin của bạn. Bạn có thể sử dụng đèn pin dẻo."})
local Paragraph = Tab2:CreateParagraph({Title = "E-22", Content = "Hãy trốn đi khi nó đến."})
local Paragraph = Tab2:CreateParagraph({Title = "E-42", Content = "Đi từ hai phía của căn phòng. ĐỪNG đến gần nó."})
local Paragraph = Tab2:CreateParagraph({Title = "E-60", Content = "Hãy trốn đi khi nó đến."})
local Paragraph = Tab2:CreateParagraph({Title = "E-142", Content = "Nó sẽ đi đến phòng của bạn.Rùi bạn trốn và đợi."})
local Paragraph = Tab2:CreateParagraph({Title = "E-144", Content = "Nó sẽ xuất hiện ngay phòng mới nhất.Hãy tốn ngay."})
local Paragraph = Tab2:CreateParagraph({Title = "E-200", Content = "Nó sẽ xuất hiện ngay phòng mới nhất. Nó phát ra tiếng bíp vài lần."})


local Section = Tab2:CreateSection("V-Section")


local Paragraph = Tab2:CreateParagraph({Title = "V-5", Content = "Đừng tiếp cận nó. Nó gây ra rất ít sát thương."})
local Paragraph = Tab2:CreateParagraph({Title = "V-27", Content = "Hãy trốn đi khi nó đến."})
local Paragraph = Tab2:CreateParagraph({Title = "V-35", Content = "Hãy trốn đi khi nó đến."})
local Paragraph = Tab2:CreateParagraph({Title = "V-50", Content = "Hãy trốn đi khi nó đến."})


local Section = Tab2:CreateSection("Others")


local Paragraph = Tab2:CreateParagraph({Title = "Locker John", Content = "It rarely appears in a locker. It renders that locker unusable."})
local Paragraph = Tab2:CreateParagraph({Title = "Trollface", Content = "It is so fast."})
local Paragraph = Tab2:CreateParagraph({Title = "G-GLITCH", Content = "Don't worry. Even though he is very fast, he is harmless."})


local Paragraph = Tab3:CreateParagraph({Title = "Credits", Content = "Script made by Nenarus#3186."})
