# Flood UI

> Modern, animated and customizable Roblox UI library.

## Features

- Smooth animations
- Customizable themes
- Simple API
- Modular structure
- Lightweight components

## Installation

Add your installation method here.

## Example

```lua
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GhosterXS/Flood-Ui/refs/heads/main/Flood%20Ui"))()

local Window = Library:CreateWindow({
    Name = "Flood Ui Example",
    LoadingTitle = "Flood Ui Example",
    LoadingSubtitle = "by GhosterXS",
    Theme = Color3.fromRGB(255, 255, 255)
})

local Main = Window:CreateTab("Main")
local Player = Window:CreateTab("Player")
local Misc = Window:CreateTab("Misc")

Main:CreateSection("Welcome")
Main:CreateLabel("Flood Ui is loaded")
Main:CreateLabel("Theme and keybind auto-save")

Main:CreateButton({
    Name = "Test Notification",
    Callback = function()
        Library:Notify({
            Title = "Flood Ui",
            Content = "Notification works!",
            Duration = 4
        })
    end
})

Main:CreateToggle({
    Name = "Example Toggle",
    Default = false,
    Callback = function(Value)
        print("Toggle:", Value)
    end
})

Main:CreateDropdown({
    Name = "Mode",
    Options = {"Option 1", "Option 2", "Option 3"},
    Default = "Option 1",
    Callback = function(Value)
        print("Selected:", Value)
    end
})

Main:CreateSection("Credits")
Main:CreateLabel("UI Library: Flood Ui")
Main:CreateLabel("GitHub: GhosterXS/Flood-Ui")

Player:CreateSection("Character")

Player:CreateSlider({
    Name = "WalkSpeed",
    Min = 16,
    Max = 200,
    Default = 16,
    Callback = function(Value)
        local lp = game.Players.LocalPlayer
        if lp.Character and lp.Character:FindFirstChild("Humanoid") then
            lp.Character.Humanoid.WalkSpeed = Value
        end
    end
})

Player:CreateSlider({
    Name = "JumpPower",
    Min = 50,
    Max = 200,
    Default = 50,
    Callback = function(Value)
        local lp = game.Players.LocalPlayer
        if lp.Character and lp.Character:FindFirstChild("Humanoid") then
            lp.Character.Humanoid.JumpPower = Value
        end
    end
})

Player:CreateToggle({
    Name = "Infinite Jump",
    Default = false,
    Callback = function(Value)
        print("Infinite Jump:", Value)
    end
})

Misc:CreateSection("Extra")

Misc:CreateButton({
    Name = "Print Hello",
    Callback = function()
        print("Hello from Flood Ui")
        Library:Notify({
            Title = "Hello",
            Content = "Hello World!",
            Duration = 3
        })
    end
})

Misc:CreateSlider({
    Name = "FOV",
    Min = 70,
    Max = 120,
    Default = 70,
    Callback = function(Value)
        workspace.CurrentCamera.FieldOfView = Value
    end
})

Misc:CreateSection("Info")
Misc:CreateLabel("Keybind default: RightControl")
Misc:CreateLabel("Settings: topbar 3 lines icon")
Misc:CreateLabel("Theme button: Light / Dark")

```

## Components

- Window
- Tab
- Button
- Toggle
- Slider
- Dropdown
- Section

## Documentation

See [`docs/API.md`](docs/API.md).

## License

See [`LICENSE`](LICENSE).
