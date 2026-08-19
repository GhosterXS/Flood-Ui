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
--[[
    Flood Ui - Example (Showcase Only)
    Shows available functions. Callbacks are empty on purpose.
    GitHub: GhosterXS/Flood-Ui
]]

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/GhosterXS/Flood-Ui/refs/heads/main/Flood%20Ui"))()

local Window = Library:CreateWindow({
    Name = "Flood Ui Example",
    LoadingTitle = "Flood Ui",
    LoadingSubtitle = "Interface Example",
    Theme = Color3.fromRGB(255, 255, 255)
})

local Tab = Window:CreateTab("Example Tab")
local Tab2 = Window:CreateTab("Another Tab")

------------------------------------------------
-- Example Tab
------------------------------------------------
Tab:CreateSection("Section Example")

local Label = Tab:CreateLabel("Label Example")
-- Label:Set("Updated Label")

Tab:CreateButton({
    Name = "Button Example",
    Callback = function()
        -- The function that takes place when the button is pressed
    end
})

local Toggle = Tab:CreateToggle({
    Name = "Toggle Example",
    Default = false,
    Callback = function(Value)
        -- Value is true or false
    end
})
-- Toggle:Set(true)
-- Toggle:Get()

Tab:CreateSlider({
    Name = "Slider Example",
    Min = 0,
    Max = 100,
    Default = 50,
    Callback = function(Value)
        -- Value is the current number
    end
})

Tab:CreateDropdown({
    Name = "Dropdown Example",
    Options = {"Option 1", "Option 2", "Option 3"},
    Default = "Option 1",
    Callback = function(Value)
        -- Value is the selected option
    end
})

Library:Notify({
    Title = "Notification Title",
    Content = "Notification Content",
    Duration = 4
})

------------------------------------------------
-- Another Tab
------------------------------------------------
Tab2:CreateSection("Section Example 2")

Tab2:CreateLabel("Label Example 2")

Tab2:CreateButton({
    Name = "Button Example 2",
    Callback = function()
        -- The function that takes place when the button is pressed
    end
})

Tab2:CreateToggle({
    Name = "Toggle Example 2",
    Default = false,
    Callback = function(Value)
        -- Value is true or false
    end
})

Tab2:CreateSlider({
    Name = "Slider Example 2",
    Min = 0,
    Max = 100,
    Default = 25,
    Callback = function(Value)
        -- Value is the current number
    end
})

Tab2:CreateDropdown({
    Name = "Dropdown Example 2",
    Options = {"Option A", "Option B", "Option C"},
    Default = "Option A",
    Callback = function(Value)
        -- Value is the selected option
    end
})

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
