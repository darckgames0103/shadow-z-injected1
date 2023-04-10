local ts = game:GetService('TweenService')

-- // TweenInfo \\ --

local info = TweenInfo.new(
    0.9,
    Enum.EasingStyle.Quint,
    Enum.EasingDirection.Out
)

local Main = Instance.new("ScreenGui")
local InjectedFrame = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local DropShadowHolder = Instance.new("Frame")
local DropShadow = Instance.new("ImageLabel")
local Icon = Instance.new("ImageLabel")
local Blur = Instance.new("BlurEffect")

Main.Name = "Main"
Main.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")

InjectedFrame.Name = "InjectedFrame"
InjectedFrame.Parent = Main
InjectedFrame.AnchorPoint = Vector2.new(0.5, 0.5)
InjectedFrame.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
InjectedFrame.BackgroundTransparency = 1.000
InjectedFrame.Position = UDim2.new(0.5, 0, 0.5, 0)
InjectedFrame.Size = UDim2.new(0, 170, 0, 170)

UICorner.CornerRadius = UDim.new(0, 6)
UICorner.Parent = InjectedFrame

DropShadowHolder.Name = "DropShadowHolder"
DropShadowHolder.Parent = InjectedFrame
DropShadowHolder.BackgroundTransparency = 1.000
DropShadowHolder.BorderSizePixel = 0
DropShadowHolder.Size = UDim2.new(1, 0, 1, 0)
DropShadowHolder.ZIndex = 0

DropShadow.Name = "DropShadow"
DropShadow.Parent = DropShadowHolder
DropShadow.AnchorPoint = Vector2.new(0.5, 0.5)
DropShadow.BackgroundTransparency = 1.000
DropShadow.BorderSizePixel = 0
DropShadow.Position = UDim2.new(0.5, 0, 0.5, 0)
DropShadow.Size = UDim2.new(1, 47, 1, 47)
DropShadow.ZIndex = 0
DropShadow.Image = "rbxassetid://6014261993"
DropShadow.ImageColor3 = Color3.fromRGB(0, 0, 0)
DropShadow.ImageTransparency = 1.000
DropShadow.ScaleType = Enum.ScaleType.Slice
DropShadow.SliceCenter = Rect.new(49, 49, 450, 450)

Icon.Name = "Icon"
Icon.Parent = InjectedFrame
Icon.AnchorPoint = Vector2.new(0.5, 0.5)
Icon.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
Icon.BackgroundTransparency = 1.000
Icon.Position = UDim2.new(0.499705911, 0, 0.497941196, 0)
Icon.Size = UDim2.new(0, 140, 0, 140)
Icon.Image = "rbxassetid://13063642390"
Icon.ImageTransparency = 1.000

Blur.Enabled = true
Blur.Size = 0
Blur.Parent = game:GetService("Lighting")

ts:Create(
    Blur,
    info,
    {
        Size = 24
    }
):Play()

ts:Create(
    InjectedFrame,
    info,
    {
        BackgroundTransparency = 0
    }
):Play()

ts:Create(
    DropShadow,
    info,
    {
        ImageTransparency = 0
    }
):Play()

ts:Create(
    Icon,
    info,
    {
        ImageTransparency = 0
    }
):Play()

task.wait(1)

ts:Create(
    DropShadow,
    info,
    {
         ImageColor3 = Color3.fromRGB(86, 224, 58)
    }
):Play()

task.wait(2)

ts:Create(
    Icon,
    info,
    {
        ImageTransparency = 1
    }
):Play()

task.wait(1)

ts:Create(
    InjectedFrame,
    info,
    {
        BackgroundTransparency = 1
    }
):Play()

ts:Create(
    InjectedFrame,
    info,
    {
        Size = UDim2.new(0, 0, 0, 0)
    }
):Play()

ts:Create(
    DropShadow,
    info,
    {
        Size = UDim2.new(0, 0, 0, 0)
    }
):Play()

ts:Create(
    Blur,
    info,
    {
        Size = 0
    }
):Play()


ts:Create(
    DropShadow,
    info,
    {
        ImageTransparency = 1
    }
):Play()
