-- Função para verificar a cor de uma bola
function verificarCor(bola)
    local cor = bola.BrickColor -- Verifica a cor da bola
    return cor == BrickColor.new("Bright red") or cor == BrickColor.new("Bright yellow") or cor == BrickColor.new("Bright blue")
end

-- Encontrar todas as bolas no jogo
local bolas = workspace:GetDescendants() -- Pega todos os objetos no ambiente

-- Iterar sobre todas as bolas e verificar a cor
for _, objeto in ipairs(bolas) do
    if objeto:IsA("Part") and verificarCor(objeto) then
        -- Se o objeto é uma bola e tem a cor desejada
        print("Bola encontrada com a cor: " .. objeto.BrickColor.Name)
        -- Aqui você pode adicionar código para pegar a bola ou interagir com ela
    end
end
