# XCUHUB Documentation (Code: Rayfield)

## Loadstring loader
```lua
local XCU = loadstring(game:HttpGet(('https://raw.githubusercontent.com/WackyWorId/RayfieldA1R/main/Main')))()
```
## Creating a Window
```lua
local XCUWINDOW = XCU:CreateWindow({
   Name = "Your title here",
   LoadingTitle = "XCU HUB",
   LoadingSubtitle = "game title",
   ConfigurationSaving = {
      Enabled = true,
      FolderName = "Xecutioner", --The folder for the hub
      FileName = "Your file name here"
   },
   Discord = {
      Enabled = false,
      Invite = "nodiscorddotggslash", -- Make sure to put invite code only
      RememberJoins = true -- Set this to false to make them join the discord every time they load it up
   },
   KeySystem = false, -- Set this to true to use the key system
   KeySettings = {
      Title = "XCU HUB",
      Subtitle = "Verify key",
      Note = "Get key from linkvertise",
      FileName = "XCUKey",
      SaveKey = true,
      GrabKeyFromSite = true, -- If this is true, set Key below to the RAW site you would like Rayfield to get the key from
      Key = https://raw.githubusercontent.com/WackyWorId/Main-key/main/XCUKEY
   }
})
```


## Creating a Tab
```lua
local Tab = XCUWINDOW:CreateTab("My tab", 4483362458) -- Title, Image
```

## Creating a Section
```lua
local Section = Tab:CreateSection("My section")
```

# Buttons/Elements

## Notify
```lua
XCU:Notify({
   Title = "Your title",
   Content = "Description",
   Duration = 6.5, --How long it will last for
   Image = 4483362458,
   Actions = { -- Notification Actions
      Ignore = {
         Name = "Okay!",
         Callback = function()
          --Add code here
      end
   },
},
})
```

## Button
```lua
local Button = Tab:CreateButton({
   Name = "Name",
   Callback = function()
   -- The function that takes place when the button is pressed
   end,
})
```
## Toggle
```lua
local Toggle = Tab:CreateToggle({
   Name = "Your toggle title",
   CurrentValue = false, --Make this true to set this always to true when loaded.
   Flag = "Toggle1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to
   ensure no overlaps!
   Callback = function(Tog)
   -- The function that takes place when the toggle is pressed
   -- The variable (Tog) is a boolean on whether the toggle is true or false (Ex: if tog == true/false then)
   end,
})
```

## Slider
```lua
local Slider = Tab:CreateSlider({
   Name = "Your slider name",
   Range = {0, 100},
   Increment = 10,
   Suffix = "yoursuffix",
   CurrentValue = 10, --This is the value that sets the slider number when loaded first time.
   Flag = "Slider1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(numb)
   -- The function that takes place when the slider changes
   -- The variable (numb) is a number which correlates to the value the slider is currently at
   end,
})
```
## Updating slider
```lua
Slider:Set(10) -- The new slider value/number
```

## Dropdown menu
```lua
local Dropdown = Tab:CreateDropdown({
   Name = "Your dropdown name",
   Options = {"Option 1"},
   CurrentOption = "--Choose--",
   Flag = "Dropdown1", -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
   Callback = function(Option)
   -- The function that takes place when the selected option is changed
   -- The variable (Option) is a string for the value that the dropdown was changed to
   end,
})
```
## Update dropdown
```lua
Dropdown:Set("Your option") -- The new option thats setted
```
## End of documentation.
