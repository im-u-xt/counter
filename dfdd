-- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local TextLabel2 = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.CoreGui

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
Frame.BorderColor3 = Color3.fromRGB(50, 50, 50)
Frame.Position = UDim2.new(0.77241379, 0, 0.806387305, 0)
Frame.Size = UDim2.new(0, 100, 0, 29)

TextLabel.Parent = Frame
TextLabel.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
TextLabel.BorderColor3 = Color3.fromRGB(50, 50, 50)
TextLabel.Position = UDim2.new(0.295813501, 0, 0.175876066, 0)
TextLabel.Size = UDim2.new(0, 38, 0, 16)
TextLabel.Font = Enum.Font.GothamBlack
TextLabel.Text = "0"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 9.000

TextLabel2.Name = "TextLabel2"
TextLabel2.Parent = Frame
TextLabel2.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
TextLabel2.BorderColor3 = Color3.fromRGB(35, 35, 35)
TextLabel2.Position = UDim2.new(0, 0, -0.594720244, 0)
TextLabel2.Size = UDim2.new(0, 100, 0, 17)
TextLabel2.Font = Enum.Font.SourceSansBold
TextLabel2.Text = "Retain X Premium"
TextLabel2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel2.TextSize = 12.000

-- Scripts:

function runScript()
	local script = Instance.new('LocalScript', TextLabel)
	while wait() do
		pcall(function()
			local amount = 0
			for i,v in pairs(game.Workspace.Ignored.Drop:GetChildren()) do
				if v.Name == "MoneyDrop" then
					local cash = string.split(v.BillboardGui.TextLabel.Text,"$")[2]
					if string.match(cash,',') then
						amount = amount + cash:gsub("%,","")
					else
						amount = amount + cash
					end
				end
			end
			local function checking(amount)
				amount = tostring(amount)
				return amount:reverse():gsub("%d%d%d", "%1,"):reverse():gsub("^,", "")
			end
			script.Parent.Text = "$"..checking(amount).." dropped"
		end)
	end
end
coroutine.wrap(runScript)()
