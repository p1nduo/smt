local lp = game:GetService("Players").LocalPlayer
local invUI = lp.PlayerGui:WaitForChild("UI"):WaitForChild("Menus"):WaitForChild("Inventory")
local sg = Instance.new("ScreenGui")
sg.Name = "InvToggle"
sg.Parent = lp.PlayerGui
local btn = Instance.new("TextButton")
btn.Size = UDim2.new(0,110,0,36)
btn.Position = UDim2.new(0.01,0,0.35,0)
btn.BackgroundColor3 = Color3.fromRGB(28,28,28)
btn.TextColor3 = Color3.new(1,1,1)
btn.Text = "v1"
btn.TextSize =17
btn.Font = Enum.Font.Gotham
btn.Parent = sg
local closeBtn = Instance.new("TextButton")
closeBtn.Size = UDim2.new(0,32,0,32)
closeBtn.Position = UDim2.new(0.01, 118, 0.35, 0)
closeBtn.BackgroundColor3 = Color3.fromRGB(180,30,30)
closeBtn.TextColor3 = Color3.new(1,1,1)
closeBtn.Text = "❌"
closeBtn.TextSize =20
closeBtn.Font = Enum.Font.Gotham
closeBtn.Parent = sg
btn.MouseButton1Click:Connect(function()
	invUI.Visible = not invUI.Visible
end)
closeBtn.MouseButton1Click:Connect(function()
	sg.Enabled = false
end)
