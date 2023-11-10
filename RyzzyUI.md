# Ryzzy Community Library
## Library 🇧🇷
Discord 
https://discord.gg/3VEWRNvryF

## Tema Roxo 
```lua
local RyzzyLib = loadstring(game:HttpGet(("https://raw.githubusercontent.com/Rhyankkj/UI.library/main/ryzzylib")))()
```
## Tema Vermelho 
```lua
local RyzzyLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/Rhyankkj/UI.library/main/redtheme"))()
```
## Tema Verde
```lua
local RyzzyLib = loadstring(game:HttpGet("https://raw.githubusercontent.com/Rhyankkj/UI.library/main/greentheme"))()
```

## Cria a janela Inicial
```lua
MakeWindow({
  Hub = {
    Title = "Ryzzy Hub",
    Animation = "Ryzzy"
  },
  Key = {
    KeySystem = true,
    Title = "Key System",
    Description = "",
    KeyLink = "",
    Keys = {"123", "321"},
    Notifi = {
      Notifications = true,
      CorrectKey = "Executando o script...",
      Incorrectkey = "A chave está incorreta",
      CopyKeyLink = "Copiado para a área de transferência"
    }
  }
})

--[[
  Hub = {
    Title = "Ryzzy" -- <string> Titulo do seu script
    Animation = "by : Rhyan" -- <string> Adiciona um texto na animacão do seu HUB
  },
  Key = {
    KeySystem = <bollean> Adiciona um sistema de chaves
    Title = "Key System" <string> Adiciona um titulo ao seu sistema de chaves
    Description = "" <string> Adiciona uma descrição ao seu sistema de chaves
    KeyLink = "" <string> Adicina o Link onde pega a chave do HUB
    Keys = {"1234"} <table> Adiciona as Chaves
    Notifi = {
      Notifications = true <boolean> Adicina notificações ao sistema de chaves
      CorrectKey = "Running the Script..." <string> notificação quando a chave estiver correta
      Incorrectkey = "The key is incorrect" <string> notificação quando a chave estiver incorreta
      CopyKeyLink = "Copied to Clipboard" <string> notificação quando o link da chave fir copiado
    }
  }
]]
```

## Botão de minimizar
Adiciona um botão para você minimizar o seu HUB
```lua
MinimizeButton({
  Image = "rbxassetid://11486398809",
  Size = {40, 40},
  Color = Color3.fromRGB(0, 0, 0),
  Corner = true,
  Stroke = false,
  StrokeColor = Color3.fromRGB(255, 0, 0)
})```

--[[
  Image = "" <string> imagem do botão
  Size = {40, 40} <table> tamanho do botão
  Color = Color3.fromRGB(10, 10, 10) <Color3>  Cor do fundo do botäo
  Corner = true -- <boolean> Adicina um UICorner
  Stroke = false <boolean> Adiciona um UIStroke
  StrokeColor = Color3.fromRGB(255, 0, 0) <Color3> Cor do UIStroke
]]
```

## Tab
Cria uma guia
```lua
local Main = MakeTab({Name = "Main"})

--[[
  Name = "Main" <string> Nome da guia
]]
```

## Notificação
Cria uma notificacão
```lua
MakeNotifi({
  Title = "Ryzzy",
  Text = "Notificação teste",
  Time = 5
})

--[[
  Title = "Ryzzy" <string> titulo da notificação
  Text = "Notificação teste" <string> descrição da notificação
  Time = 5 <number> tempo da notificação
]]

```

## Sesão
cria uma sesão
```lua
local section = AddSection(Main, {"Teste"})
--[[
  {"Teste"} <table> nome da janela
]]
```

## Atualizar sesão
Atualiza um texto de uma sesão
```lua
SetSection(section, "Opa")
```

## Botão
cria um botão
```lua
AddButton(Main, {
  Name = "Botão teste",
  Callback = function()
    
  end
})

--[[
  Name = "Botão teste" <string> nome do seu botão
  Callback = function()
    -- funcão do seu botão
  end
]]
```

## caixa de seleção
cria uma caixa de seleção onde você pode alternar entre (true/false)
```lua
local Toggle = AddToggle(Main, {
  Name = "Toggle teste",
  Default = false,
  Callback = function(Value)
    
  end
})

--[[
  Name = "Toggle teste" <string> nome da sua caixa de seleção
  Default = false <boolean> valor padrão
  Callback = function(Value)
    -- função da sua caixa de seleção
  end
]]
```

## Atualizar caixa de seleção
Atualiza o valor atual de uma caixa de seleção
```lua
UpdateToggle(Toggle, true)
```

## controle deslizante
cria um controle deslizante
```lua
local Slider = AddSlider(Main, {
  Name = "Slider teste",
  MinValue = 10,
  MaxValue = 100,
  Default = 25,
  Increase = 1,
  Callback = function(Value)
    
  end
})

--[[
  Name = "Slider teste" <string> nome do controle deslizante
  MinValue = 10 <number> valor minimo
  MaxValue = 100 <number> valor maximo
  Default = 25 <number> valor padrão
  Increase = 1 <number> valor que almenta de acordo com a posição do 
  Callback = function(Value)
    função do controle deslizante
  end
]]
```

## Atualizar controle deslizante
atualiza o valor atual de um controle deslizante
```lua
UpdateSlider(Slider, 25)

--[[
  <number> novo valor do controle deslizante
]]
```

## atalho do teclado
cria um atalho para uma tecla do teclado
```lua
AddKeybind(Main, {
  Name = "Keybind teste",
  KeyCode = "E",
  Default = false,
  Callback = function(Value)
    
  end
})

--[[
  Name = "Keybind teste" <string> nome do atalho do teclado
  KeyCode = "E" <string> tecla
  Default = false <boolean> valor padrã (isso fara funcionar como uma caixa de seleção)
  Callback = function(Value)
    -- função do atalho do teclado
  end
]]
```

## caixa de texto
Cria uma Caixa de Texto
```lua
AddTextBox(Main, {
  Name = "TextBox teste",
  Default = "bom dia",
  PlaceholderText = "teste",
  ClearText = true,
  Callback = function(Value)
    
  end
})

--[[
  Name = "TextBox teste" <string> Nome da caixa de texto
  Default = "bom dia" <string> texto padrão
  PlaceholderText = "teste" <string> texto que mostrará quando a caixa de selecão não tiver nenhum texto
  ClearText = true <boolean> não exclui o texto quando você abre a caixa de texto
  Callback = function(Value)
    -- fucão da caixa de texto
  end
]]
```

## Menu Suspenso
Cria uma lista de opções
```lua
local Dropdown = AddDropdown(Main, {
  Name = "Dropdown teste",
  Options = {"1", "2", "3"},
  Default = "2",
  Callback = function(Value)
    
  end
})

--[[
  Name = "Dropdown teste" <string> nome do menu suspenso
  Options = {"1", "2", "3"} <table> lista de opções
  Default = "2" <string> opção padrão
  Callback = function(Value)
    -- função do menu suspenso
  end
]]
```

## Atualizar Menu suspenso
Atualiza a lista de opções do menu suspenso
```lua
UpdateDropdown(Dropdown, {"um", "dois", "três"})

--[[
  {"um", "dois", "três"} <table> novas opções do menu suspenso
]]
```

## setor de cores
cria um setor de cores
```lua
AddColorPicker(Main, {
  Name = "Color picker teste",
  Default = Color3.fromRGB(255, 255, 0),
  Callback = function(Value)
    
  end
})

--[[
  Name = "Color picker teste" <string> Nome do setor de cores
  Default = Color3.fromRGB(255, 255, 0) <Color3> Define a cor padrão do setor de cores
  Callback = function(Value)
    -- funcão do setor de cores
  end
]]
```

## Texto 
Cria um texto
```lua
local Label = AddTextLabel(Main, "AutoFarm")

--[[
  <string> Texto
]]
```

## Atualizar texto
atualiza um texto
```lua
SetLabel(Label, "HI")

--[[
  <string> novo Texto
]]
```

## Parágrafo
cria um Parágrafo
```lua
local Paragraph = AddParagraph(Main, {"Paragraph teste", "bom dia meus manos"})

--[[
  <string> Nome do Parágrafo
  <string> descrição do Parágrafo
]]
```

## Atualizar Parágrafo
Atualiza um texto de um Parágrafo
```lua
SetParagraph(Paragraph, {"Paragraph", ":>"})

--[[
  <string> novo Nome do Parágrafo
  <string> Nova descrição do Parágrafo
]]
```

## Imagem
cria uma imagem
```lua
local Image = AddImageLabel(Main, {
  Name = "Cool Image",
  Image = "rbxassetid://"
})

--[[
  Name = "Cool Image" <string> Nome da imagem
  Image = "rbxassetid://" <string> id da imagem
]]
```

## Atualizar Imagem
atualiza uma imagem
```lua
SetImage(Image, "rbxassetid://4155801252")

--[[
  <string> Nova imagem
]]
```

## Destruir o script
DestroyScript()

# Extra
## Caixa de seleção Mobile
Adicina uma caixa de seleção que fica voando na tela
```lua
local MobileToggle = AddMobileToggle({
  Name = "Toggle",
  Visible = true,
  Callback = function(Value)
    
  end
})

MobileToggle.Visible = (false/true)

--[[
  Name = "Toggle" <string> Nome da caixa de seleção
  Visible = false <boolean> coloca ela invisivel ou visivel
  Callback = function()
    -- função da caixa de seleção
  end
]]
```
