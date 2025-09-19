graph TD
    subgraph Sistema de E-commerce
        subgraph Gerenciamento de Clientes
            C1[Cadastrar Cliente]
            C2[Login]
            C3[Atualizar Perfil]
            C4[Visualizar Histórico de Pedidos]
        end

        subgraph Processamento de Pedidos
            P1[Buscar Produtos]
            P2[Adicionar ao Carrinho]
            P3[Checkout]
            P4[Efetuar Pagamento]
        end

        subgraph Administração
            A1[Gerenciar Produtos]
            A2[Gerenciar Pedidos]
            A3[Gerenciar Clientes]
        end
    end

    actor_cliente(Cliente)
    actor_admin(Administrador)

    actor_cliente --> C1
    actor_cliente --> C2
    actor_cliente --> C3
    actor_cliente --> C4
    actor_cliente --> P1
    actor_cliente --> P2
    actor_cliente --> P3
    actor_cliente --> P4

    actor_admin --> C2
    actor_admin --> A1
    actor_admin --> A2
    actor_admin --> A3

    A2 --> P4
