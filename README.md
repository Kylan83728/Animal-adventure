local Rayfield = loadstring(game:HttpGet('https://sirius.menu/rayfield'))()
local Window = Rayfield:CreateWindow({
   Name = "Rayfield Example Window",
   Icon = 0, -- Icon in Topbar. Can use Lucide Icons (string) or Roblox Image (number). 0 to use no icon (default).
   LoadingTitle = "Rayfield Interface Suite",
   LoadingSubtitle = "by Sirius",
   Theme = "Default", -- Check https://docs.sirius.menu/rayfield/configuration/themes

   DisableRayfieldPrompts = false,
   DisableBuildWarnings = false, -- Prevents Rayfield from warning when the script has a version mismatch with the interface

   ConfigurationSaving = {
      Enabled = true,
      FolderName = nil, -- Create a custom folder for your hub/game
      FileName = "Big Hub"
   },

   Discord = {
      Enabled = false, -- Prompt the user to join your Discord server if their executor supports it
      Invite = "noinvitelink", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },

   KeySystem = false, -- Set this to true to use our key system
   KeySettings = {
      Title = "Untitled",
      Subtitle = "Key System",
      Note = "No method of obtaining the key is provided", -- Use this to tell the user how to get a key
      FileName = "Key", -- It is recommended to use something unique as other scripts using Rayfield may overwrite your key file
      SaveKey = true, -- The user's key will be saved, but if you change the key, they will be unable to use your script
      GrabKeyFromSite = false, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = {"Hello"} -- List of keys that will be accepted by the system, can be RAW file links (pastebin, github etc) or simple strings ("hello","key22")
   }
})


local farmTab = Window:CreateTab("Farm", 4483362458) -- Title, Image


local isHitting = false
local Toggle = farmTab:CreateToggle({
   Name = "dummy lvl0👊",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = {
        ["isLocalNPC"] = true,
        ["npcName"] = "Lvl1"
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").Events.DamageEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end
   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})


local isHitting = false
local Toggle = farmTab:CreateToggle({
   Name = "dummy lvl50👊",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = {
        ["isDummy"] = true,
        ["enemyChar"] = workspace:FindFirstChild("Area Creator").area1.dummy.Rock
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").Events.DamageEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end

   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})


local Toggle = farmTab:CreateToggle({
   Name = "dummy lvl200",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = {
        ["isDummy"] = true,
        ["enemyChar"] = workspace:FindFirstChild("Area Creator").area2.dummy.Grass
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").Events.DamageEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end

   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local coinTab = Window:CreateTab("Auto coin", 4483362458) -- Title, Image



local isHitting = false
local Toggle = coinTab:CreateToggle({
   Name = "auto coin lvl0",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = {
        ["action"] = "npc_died",
        ["npcName"] = "Lvl1"
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").Events.coinsEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end

   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})



local isHitting = false
local Toggle = coinTab:CreateToggle({
   Name = "auto coin lvl50",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = {
        ["action"] = "npc_died",
        ["npcName"] = "Rock"
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").Events.coinsEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end

   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})


local Toggle = coinTab:CreateToggle({
   Name = "auto coin lvl200",
   CurrentValue = false,
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Value)
local args = {
    [1] = {
        ["action"] = "npc_died",
        ["npcName"] = "Grass"
    }
}

 isHitting = Value

        if isHitting then
            -- Lancer une boucle non bloquante
            task.spawn(function()
                while isHitting do

game:GetService("ReplicatedStorage").Events.coinsEvent:FireServer(unpack(args))
task.wait(0.1) -- Pause
end
            end)
        end

   -- The function that takes place when the toggle is pressed
   -- The variable (Value) is a boolean on whether the toggle is true or false
   end,
})
