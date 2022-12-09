local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("TITLE", "Midnight")
local Tab = Window:NewTab("Johncina")
    local Section = Tab:NewSection("Skill")
        Section:NewKeybind("Stab", "KeybindInfo", Enum.KeyCode.Z, function()
            local args = {
                [1] = Vector3.new(-2.8945560455322266, 12.737393379211426, 391.5618896484375)
            }
            
            game:GetService("ReplicatedStorage").Characters.Vigilante.Remotes.QuickStab:FireServer(unpack(args))                       
    end)
    Section:NewKeybind("ChaiSawAT", "KeybindInfo", Enum.KeyCode.X, function()
        local args = {
            [1] = game:GetService("Players").LocalPlayer
        }
        
        game:GetService("ReplicatedStorage").Characters.Vigilante.Remotes.ChainsawPierce:FireServer(unpack(args))                
    end)
    Section:NewKeybind("Counter", "KeybindInfo", Enum.KeyCode.C, function()
        local args = {
            [1] = game:GetService("Players").LocalPlayer
        }
        
        game:GetService("Players").LocalPlayer.Character.Vigilante.CounterActivate:FireServer(unpack(args))                
    end)
    Section:NewKeybind("Dynamite", "KeybindInfo", Enum.KeyCode.V, function()
        local args = {
            [1] = Vector3.new(33.36574172973633, 9.719757080078125, 340.9559326171875)
        }
        
        game:GetService("ReplicatedStorage").Characters.Vigilante.Remotes.Dynamite:FireServer(unpack(args))        
    end)
    Section:NewKeybind("Heal", "KeybindInfo", Enum.KeyCode.R, function()
        local args = {
            [1] = Vector3.new(-2.6949658393859863, 14.10774040222168, 390.3093566894531)
        }
        
        game:GetService("ReplicatedStorage").Characters.Moonknight.Remotes.Heal:FireServer(unpack(args))                
    end)
local Tab = Window:NewTab("Cradit")
    local Section = Tab:NewSection("UI")
    Section:NewKeybind("Hide UI", "KeybindInfo", Enum.KeyCode.P, function()
	Library:ToggleUI()
end)
