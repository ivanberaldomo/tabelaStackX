Script para qualquer banco de dados compatível com SQL

Visão Geral do Design do Banco de Dados

    Principais Características

        Chaves Primárias (Primary Key)

            Cada tabela possui uma coluna *_id configurada como chave primária para garantir a unicidade de cada registro.

        Chaves Estrangeiras (Foreign Key)

            Os relacionamentos entre as tabelas são garantidos por chaves estrangeiras, como o campo user_id na tabela places, que indica quem cadastrou o lugar.

            A configuração ON DELETE CASCADE assegura que registros relacionados sejam removidos automaticamente, mantendo a integridade referencial do banco de dados.

        Restrições e Configurações

            Unicidade: Campos como email são configurados como únicos na tabela users.

            Validação: O campo rating na tabela reviews possui uma restrição que limita os valores de avaliação entre 1 e 5 estrelas.

            Controle de Tempo: Os campos created_at e updated_at são gerados automaticamente para registrar as datas de criação e atualização dos registros.

        Escalabilidade

            O design é modular e extensível, permitindo a adição de novas funcionalidades no futuro.

            Exemplos de possíveis expansões incluem tabelas para armazenar imagens, processar pagamentos ou organizar categorias de lugares, sem impactar a estrutura inicial.