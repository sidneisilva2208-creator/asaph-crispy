# Asaph Crispy - TODO

## v1 — Base

- [x] Schema do banco: tabelas products, categories, orders, order_items, loyalty_points, loyalty_transactions
- [x] Migração SQL aplicada
- [x] Helpers de DB em server/db.ts
- [x] Rotas tRPC: produtos (CRUD), pedidos, fidelidade, admin
- [x] Gerar imagens IA para produtos de exemplo
- [x] Página inicial (landing) com visual elegante/sofisticado
- [x] Cardápio com categorias e produtos
- [x] Carrinho lateral (drawer) com add/remover/ajustar quantidade
- [x] Total em tempo real no carrinho
- [x] Finalização via WhatsApp com mensagem formatada
- [x] Aplicação de desconto por pontos no checkout
- [x] Login/cadastro de clientes via OAuth
- [x] Exibir saldo de pontos do cliente logado
- [x] Acumular pontos após cada pedido
- [x] Resgatar pontos como desconto no pedido
- [x] Página de perfil com histórico de pontos e pedidos
- [x] Rota /admin protegida por role=admin
- [x] Gerenciar produtos: adicionar, editar, remover
- [x] Visualizar pedidos recebidos com troca de status
- [x] Gerenciar clientes e saldos de pontos
- [x] Configurar WhatsApp, endereço, horários e taxa de pontos
- [x] Testes Vitest (23 testes passando)

## v2 — Evolução Profissional

- [x] Campos ao orders: customerAddress, customerPhone, deliveryType, deliveryFee, neighborhood
- [x] Tabela delivery_zones: id, name, fee, estimatedMinutes, active
- [x] Tabela product_ingredients: id, productId, name, unit, quantity, costPerUnit
- [x] Tabela sales_goals: id, month, year, targetAmount, notes
- [x] Tabela cash_closings: id, date, openingBalance, totalSales, totalOrders, closingBalance, notes
- [x] Tabela loyalty_rewards: id, name, description, pointsCost, productId, active
- [x] Tabela message_broadcasts: id, title, message, sentAt, recipientCount
- [x] Rotas tRPC para todas as novas entidades
- [x] Remover categorias pastéis e empadinhas — manter só coxinhas e bebidas
- [x] Formulário de checkout com nome, telefone, endereço, número, bairro
- [x] Seleção retirada/entrega com taxa automática por bairro
- [x] Cálculo automático do total com taxa de entrega
- [x] Dashboard: cards vendas do dia, vendas do mês, total pedidos, ticket médio
- [x] Gráfico de área de vendas por dia (últimos 30 dias)
- [x] Top produtos mais vendidos
- [x] Fechamento de caixa: saldo inicial, total vendas, saldo final
- [x] Meta de vendas do mês com barra de progresso
- [x] Cadastro de recompensas (produtos resgatáveis por pontos)
- [x] Cliente pode trocar pontos por produtos no checkout
- [x] Painel admin: compor mensagem e selecionar destinatários
- [x] Histórico de transmissões enviadas
- [x] Cadastro de insumos por produto (nome, unidade, quantidade, custo unitário)
- [x] Cálculo automático do custo total de produção por produto
- [x] Margem de lucro: preço de venda vs custo calculado
- [x] Painel admin com sidebar responsiva (mobile hamburger + desktop fixo)
- [x] Testes Vitest expandidos (49 testes, 0 falhas)

## v3 — Cadastro de Conta e Endereço Salvo

- [x] Adicionar campos de perfil na tabela users: phone, address, addressNumber, neighborhood, deliveryZoneId, birthdate
- [x] Rota tRPC profile.get e profile.save para buscar e salvar dados do cliente
- [x] Página de perfil completa com formulário de cadastro e edição
- [x] Preenchimento automático do endereço no checkout quando cliente está logado
- [x] Exibir badge "Endereço salvo" no checkout quando dados já existem
- [x] Testes atualizados para profile.save

## v4 — Pontos por Entrega e Avaliação

- [x] Remover crédito imediato de pontos ao criar pedido
- [x] Creditar pontos apenas quando admin marcar pedido como "Entregue"
- [x] Adicionar campos rating (1-5) e ratingComment na tabela orders
- [x] Rota tRPC orders.rate para o cliente avaliar o pedido
- [x] Rota tRPC orders.updateStatus atualizar para creditar pontos ao marcar "Entregue"
- [x] UI de avaliação no perfil do cliente (estrelas + comentário)
- [x] Mostrar pedidos aguardando avaliação em destaque no perfil
- [x] Exibir média de avaliações no painel admin (dashboard e lista de pedidos)
- [x] Testes atualizados para o novo fluxo
