-- Gui to Lua
-- Version: 3.2

-- Instances:

local RadiantTowerOfHell = Instance.new("ScreenGui")
local Topbar = Instance.new("ImageLabel")
local TowerOfHell = Instance.new("TextLabel")
local Line = Instance.new("ImageLabel")
local UIGradient = Instance.new("UIGradient")
local ScrollingFrame = Instance.new("ScrollingFrame")
local Frame = Instance.new("Frame")
local Button = Instance.new("ImageButton")

--Properties:

RadiantTowerOfHell.Name = "Radiant-TowerOfHell"
RadiantTowerOfHell.Parent = game.CoreGui

Topbar.Name = "Topbar"
Topbar.Parent = RadiantTowerOfHell
Topbar.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Topbar.BackgroundTransparency = 1.000
Topbar.Position = UDim2.new(0.00907715596, 0, 0.0212443098, 0)
Topbar.Size = UDim2.new(0, 163, 0, 33)
Topbar.Image = "rbxassetid://3570695787"
Topbar.ImageColor3 = Color3.fromRGB(15, 15, 15)
Topbar.ScaleType = Enum.ScaleType.Slice
Topbar.SliceCenter = Rect.new(100, 100, 100, 100)
Topbar.SliceScale = 0.040

TowerOfHell.Name = "TowerOfHell"
TowerOfHell.Parent = Topbar
TowerOfHell.Active = true
TowerOfHell.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TowerOfHell.BackgroundTransparency = 1.000
TowerOfHell.Size = UDim2.new(0, 104, 0, 33)
TowerOfHell.Font = Enum.Font.SourceSansSemibold
TowerOfHell.Text = "TOWER OF HELL"
TowerOfHell.TextColor3 = Color3.fromRGB(255, 255, 255)
TowerOfHell.TextSize = 14.000

Line.Name = "Line"
Line.Parent = Topbar
Line.Active = true
Line.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
Line.BackgroundTransparency = 1.000
Line.Position = UDim2.new(0, 0, 0.939393997, 0)
Line.Size = UDim2.new(0, 163, 0, 2)
Line.Image = "rbxassetid://3570695787"
Line.ScaleType = Enum.ScaleType.Slice
Line.SliceCenter = Rect.new(100, 100, 100, 100)
Line.SliceScale = 0.040

UIGradient.Color = ColorSequence.new{ColorSequenceKeypoint.new(0.00, Color3.fromRGB(182, 141, 159)), ColorSequenceKeypoint.new(1.00, Color3.fromRGB(64, 96, 161))}
UIGradient.Parent = Line

ScrollingFrame.Parent = Topbar
ScrollingFrame.Active = true
ScrollingFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
ScrollingFrame.BorderColor3 = Color3.fromRGB(20, 20, 20)
ScrollingFrame.BorderSizePixel = 0
ScrollingFrame.Position = UDim2.new(0, 0, 1, 0)
ScrollingFrame.Size = UDim2.new(0, 163, 0, 0)
ScrollingFrame.ScrollBarThickness = 0
ScrollingFrame.ScrollingEnabled = false

Frame.Parent = ScrollingFrame
Frame.Active = true
Frame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
Frame.BorderColor3 = Color3.fromRGB(20, 20, 20)
Frame.Size = UDim2.new(0, 163, 0, 250)

Button.Name = "Button"
Button.Parent = RadiantTowerOfHell
Button.BackgroundTransparency = 1.000
Button.Position = UDim2.new(0.110438727, 0, 0.0303490125, 0)
Button.Rotation = 180.000
Button.Size = UDim2.new(0, 20, 0, 20)
Button.ZIndex = 2
Button.Image = "rbxassetid://3926307971"
Button.ImageRectOffset = Vector2.new(324, 524)
Button.ImageRectSize = Vector2.new(36, 36)

-- Scripts:
	local script = Instance.new('LocalScript', RadiantTowerOfHell)

	Topbar = script.Parent.Topbar
	ScrollingFrame = script.Parent.Topbar.ScrollingFrame
	Button = script.Parent.Button
	
	Button.MouseButton1Down:Connect(function()
		if Button.Rotation == 180 then
			wait(0.025)
			Button.Rotation = 90
			wait(0.025)
			Button.Rotation = 60
			wait(0.025)
			ScrollingFrame:TweenSize(UDim2.new(0, 163,0, 250), "Out", "Sine", 0.25)
			Button.Rotation = 30
			wait(0.025)
			Button.Rotation = 0
		elseif
			Button.Rotation == 0 then
			wait(0.025)
			Button.Rotation = 0
			wait(0.025)
			Button.Rotation = 30
			wait(0.025)
			ScrollingFrame:TweenSize(UDim2.new(0, 163,0, 0), "Out", "Sine", 0.25)
			Button.Rotation = 60
			wait(0.025)
			Button.Rotation = 90
			wait(0.025)
			Button.Rotation = 180
		
		end
	end)
