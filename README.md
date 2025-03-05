# Modelo Banco de Dados para uma Oficina  
Projeto proposto no bootcamp da Dio em parceria com a Heineken para a criação, do zero, de um banco de dados para uma oficina.  

## Pontos em consideração do projeto:  
- Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões periódicas;  
- Cada veículo é designado a uma equipe de mecânicos, que identifica os serviços a serem executados e preenche uma OS com a data de entrega;  
- A partir da OS, calcula-se o valor de cada serviço, consultando uma tabela de referência de mão de obra;  
- O valor de cada peça também compõe a OS, e o cliente autoriza a execução dos serviços;  
- A mesma equipe avalia e executa os serviços;  
- Os mecânicos possuem código, nome, especialidade e podem integrar diferentes equipes;  
- Cada OS possui: número, data de emissão, valor, status e uma data para a conclusão dos trabalhos.  

## Como eu fiz  
Primeiro, eu criei um modelo bem simples no **draw.io** para ter uma visualização das entidades e seus relacionamentos. Depois, no **Workbench do MySQL**, comecei a separar as entidades e seus atributos.  

Removi o atributo **"endereço"** dos mecânicos e o adicionei à entidade **clientes**, pois fazia mais sentido armazenar essa informação lá. Também adicionei atributos para armazenar informações sobre o veículo e conectei tanto o **veículo quanto o cliente à OS (Ordem de Serviço)**.  

A OS possui um **relacionamento com a tabela de orçamento**, para registrar os custos ao cliente, e com a **tabela de peças**, que contém os itens necessários durante o processo.  

Já os **mecânicos foram vinculados à entidade-relacionamento "Equipe"**, que os conecta à OS, tornando o sistema mais distribuído e organizado.  

# Segunda parte do projeto
Agora na segunda parte o desafio proposto foi ajustar alguns pontos na modelagem inicial para que pudesse ser feito a criação do banco de dados e alguns testes de perguntas que podem ser respondidas.
### Pontos que ajustei na minha modelagem
1. Criei um campo separado para pagamento, para que possa ser adicionado mais de uma forma de pagamento,
2. Criação de 2 tabelas, uma para CPF e uma para CNPJ. Utilizei a tabela de CPF tanto para clientes quanto para funcionarios, sendo dividido pelo tipo.O CNPJ era exclusivamente para clientes.
3. Adicionei uma tabela intermediaria entre funcionarios e equipes para que uma equipe possa ter mais de um funcionario.
### Como fiz a minha criação
1. Defini toda a minha tabela conforme estava no modelo, começando pelas tabelas que não iriam precisar de nenhuma chave estrangeira,
2. Definir um trigger para que meu cliente possa escolher entre um CNPJ ou um CPF,
3. Adicionei tanto mas minhas chaves primarias quanto as minhas chaves estrangeiras em constraint para que eu pudesse recupera-las depois.
4. 
### Insights que podem ser retirados do meu banco de dados
1. Quais metodos de pagamento mais usados?
2. Qual serviço é mais vendido?
3. Qual equipe atende mais?
4. Quantos serviços ja foram finalizar e quantos foram cancelados?
5. Qual marca mais é solicitado o conserto?
6. Quais pecas são mais requisitadas?

### Amei o processo de criação do projeto, estou muito orgulhosa do meu resultado e sempre aberta a dicas de melhorias!

