game.Players.PlayerAdded:Connect(function(player)
    local backpack = player:WaitForChild("Backpack")

    for _, weapon in pairs(game.ServerStorage.Guns:GetDescendants()) do
        if weapon:IsA("Tool") then
            weapon:Clone().Parent = backpack
        end
    end
end)
