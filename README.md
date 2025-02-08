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

### Amei o processo de criação do projeto, estou muito orgulhosa do meu resultado e sempre aberta a dicas de melhorias!
