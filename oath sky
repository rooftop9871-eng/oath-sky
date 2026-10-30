local Lighting = game:GetService("Lighting")

local skyData = {
    SkyboxBk = "rbxassetid://106771111577360",
    SkyboxDn = "rbxassetid://120543510604286",
    SkyboxFt = "rbxassetid://113323211871826",
    SkyboxLf = "rbxassetid://127625156082693",
    SkyboxRt = "rbxassetid://92126106430527",
    SkyboxUp = "rbxassetid://133072754041041"
}

local function applySkybox()
    local sky = Lighting:FindFirstChildOfClass("Sky")
    if not sky then
        sky = Instance.new("Sky")
        sky.Parent = Lighting
    end

    for property, value in pairs(skyData) do
        sky[property] = value
    end
end

applySkybox()

Lighting.ChildRemoved:Connect(function(child)
    if child:IsA("Sky") then
        task.wait()
        applySkybox()
    end
end)
