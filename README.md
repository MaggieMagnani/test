-- Obter todos os redstone integrators conectados
local integradores = {}

for _, nome in ipairs(peripheral.getNames()) do
  if peripheral.getType(nome) == "redstone_integrator" then
    table.insert(integradores, peripheral.wrap(nome))
  end
end

if #integradores == 0 then
  print("Nenhum redstone integrator encontrado.")
  return
end

-- Lados possíveis onde as lâmpadas podem estar conectadas
local lados = { "top", "bottom", "left", "right", "front", "back" }

-- Função pra ativar uma lâmpada aleatória em um integrador
local function ativarAleatorio(integrador)
  local lado = lados[mat]()
