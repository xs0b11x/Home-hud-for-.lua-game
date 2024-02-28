Usando o Love2D. Esta interface incluirá um botão "Iniciar Jogo":

Claro! Aqui está um exemplo básico de uma interface inicial para um jogo em Lua usando a biblioteca Love2D. Esta interface incluirá um botão "Iniciar Jogo":

```lua
-- Definição das variáveis
local buttonX = 300
local buttonY = 200
local buttonWidth = 200
local buttonHeight = 50

-- Função para verificar se o mouse está sobre o botão
function isMouseOverButton(x, y, w, h)
    local mouseX, mouseY = love.mouse.getPosition()
    return mouseX >= x and mouseX <= x + w and mouseY >= y and mouseY <= y + h
end

-- Função de desenho da interface
function drawInterface()
    -- Desenha o botão
    love.graphics.setColor(0.4, 0.4, 0.4) -- Define a cor para cinza
    love.graphics.rectangle("fill", buttonX, buttonY, buttonWidth, buttonHeight)

    -- Desenha o texto do botão
    love.graphics.setColor(1, 1, 1) -- Define a cor para branco
    love.graphics.print("Iniciar Jogo", buttonX + 30, buttonY + 15)
end

-- Função chamada quando o botão é clicado
function love.mousepressed(x, y, button)
    if button == 1 and isMouseOverButton(buttonX, buttonY, buttonWidth, buttonHeight) then
        -- Aqui você pode adicionar a lógica para iniciar o jogo
        -- Por exemplo: iniciarJogo()
        print("O jogo foi iniciado!")
    end
end

-- Função de desenho principal do jogo
function love.draw()
    drawInterface()
end
```

Este código desenha um botão "Iniciar Jogo" na tela usando a biblioteca Love2D. Quando o botão é clicado, ele imprime "O jogo foi iniciado!" no console. Você pode adicionar a lógica necessária dentro da função `love.mousepressed` para iniciar o jogo de acordo com suas necessidades.
