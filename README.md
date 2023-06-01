-- by 4ttach
-- bypass script 1week
-- wroge ban 1day this beta on

local ChatBypass = Instance.new("ScreenGui")
local TextBox = Instance.new("TextBox")
local TextButton = Instance.new("TextButton")
 
ChatBypass.Name = "ChatBypass"
ChatBypass.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ChatBypass.ZIndexBehavior = Enum.ZIndexBehavior.Sibling
 
TextBox.Parent = ChatBypass
TextBox.AnchorPoint = Vector2.new(0, 1)
TextBox.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
TextBox.BackgroundTransparency = 0.500
TextBox.BorderColor3 = Color3.fromRGB(0, 0, 0)
TextBox.Position = UDim2.new(0, 0, 1, 0)
TextBox.Size = UDim2.new(1, 0, 0.100000001, 0)
TextBox.ZIndex = 100
TextBox.ClearTextOnFocus = false
TextBox.Font = Enum.Font.Code
TextBox.PlaceholderColor3 = Color3.fromRGB(178, 178, 178)
TextBox.PlaceholderText = "Enter Text To Bypass"
TextBox.Text = ""
TextBox.TextColor3 = Color3.fromRGB(255, 255, 255)
TextBox.TextScaled = true
TextBox.TextSize = 14.000
TextBox.TextWrapped = true
 
TextButton.Parent = TextBox
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.Size = UDim2.new(0.0500000007, 0, 1, 0)
TextButton.ZIndex = 101
TextButton.Style = Enum.ButtonStyle.RobloxRoundDropdownButton
TextButton.Font = Enum.Font.SciFi
TextButton.Text = "X"
TextButton.TextColor3 = Color3.fromRGB(0, 0, 0)
TextButton.TextScaled = true
TextButton.TextSize = 14.000
TextButton.TextStrokeColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextStrokeTransparency = 0.000
TextButton.TextWrapped = true
 
local function PHLLGL_fake_script() -- TextBox.LocalScript
    local script = Instance.new('LocalScript', TextBox)
 
    local box = script.Parent
    local focused = false
   
    box.Focused:Connect(function()
        focused = true
    end)
   
    box.FocusLost:Connect(function()
        focused = false
    end)
   
    function bypass(msg)
            local bypassedAlphebet = {
                ["a"] = "ٴٴa",
                ["b"] = "ٴٴb",
                ["c"] = "ٴٴc",
                ["d"] = "ٴٴd",
                ["e"] = "ٴٴe",
                ["f"] = "ٴٴf",
                ["g"] = "ٴٴg",
                ["h"] = "ٴٴh",
                ["i"] = "ٴٴi",
                ["j"] = "ٴٴj",
                ["k"] = "ٴٴk",
                ["l"] = "ٴٴl",
                ["m"] = "ٴٴm",
                ["n"] = "ٴٴn",
                ["o"] = "ٴٴo",
                ["p"] = "ٴٴp",
                ["q"] = "ٴٴq",
                ["r"] = "ٴٴr",
                ["s"] = "ٴٴs",
                ["t"] = "ٴٴt",
                ["u"] = "ٴٴu",
                ["v"] = "ٴٴv",
                ["w"] = "ٴٴw",
                ["x"] = "ٴٴx",
                ["y"] = "ٴٴy",
                ["z"] = "ٴٴz"
            }
            local msgChars = string.split(msg,"")
            local bypassedMsg = ""
            for i,v in pairs(msgChars) do
                local bypassedChar = bypassedAlphebet[v:lower()]
                bypassedMsg = bypassedMsg..bypassedChar
                if v == v:upper() then -- if 'v' is uppercase
                    bypassedChar = bypassedChar:upper()
                end
            end
            wait()
            box.Text = bypassedMsg
            box:CaptureFocus()
            wait()
            box.SelectionStart = 1
            box.CursorPosition = string.len(box.Text)+1
            wait()
    end
   
    game:GetService("UserInputService").InputBegan:Connect(function(k)
        if k.KeyCode == Enum.KeyCode.Return then
            bypass(box.Text)
        end
    end)
end
coroutine.wrap(PHLLGL_fake_script)()
local function OTFF_fake_script() -- TextButton.LocalScript
    local script = Instance.new('LocalScript', TextButton)
 
    -- game.Players.LocalPlayer:GetMouse().Icon = "rbxassetid://4563813357"
   
    script.Parent.MouseEnter:Connect(function()
        -- game.Players.LocalPlayer:GetMouse().Icon = "rbxassetid://4563813357"
    end)
   
    script.Parent.MouseLeave:Connect(function()
        game.Players.LocalPlayer:GetMouse().Icon = ""
    end)
   
    script.Parent.MouseButton1Down:Connect(function()
        script.Parent.Parent.Parent:Destroy()
    end)
end
coroutine.wrap(OTFF_fake_script)()
