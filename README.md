# semana19modelagem


aula 1

1. Qual é a diferença entre um comando DDL e um comando DML?
R: O DDL é usado para criar e alterar a estrutura do banco de dados, como tabelas. Já o DML é usado para adicionar, alterar ou excluir os dados dessas tabelas.

2. Quais são os riscos ao executar comandos DDL em um banco de dados em produção?
R: O risco é alterar ou apagar alguma estrutura importante do banco, podendo causar erros no sistema ou até perda de dados.

3. Qual é a vantagem de usar comandos DML em um banco de dados dinâmico?
R: A vantagem é que podemos adicionar, alterar e excluir informações facilmente, deixando o banco de dados sempre atualizado.

aula 2

1. Expliquem a importância de planejar as modificações de estrutura em um banco de dados em produção.

R: É importante planejar antes de fazer alterações para evitar erros, perda de dados ou problemas no funcionamento do sistema. Assim, podemos fazer as mudanças com mais segurança.

2. Qual é a vantagem de definir valores padrão, como no caso da coluna disponibilidade na tabela Menu?

R: A vantagem é que, caso nenhum valor seja informado, o banco de dados já coloca um valor automaticamente. No caso da disponibilidade, ela ficará como **TRUE**, indicando que o item está disponível. Isso facilita o cadastro e evita informações vazias.


aula 3


1. Por que é importante utilizar UPDATE com cuidado em um banco de dados?

R: É importante usar o UPDATE com cuidado porque, se o comando estiver errado, podemos alterar informações que não deveriam ser modificadas. Por isso, é importante usar o `WHERE` para atualizar somente os dados desejados.

2. Quais cuidados devem ser tomados ao excluir dados de clientes ou pedidos, considerando a integridade do banco de dados?

R: Antes de excluir um cliente ou pedido, é importante verificar se existem outros dados relacionados a ele. Isso evita problemas com chaves estrangeiras e ajuda a manter o banco de dados organizado e correto.


aula 4

1. Como vocês podem garantir que a transação será revertida se houver um erro ao inserir dados na tabela Itens_Pedido?

R: Podemos usar o comando `ROLLBACK` caso aconteça algum erro. Assim, todas as alterações feitas durante a transação são desfeitas e nenhum dado fica salvo pela metade.

2. Como a cláusula ROLLBACK pode ser usada para reverter transações parciais em caso de falha em qualquer etapa do processo?

R: O `ROLLBACK` cancela todas as operações feitas desde o início da transação. Por exemplo, se o cliente e o pedido foram cadastrados, mas ocorrer um erro ao adicionar o item, o `ROLLBACK` desfaz tudo, mantendo o banco de dados organizado e correto.
