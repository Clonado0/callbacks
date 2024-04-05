Client:   local result = TriggerServerCallback('eventName')

Server: RegisterServerCallback('eventName', function(source, cb)
    local src = source
    for k, player in ipairs(GetPlayers()) do
        local Character = VORPcore.getUser(player).getUsedCharacter
        if Character.job == "doctor" then
        else
            return true
        end
    end
end)
