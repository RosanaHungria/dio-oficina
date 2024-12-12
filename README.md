# dio-oficina
Esquema conceitual para o contexto de oficina com base na narrativa fornecida
Objetivo:
Criar o esquema conceitual para o contexto de oficina com base na narrativa fornecida para um Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica

Narrativa:
•	Sistema de controle e gerenciamento de execução de ordens de serviço em uma oficina mecânica
•	Clientes levam veículos à oficina mecânica para serem consertados ou para passarem por revisões  periódicas
•	Cada veículo é designado a uma equipe de mecânicos que identifica os serviços a serem executados e preenche uma OS com data de entrega.
•	A partir da OS, calcula-se o valor de cada serviço, consultando-se uma tabela de referência de mão-de-obra
•	O valor de cada peça também irá compor a OS 
•	O cliente autoriza a execução dos serviços
•	A mesma equipe avalia e executa os serviços
•	Os mecânicos possuem código, nome, endereço e especialidade
•	Cada OS possui: n°, data de emissão, um valor, status e uma data para conclusão dos trabalhos.
•	Uma OS pode ser composta por vários serviços e um mesmo serviço pode estar contido em mais de uma OS.
•	Uma OS pode ter vários tipos  de peça e uma peça pode estar presente em mais de uma OS

## Contexto do Projeto
Este projeto foi desenvolvido para atender às necessidades de gestão de ordens de serviço em uma oficina mecânica. O sistema permite o cadastro de clientes, veículos, equipes de mecânicos, serviços e peças, além do acompanhamento detalhado das ordens de serviço.

## Funcionalidades do Sistema
- Gerenciamento de clientes e veículos.
- Emissão de ordens de serviço (OS) associadas a equipes de mecânicos.
- Registro e rastreamento dos serviços realizados e das peças utilizadas em cada OS.
- Cálculo do custo total das OS com base nos serviços e peças associados.
- Controle de status das OS.
  O esquema EER é composto pelas seguintes entidades e relacionamentos principais:
## Entidades Principais
1.	Cliente: Representa os clientes que levam os veículos para reparos ou revisões.
2.	Veículo: Pertence a um cliente e é enviado à oficina para reparos.
3.	Ordem de Serviço (OS): Documento que registra os serviços e peças atribuídos ao veículo, incluindo informações como status, datas e valores.
4.	Equipe: Grupos de mecânicos responsáveis por avaliar e executar os serviços.
5.	Mecânico: Funcionários especializados que realizam os serviços associados às OS.
6.	Serviço: Define o catálogo de serviços disponíveis com valores de mão de obra.
7.	Peça: Define o catálogo de peças disponíveis para uso em reparos.
8.	Serviços da OS: Relaciona os serviços realizados e suas quantidades a uma OS.
9.	Peças da OS: Relaciona as peças utilizadas e suas quantidades a uma OS.
    
## Relacionamentos Identificados
1.	Um Cliente pode possuir vários Veículos, mas cada veículo pertence a apenas um cliente.
2.	Um Veículo pode ter várias OS, mas cada OS está associada a apenas um veículo.
3.	Uma OS é realizada por uma única Equipe, mas uma equipe pode realizar várias OS.
4.	Cada Equipe pode ser composta por vários Mecânicos, e um mecânico pode fazer parte de uma equipe.
5.	Uma OS pode conter vários Serviços, e cada serviço pode aparecer em mais de uma OS.
6.	Uma OS pode conter várias Peças, e cada peça pode aparecer em mais de uma OS.
Relacionamentos:
1.	Cliente - (1:N) - Veículo
2.	Veículo - (1:N) - Ordem de Serviço
3.	Equipe - (1:N) - Ordem de Serviço
4.	Equipe - (1:N) - Mecânico
5.	Ordem de Serviço - (N:M) - Serviço (via Serviço na OS)
6.	Ordem de Serviço - (N:M) - Peça (via Peça na OS)

    

